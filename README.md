# Speed up secp256k1 with endomorphism

<p>In this article, we will look&nbsp;&nbsp;<code>secp256k1</code>&nbsp;at the endomorphism acceleration function that helps in optimizing the validation&nbsp;&nbsp;<code>ECDSA</code>&nbsp;for the Bitcoin cryptocurrency, but first, a little history.</p>
<blockquote class="wp-block-quote"><p><code>12 января 2009 года</code>&nbsp;<a href="https://ru.wikipedia.org/wiki/%D0%A1%D0%B0%D1%82%D0%BE%D1%81%D0%B8_%D0%9D%D0%B0%D0%BA%D0%B0%D0%BC%D0%BE%D1%82%D0%BE" target="_blank" rel="noreferrer noopener">Satoshi Nakamoto sent&nbsp;</a><a href="https://ru.wikipedia.org/wiki/%D0%93%D0%B0%D1%80%D0%BE%D0%BB%D1%8C%D0%B4_%D0%A2%D0%BE%D0%BC%D0%B0%D1%81_%D0%A4%D0%B8%D0%BD%D0%BD%D0%B8_II" target="_blank" rel="noreferrer noopener">Hal Finney</a>&nbsp;&nbsp;&nbsp;in the earliest bitcoin transactions&nbsp;&nbsp;<code>10 BTC</code>.</p></blockquote>
<p>That Satoshi Nakamoto chose Hal as the first recipient of Bitcoins is not surprising.&nbsp;Satoshi had great respect for Hal, who established himself as one of the world’s brightest programmers and cryptographers by developing the&nbsp;&nbsp;<a href="https://ru.wikipedia.org/wiki/PGP" target="_blank" rel="noreferrer noopener">PGP</a>&nbsp;encryption system .&nbsp;Hal also laid an important foundation for the reusable proof-of-work that Satoshi would use in the development of Bitcoin.</p>
<p>Being one of the best cryptographers in the world, Hal realized that Bitcoin was a huge breakthrough immediately after he stumbled upon it.</p>
<p>Back in&nbsp; it,&nbsp;<code>2008 году</code>&nbsp;he called Bitcoin&nbsp;&nbsp;<strong><em>«a very promising idea</em></strong>&nbsp;. »</p>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/e90c1948ecdd67427ca6fd6eb0fe7b24.jpg" alt="Speed ​​up secp256k1 with endomorphism"></figure>
<blockquote class="wp-block-quote"><p>This&nbsp;&nbsp;<em>tweet</em>&nbsp;, posted by&nbsp;&nbsp;<code>11 января 2009 года</code>, is proof enough that Hal&nbsp;&nbsp;<em><u>predicted the success of Bitcoin</u></em>&nbsp;&nbsp;before many even knew what it was.</p></blockquote>
<p>Two years have passed and&nbsp;&nbsp;<code>2011 году</code>&nbsp;Hal Finney as a developer and Bitcoin enthusiast wrote on the&nbsp;&nbsp;<a href="https://bitcointalk.org/index.php?topic=3238.msg45565#msg45565" target="_blank" rel="noreferrer noopener"><strong>Bitcointalk</strong></a>&nbsp;forum that&nbsp;&nbsp;<em><u>the secp256k1 endomorphism function can be used to speed up ECDSA signature verification</u></em></p>
<h2>LAMBDA and BETA are the values ​​on the secp256k1 curve, where:</h2>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/9a4ce63afa2c39ded280bea637d2ba70.svg" alt="λ^3 (mod n) = 1  "></figure>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/df44d75ceb126764e40606ad336f26e3.svg" alt="β^3(modp)=1"></figure>
<h3>secp256k1 uses the following prime number for its x and y coordinates:</h3>
<pre class="wp-block-code"><code>p = 0xffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffc2f</code></pre>
<h3>and the order of the curve:</h3>
<pre class="wp-block-code"><code>n = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141</code></pre>
<p>The first step is to calculate the values ​​of&nbsp;&nbsp;<code>LAMBDA</code>&nbsp;and&nbsp;&nbsp;<code>BETA</code>, such that for any point on the curve&nbsp;&nbsp;<code>Q = (x, y)</code>:</p>
<pre class="wp-block-code"><code>LAMBDA * Q = (BETA*х mod р, у)</code></pre>
<blockquote class="wp-block-quote"><p>This is the so-called effectively computable&nbsp;&nbsp;<em><u>endomorphism</u></em>&nbsp;, and it means that you can multiply any point on the curve&nbsp;&nbsp;<code>secp256k1</code>&nbsp;by this special value&nbsp; very quickly by&nbsp;<code>LAMBDA</code>doing a single multiplication&nbsp;&nbsp;<code>mod p</code>.</p></blockquote>
<h2>The meaning found and published by Hal Finney:</h2>
<pre class="wp-block-code"><code>LAMBDA = 0x5363ad4cc05c30e0a5261c028812645a122e22ea20816678df02967c1b23bd72

BETA = 0x7ae96a2b657c07106e64479eac3434e99cf0497512f58995c1396c28719501ee</code></pre>
<p>Given that we can quickly multiply, the&nbsp;&nbsp;<code>LAMBDA,</code>&nbsp;trick is to calculate&nbsp;&nbsp;<code>kQ</code><em>.&nbsp;</em>Let’s use the calculation first&nbsp;.&nbsp;Then&nbsp;&nbsp;&nbsp;you need to break it into two parts&nbsp;&nbsp;&nbsp;and&nbsp;&nbsp;, each about half the width of&nbsp;&nbsp;, so that:<em>&nbsp;</em><code>Q' = lambdaQ</code><code>k</code><code>k1</code><code>k2</code><code>n</code></p>
<pre class="wp-block-code"><code>k = k1 + k2*LAMBDA  mod  n</code></pre>
<p>then</p>
<pre class="wp-block-code"><code>k*Q = (k1 + k2*LAMBDA)*Q = k1*Q + k2*LAMBDA*Q = k1*Q + k2*Q'</code></pre>
<p>This last expression can be computed efficiently using the double multiplication algorithm, and since&nbsp;&nbsp;<code>k1</code>&nbsp;and&nbsp;&nbsp;<code>k2</code>&nbsp;are half the length, we get a speedup.</p>
<p>The missing part splits&nbsp;&nbsp;<code>k</code>&nbsp;into&nbsp;&nbsp;<code>k1</code>&nbsp;and&nbsp;&nbsp;<code>k2</code>.&nbsp;The following&nbsp;&nbsp;<em><u>4 values</u></em>&nbsp;​​are used for this :</p>
<pre class="wp-block-code"><code>а1 = 0x3086d221a7d46bcde86c90e49284eb15
b1 = -0xe4437ed6010e88286f547fa90abfe4c3
а2 = 0x114ca50f7a8e2f3f657c1108d9d44cfd8
b2 = 0x3086d221a7d46bcde86c90e49284eb15</code></pre>
<p><em>(it’s ok that a1 = b2)</em></p>
<h4>We use them as follows to divide k:</h4>
<pre class="wp-block-code"><code>c1 = RoundToNearestInteger(b2*k/n)
c2 = RoundToNearestInteger(-b1*k/n)

k1 = k - c1*a1 - c2*a2
k2 = -c1*b1 - c2*b2</code></pre>
<blockquote class="wp-block-quote"><p>We end up with roughly&nbsp;&nbsp;<code>20%-е</code>&nbsp;a speedup due to the halving of the number of doublings.<br>
This gives many algorithms that can be grouped on multiple points the performance they would have with twice the number of public keys.<br>
<em>This speedup at an equivalent level of optimization makes it&nbsp;&nbsp;</em><code>secp256k1</code><em>&nbsp;the fastest curve to test out of all the commonly used curves.</em></p></blockquote>
<h3>We learned about the existence of endomorphism in a more detailed study of the repository from the developer and researcher Jean Luc Pons</h3>
<div class="wp-block-image">
<figure class="aligncenter"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/53aa4146a4d43ac9279e96b8e403216d.png" alt="Speed ​​up secp256k1 with endomorphism"></figure>
</div>
<p>We previously published an article:&nbsp;&nbsp;<a href="https://cryptodeep.ru/kangaroo/" target="_blank" rel="noreferrer noopener"><strong><em>«Pollard’s Kangaroo find solutions to the discrete logarithm of secp256k1 PRIVATE KEY + NONCES in a known range»</em></strong></a><strong><em>&nbsp;&nbsp;,&nbsp;</em></strong>&nbsp;where we used the source code to build&nbsp;&nbsp;<a href="https://cryptodeep.ru/kangaroo/" target="_blank" rel="noreferrer noopener">Kangaroo</a>&nbsp;&nbsp;by&nbsp;&nbsp;<a href="https://cryptodeep.ru/kangaroo/" target="_blank" rel="noreferrer noopener">Jean Luc Pons</a>&nbsp;.</p>
<h2>Based on accelerated mechanism Jean Luc Pons pointed VanitySearch</h2>
<p>Open&nbsp;&nbsp;<a href="https://github.com/JeanLucPons/VanitySearch/blob/c8d48ce5f03f5357c0e87cbdb3e1e93cd50af88b/main.cpp#L255" target="_blank" rel="noreferrer noopener"><strong>main.cpp</strong></a></p>
<figure class="wp-block-image"><img title="main.cpp" src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/605fca301a5eef1f215250562ff4e039.png" alt="main.cpp"><figcaption>main.cpp</figcaption></figure>
<p>In lines&nbsp;&nbsp;<a href="https://github.com/JeanLucPons/VanitySearch/blob/c8d48ce5f03f5357c0e87cbdb3e1e93cd50af88b/main.cpp#L255" target="_blank" rel="noreferrer noopener">255</a>&nbsp;&nbsp;and&nbsp;&nbsp;<a href="https://github.com/JeanLucPons/VanitySearch/blob/c8d48ce5f03f5357c0e87cbdb3e1e93cd50af88b/main.cpp#L256" target="_blank" rel="noreferrer noopener">256</a>&nbsp;&nbsp;we see that Jean Luc Pons applied the elliptic curve acceleration function&nbsp;&nbsp;<code>secp256k1</code>&nbsp;using&nbsp;&nbsp;<em><u>endomorphism</u></em>&nbsp;.</p>
<pre class="wp-block-code"><code>  lambda.SetBase16("5363ad4cc05c30e0a5261c028812645a122e22ea20816678df02967c1b23bd72");
  lambda2.SetBase16("ac9c52b33fa3cf1f5ad9e3fd77ed9ba4a880b9fc8ec739c2e0cfc810b51283ce");</code></pre>
<h2>Let’s move on to the experimental part:</h2>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/7df255c08ea1fb0e498b76bf4a431873.png" alt="Speed ​​up secp256k1 with endomorphism"></figure>
<blockquote class="wp-block-quote"><p>As we remember from the&nbsp;&nbsp;<a href="https://cryptodeep.ru/kangaroo/" target="_blank" rel="noreferrer noopener">article,</a>&nbsp;&nbsp;we analyzed transactions of Bitcoin Address&nbsp;&nbsp;<a href="https://www.blockchain.com/ru/btc/address/14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE" target="_blank" rel="noreferrer noopener"><strong>14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE</strong></a><br>
from the&nbsp;&nbsp;<a href="https://bitinfocharts.com/top-100-richest-bitcoin-addresses.html" target="_blank" rel="noreferrer noopener"><strong>Bitcoin Rich List</strong></a>&nbsp;&nbsp;for a total of more than&nbsp;&nbsp;<a href="https://bitinfocharts.com/top-100-richest-bitcoin-addresses.html" target="_blank" rel="noreferrer noopener"><strong>10 million US dollars</strong></a>&nbsp;, take this Bitcoin Address as an example</p></blockquote>
<p>Open Google Colab&nbsp;&nbsp;<a href="https://github.com/demining/TerminalGoogleColab" target="_blank" rel="noreferrer noopener"><strong>[TerminalGoogleColab]</strong></a>&nbsp;in the terminal &nbsp;and use the repository&nbsp;&nbsp;<a href="https://github.com/demining/CryptoDeepTools/tree/main/07EndomorphismSecp256k1" target="_blank" rel="noreferrer noopener">«07EndomorphismSecp256k1»</a></p>
<pre class="wp-block-code"><code>git clone https://github.com/demining/CryptoDeepTools.git

cd CryptoDeepTools/07EndomorphismSecp256k1/

pip3 install base58</code></pre>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/92866f34b1dcfbce80b23fd56a913744.png" alt="Speed ​​up secp256k1 with endomorphism"></figure>
<p>Open code&nbsp;&nbsp;<a href="https://github.com/demining/CryptoDeepTools/blob/9dfd594126117e07fc51a77a7c613180eb662f18/07EndomorphismSecp256k1/endomorphism.py#L145" target="_blank" rel="noreferrer noopener">endomorphism.py&nbsp;</a>&nbsp;<em>on line&nbsp;</em>&nbsp;<a href="https://github.com/demining/CryptoDeepTools/blob/9dfd594126117e07fc51a77a7c613180eb662f18/07EndomorphismSecp256k1/endomorphism.py#L145" target="_blank" rel="noreferrer noopener">145</a>&nbsp;&nbsp;we use all short values ​​to speed up&nbsp;&nbsp;<code>secp256k1</code>&nbsp;with&nbsp;&nbsp;<em>endomorphism</em></p>
<pre class="wp-block-code"><code><strong>def</strong> <strong>split_scalar_endo</strong>(k):
    n = N
    a1 = 0x3086d221a7d46bcde86c90e49284eb15
    b1 = -0xe4437ed6010e88286f547fa90abfe4c3
    a2 = 0x114ca50f7a8e2f3f657c1108d9d44cfd8
    b2 = a1
    c1 = div_nearest(b2 * k, n)
    c2 = div_nearest(-b1 * k, n)
    k1 = mod(k - c1 * a1 - c2 * a2, n)
    k2 = mod(-c1 * b1 - c2 * b2, n)
    k1neg = k1 &gt; POW_2_128
    k2neg = k2 &gt; POW_2_128
    <strong>if</strong> k1neg:
        k1 = n - k1
    <strong>if</strong> k2neg:
        k2 = n - k2
    <strong>return</strong> (k1neg, k1, k2neg, k2)</code></pre>
<p>Copy the private key in the&nbsp;&nbsp;<code>HEX</code>-format that we published in the&nbsp;&nbsp;<a href="https://cryptodeep.ru/kangaroo/" target="_blank" rel="noreferrer noopener">article</a></p>
<pre class="wp-block-code"><code>HEX:  23d4a09295be678b21a5f1dceae1f634a69c1b41775f680ebf8165266471401b</code></pre>
<h4>Let’s run the Python script endomorphism.py specifying the private key:</h4>
<pre class="wp-block-code"><code>python3 endomorphism.py 23d4a09295be678b21a5f1dceae1f634a69c1b41775f680ebf8165266471401b &gt; pubkey.txt
</code></pre>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/3c56f13d77ef80024a8cfb16f80943fc.png" alt="Speed ​​up secp256k1 with endomorphism"></figure>
<h4>The result of the public key will be saved to the file: pubkey.txt</h4>
<pre class="wp-block-code"><code>Откроем файл: pubkey.txt и проверим:

cat pubkey.txt

04ca5606a1e820e7a2f6bb3ab090e8ade7b04a7e0b5909a68dda2744ae3b8ecbfa280a47639c811134d648e8ee8096c33b41611be509ebca837fbda10baaa1eb15
</code></pre>
<figure class="wp-block-image"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/4485295113ba74f334a01f4ed2b54bd4.png" alt="Speed ​​up secp256k1 with endomorphism"></figure>
<h4>Next, get the Bitcoin Address by running the Python script pubtoaddr.py</h4>
<pre class="wp-block-code"><code>python3 pubtoaddr.py

Откроем файл: BitcoinAddress.txt и проверим:

cat BitcoinAddress.txt

14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE
</code></pre>
<div class="wp-block-image">
<figure class="aligncenter"><img src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/1a480554216e020e1c53a9370661274a.png" alt="Speed ​​up secp256k1 with endomorphism"></figure>
</div>
<pre class="wp-block-code"><code>ADDR: 14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE
WIF:  5J64pq77XjeacCezwmAr2V1s7snvvJkuAz8sENxw7xCkikceV6e
HEX:  23d4a09295be678b21a5f1dceae1f634a69c1b41775f680ebf8165266471401b</code></pre>
<figure class="wp-block-image"><img title="Checking the private key on the bitaddress website" src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/d8c78d8eb14e5246b495e09f59631e44.png" alt="Checking the private key on the bitaddress website"><figcaption>Checking the private key on the bitaddress website</figcaption></figure>
<h3>blockchain:</h3>
<div class="wp-block-image">
<figure class="aligncenter"><img title="www.blockchain.com/btc/address/14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE" src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/ed97dac1dc07e2bce09fe0951d9f64de.png" alt="www.blockchain.com/btc/address/14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE"><figcaption>www.blockchain.com/btc/address/14NWDXkQwcGN1Pd9fboL8npVynD5SfyJAE</figcaption></figure>
</div>
<h2>On this topic, you can read the literature:</h2>
<ul>
<li><em>Gallant, Robert P., Robert J. Lambert, and Scott A. Wanston.&nbsp;</em><strong><em>«Faster point multiplication on elliptic curves with efficient endomorphisms»</em></strong><em>&nbsp;.&nbsp;Annual International Conference on Cryptology, pp. 190–200.&nbsp;Springer, Berlin, Heidelberg, (2001)</em></li>
<li><em>Hankerson, Darrell, Alfred J. Menezes, and Scott Wanston.&nbsp;</em><strong><em>«A Guide to Elliptic Curve Cryptography»</em></strong><em>&nbsp;.&nbsp;Computer Reviews 46, no.&nbsp;1 (2005)</em></li>
<li><em>Hal Finney.&nbsp;bitcointalk —&nbsp;&nbsp;</em><strong><em>«Acceleration of signature verification»</em></strong><em>&nbsp;.&nbsp;(2011)&nbsp;</em>&nbsp;<a href="https://bitcointalk.org/index.php?topic=3238.0" target="_blank" rel="noreferrer noopener">https://bitcointalk.org/index.php?topic=3238.0</a></li>
<li><em>Blahut, Richard E.&nbsp;&nbsp;</em><strong><em>«Cryptography and Secure Communication»</em></strong><em>&nbsp;.&nbsp;Cambridge University Press, (2014)</em></li>
</ul>
<p>This video was created for the&nbsp;&nbsp;<a href="https://cryptodeep.ru/" target="_blank" rel="noreferrer noopener"><strong>CRYPTO DEEP TECH</strong></a>&nbsp;portal &nbsp;to ensure the financial security of data and cryptography on elliptic curves&nbsp;&nbsp;<code>secp256k1</code>&nbsp;against weak signatures&nbsp;&nbsp;<code>ECDSA</code>&nbsp;in cryptocurrency&nbsp;<code>BITCOIN</code></p>
<p><a href="https://github.com/demining/CryptoDeepTools/tree/main/07EndomorphismSecp256k1" target="_blank" rel="noreferrer noopener"><strong><u>Source</u></strong></a></p>
<p><a href="https://t.me/cryptodeeptech" target="_blank" rel="noreferrer noopener"><strong>Telegram</strong></a><strong>&nbsp;:&nbsp;&nbsp;</strong><a href="https://t.me/cryptodeeptech" target="_blank" rel="noreferrer noopener"><strong><u>https://t.me/cryptodeeptech</u></strong></a></p>
<p><a href="https://youtu.be/DH6FyNY-Gh0" target="_blank" rel="noreferrer noopener"><strong>Video</strong></a><strong>&nbsp;:&nbsp;&nbsp;<u><a href="https://youtu.be/DH6FyNY-Gh0" target="_blank" rel="noreferrer noopener">https://youtu.be/DH6FyNY-Gh0</a></u></strong></p>
<p><a href="https://cryptodeeptech.ru/endomorphism"><strong>Source : https://cryptodeeptech.ru/endomorphism</strong></a></p>
</div>


---


|  | Donation Address |
| --- | --- |
| ♥ __BTC__ | 1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v |
| ♥ __ETH__ | 0xaBd66CF90898517573f19184b3297d651f7b90bf |
