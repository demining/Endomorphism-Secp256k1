<!DOCTYPE html>
<!-- saved from url=(0039)https://cryptodeeptech.ru/endomorphism/ -->
<html lang="ru-RU"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
	
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="profile" href="https://gmpg.org/xfn/11">

	<meta name="robots" content="index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1">

	<!-- This site is optimized with the Yoast SEO plugin v19.2 - https://yoast.com/wordpress/plugins/seo/ -->
	<style type="text/css"></style><title>Speed ​​up secp256k1 with endomorphism - «CRYPTO DEEP TECH»</title>
	<meta name="description" content="The secp256k1 acceleration function using endomorphism which helps in optimizing ECDSA validation for the Bitcoin cryptocurrency. LAMBDA and BETA values">
	<link rel="canonical" href="https://cryptodeeptech.ru/endomorphism/">
	<meta property="og:locale" content="ru_RU">
	<meta property="og:type" content="article">
	<meta property="og:title" content="Speed ​​up secp256k1 with endomorphism - «CRYPTO DEEP TECH»">
	<meta property="og:description" content="The secp256k1 acceleration function using endomorphism which helps in optimizing ECDSA validation for the Bitcoin cryptocurrency. LAMBDA and BETA values">
	<meta property="og:url" content="https://cryptodeeptech.ru/endomorphism/">
	<meta property="og:site_name" content="«CRYPTO DEEP TECH»">
	<meta property="article:published_time" content="2022-08-05T07:44:37+00:00">
	<meta property="article:modified_time" content="2022-08-25T19:05:00+00:00">
	<meta property="og:image" content="https://habrastorage.org/r/w780/getpro/habr/upload_files/e90/c19/48e/e90c1948ecdd67427ca6fd6eb0fe7b24.jpg">
	<meta name="author" content="Crypto Deep Tech">
	<meta name="twitter:card" content="summary_large_image">
	<meta name="twitter:label1" content="Написано автором">
	<meta name="twitter:data1" content="Crypto Deep Tech">
	<meta name="twitter:label2" content="Примерное время для чтения">
	<meta name="twitter:data2" content="8 минут">
	<script async="" src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/tag.js"></script><script type="application/ld+json" class="yoast-schema-graph">{"@context":"https://schema.org","@graph":[{"@type":"WebSite","@id":"https://cryptodeeptech.ru/#website","url":"https://cryptodeeptech.ru/","name":"«CRYPTO DEEP TECH»","description":"Cryptanalysis and data financial security services","potentialAction":[{"@type":"SearchAction","target":{"@type":"EntryPoint","urlTemplate":"https://cryptodeeptech.ru/?s={search_term_string}"},"query-input":"required name=search_term_string"}],"inLanguage":"ru-RU"},{"@type":"ImageObject","inLanguage":"ru-RU","@id":"https://cryptodeeptech.ru/endomorphism/#primaryimage","url":"https://habrastorage.org/r/w780/getpro/habr/upload_files/e90/c19/48e/e90c1948ecdd67427ca6fd6eb0fe7b24.jpg","contentUrl":"https://habrastorage.org/r/w780/getpro/habr/upload_files/e90/c19/48e/e90c1948ecdd67427ca6fd6eb0fe7b24.jpg"},{"@type":"WebPage","@id":"https://cryptodeeptech.ru/endomorphism/#webpage","url":"https://cryptodeeptech.ru/endomorphism/","name":"Speed ​​up secp256k1 with endomorphism - «CRYPTO DEEP TECH»","isPartOf":{"@id":"https://cryptodeeptech.ru/#website"},"primaryImageOfPage":{"@id":"https://cryptodeeptech.ru/endomorphism/#primaryimage"},"datePublished":"2022-08-05T07:44:37+00:00","dateModified":"2022-08-25T19:05:00+00:00","author":{"@id":"https://cryptodeeptech.ru/#/schema/person/0ef8ac0f63991970628a3a6587f9e6c0"},"description":"The secp256k1 acceleration function using endomorphism which helps in optimizing ECDSA validation for the Bitcoin cryptocurrency. LAMBDA and BETA values","breadcrumb":{"@id":"https://cryptodeeptech.ru/endomorphism/#breadcrumb"},"inLanguage":"ru-RU","potentialAction":[{"@type":"ReadAction","target":["https://cryptodeeptech.ru/endomorphism/"]}]},{"@type":"BreadcrumbList","@id":"https://cryptodeeptech.ru/endomorphism/#breadcrumb","itemListElement":[{"@type":"ListItem","position":1,"name":"Главная страница","item":"https://cryptodeeptech.ru/"},{"@type":"ListItem","position":2,"name":"Speed ​​up secp256k1 with endomorphism"}]},{"@type":"Person","@id":"https://cryptodeeptech.ru/#/schema/person/0ef8ac0f63991970628a3a6587f9e6c0","name":"Crypto Deep Tech","sameAs":["https://cryptodeeptech.ru","https://www.youtube.com/channel/UCd8W6qtRSiBn0Q0wy6HuNkQ/"],"url":"https://cryptodeeptech.ru/author/cryptodeeptech/"}]}</script>
	<!-- / Yoast SEO plugin. -->


<link rel="dns-prefetch" href="https://fonts.googleapis.com/">
<link rel="alternate" type="application/rss+xml" title="«CRYPTO DEEP TECH» » Лента" href="https://cryptodeeptech.ru/feed/">
<link rel="alternate" type="application/rss+xml" title="«CRYPTO DEEP TECH» » Лента комментариев" href="https://cryptodeeptech.ru/comments/feed/">
<link rel="stylesheet" id="itng-block-style-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_8f426a1779caff96bb3f2afbcff86bc9.css" media="all">
<link rel="stylesheet" id="wp-block-library-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/style.min.css" media="all">
<style id="global-styles-inline-css">
body{--wp--preset--color--black: #000000;--wp--preset--color--cyan-bluish-gray: #abb8c3;--wp--preset--color--white: #ffffff;--wp--preset--color--pale-pink: #f78da7;--wp--preset--color--vivid-red: #cf2e2e;--wp--preset--color--luminous-vivid-orange: #ff6900;--wp--preset--color--luminous-vivid-amber: #fcb900;--wp--preset--color--light-green-cyan: #7bdcb5;--wp--preset--color--vivid-green-cyan: #00d084;--wp--preset--color--pale-cyan-blue: #8ed1fc;--wp--preset--color--vivid-cyan-blue: #0693e3;--wp--preset--color--vivid-purple: #9b51e0;--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple: linear-gradient(135deg,rgba(6,147,227,1) 0%,rgb(155,81,224) 100%);--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan: linear-gradient(135deg,rgb(122,220,180) 0%,rgb(0,208,130) 100%);--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange: linear-gradient(135deg,rgba(252,185,0,1) 0%,rgba(255,105,0,1) 100%);--wp--preset--gradient--luminous-vivid-orange-to-vivid-red: linear-gradient(135deg,rgba(255,105,0,1) 0%,rgb(207,46,46) 100%);--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray: linear-gradient(135deg,rgb(238,238,238) 0%,rgb(169,184,195) 100%);--wp--preset--gradient--cool-to-warm-spectrum: linear-gradient(135deg,rgb(74,234,220) 0%,rgb(151,120,209) 20%,rgb(207,42,186) 40%,rgb(238,44,130) 60%,rgb(251,105,98) 80%,rgb(254,248,76) 100%);--wp--preset--gradient--blush-light-purple: linear-gradient(135deg,rgb(255,206,236) 0%,rgb(152,150,240) 100%);--wp--preset--gradient--blush-bordeaux: linear-gradient(135deg,rgb(254,205,165) 0%,rgb(254,45,45) 50%,rgb(107,0,62) 100%);--wp--preset--gradient--luminous-dusk: linear-gradient(135deg,rgb(255,203,112) 0%,rgb(199,81,192) 50%,rgb(65,88,208) 100%);--wp--preset--gradient--pale-ocean: linear-gradient(135deg,rgb(255,245,203) 0%,rgb(182,227,212) 50%,rgb(51,167,181) 100%);--wp--preset--gradient--electric-grass: linear-gradient(135deg,rgb(202,248,128) 0%,rgb(113,206,126) 100%);--wp--preset--gradient--midnight: linear-gradient(135deg,rgb(2,3,129) 0%,rgb(40,116,252) 100%);--wp--preset--duotone--dark-grayscale: url('#wp-duotone-dark-grayscale');--wp--preset--duotone--grayscale: url('#wp-duotone-grayscale');--wp--preset--duotone--purple-yellow: url('#wp-duotone-purple-yellow');--wp--preset--duotone--blue-red: url('#wp-duotone-blue-red');--wp--preset--duotone--midnight: url('#wp-duotone-midnight');--wp--preset--duotone--magenta-yellow: url('#wp-duotone-magenta-yellow');--wp--preset--duotone--purple-green: url('#wp-duotone-purple-green');--wp--preset--duotone--blue-orange: url('#wp-duotone-blue-orange');--wp--preset--font-size--small: 13px;--wp--preset--font-size--medium: 20px;--wp--preset--font-size--large: 36px;--wp--preset--font-size--x-large: 42px;}.has-black-color{color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-color{color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-color{color: var(--wp--preset--color--white) !important;}.has-pale-pink-color{color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-color{color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-color{color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-color{color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-color{color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-color{color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-color{color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-color{color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-color{color: var(--wp--preset--color--vivid-purple) !important;}.has-black-background-color{background-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-background-color{background-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-background-color{background-color: var(--wp--preset--color--white) !important;}.has-pale-pink-background-color{background-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-background-color{background-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-background-color{background-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-background-color{background-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-background-color{background-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-background-color{background-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-background-color{background-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-background-color{background-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-background-color{background-color: var(--wp--preset--color--vivid-purple) !important;}.has-black-border-color{border-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-border-color{border-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-border-color{border-color: var(--wp--preset--color--white) !important;}.has-pale-pink-border-color{border-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-border-color{border-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-border-color{border-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-border-color{border-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-border-color{border-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-border-color{border-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-border-color{border-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-border-color{border-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-border-color{border-color: var(--wp--preset--color--vivid-purple) !important;}.has-vivid-cyan-blue-to-vivid-purple-gradient-background{background: var(--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple) !important;}.has-light-green-cyan-to-vivid-green-cyan-gradient-background{background: var(--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan) !important;}.has-luminous-vivid-amber-to-luminous-vivid-orange-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange) !important;}.has-luminous-vivid-orange-to-vivid-red-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-orange-to-vivid-red) !important;}.has-very-light-gray-to-cyan-bluish-gray-gradient-background{background: var(--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray) !important;}.has-cool-to-warm-spectrum-gradient-background{background: var(--wp--preset--gradient--cool-to-warm-spectrum) !important;}.has-blush-light-purple-gradient-background{background: var(--wp--preset--gradient--blush-light-purple) !important;}.has-blush-bordeaux-gradient-background{background: var(--wp--preset--gradient--blush-bordeaux) !important;}.has-luminous-dusk-gradient-background{background: var(--wp--preset--gradient--luminous-dusk) !important;}.has-pale-ocean-gradient-background{background: var(--wp--preset--gradient--pale-ocean) !important;}.has-electric-grass-gradient-background{background: var(--wp--preset--gradient--electric-grass) !important;}.has-midnight-gradient-background{background: var(--wp--preset--gradient--midnight) !important;}.has-small-font-size{font-size: var(--wp--preset--font-size--small) !important;}.has-medium-font-size{font-size: var(--wp--preset--font-size--medium) !important;}.has-large-font-size{font-size: var(--wp--preset--font-size--large) !important;}.has-x-large-font-size{font-size: var(--wp--preset--font-size--x-large) !important;}
</style>
<link rel="stylesheet" id="wp-date-remover-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_e6094661d8923e95b233019ebff7c8f0.css" media="all">
<link rel="stylesheet" id="itng-fonts-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/css" media="all">
<link rel="stylesheet" id="itng-style-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_8de4505c66a21eefd3c1c98b6400e4e1.css" media="all">
<link rel="stylesheet" id="itng-main-style-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_d1cf6f49400112d539e59eee9b75e10d.css" media="all">
<style id="itng-main-style-inline-css">
.custom-logo-link img {width: 400px;}@media screen and (min-width: 992px) {#header-image .header-overlay {
            opacity: 0.01;
        }}
ins,
	.nav-wrapper,
	#menu,
	.main-navigation ul#menu-desktop ul,
	#itng-featured-news .slider-post-wrapper .posted-on a,
	#itng-featured-news #itng-featured-news-list-container .posted-on a,
	#itng-featured-posts .itng-featured-post-date,
	#itng-featured-news #itng-featured-news-carousel-container .posted-on a,
	#colophon,
	[class^=itng-search] form,
	#itng-featured-cat .featured-cat-thumb h2,
	#itng-featured-cat .featured-cat-thumb h3
	{background-color: #008bca}article .entry-meta a,
	article .blog-footer,
	article .blog-footer a,
	.widget a,
	.nav-links a,
	.itng-pagination .nav-links > a,
	.itng-pagination .dots
	{color: #008bca !important}blockquote,
	#itng-content-title span
	{border-color: #008bca}button.top-menu-mobile
	{background-color: #43bdf2 !important}#footer-sidebar .widget-title
	{color: #43bdf2 !important}
</style>
<link rel="stylesheet" id="bootstrap-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_d26191bd0380b0cf97525a613b8b566c.css" media="all">
<link rel="stylesheet" id="owl-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_c8322bd5bffc8e2856f2cbcd03c61d18.css" media="all">
<link rel="stylesheet" id="mag-popup-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_30b593b71d7672658f89bfea0ab360c9.css" media="all">
<link rel="stylesheet" id="font-awesome-css" href="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_c495654869785bc3df60216616814ad1.css" media="all">
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/jquery.min.js" id="jquery-core-js"></script>
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/jquery-migrate.min.js" id="jquery-migrate-js"></script>
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_49cea0a781874a962879c2caca9bc322.js" id="wp-date-remover-js"></script>
<link rel="https://api.w.org/" href="https://cryptodeeptech.ru/wp-json/"><link rel="alternate" type="application/json" href="https://cryptodeeptech.ru/wp-json/wp/v2/posts/337"><meta name="generator" content="WordPress 6.0.1">
<link rel="alternate" type="application/json+oembed" href="https://cryptodeeptech.ru/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fcryptodeeptech.ru%2Fendomorphism%2F">
<link rel="alternate" type="text/xml+oembed" href="https://cryptodeeptech.ru/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fcryptodeeptech.ru%2Fendomorphism%2F&amp;format=xml">
		<style type="text/css">
						#header-image {
						background-image: url(https://cryptodeeptech.ru/wp-content/uploads/2022/07/header3.jpg);
						background-size: cover;
						background-repeat: repeat;
						background-position: center center;
				}
							.site-title, .site-description {
				display: none;
				position: absolute;
				clip: rect(1px, 1px, 1px, 1px);
				}
					</style>
		<style id="custom-background-css">
body.custom-background { background-color: #eff3fd; }
</style>
	<link rel="icon" href="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-32x32.png" sizes="32x32">
<link rel="icon" href="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-192x192.png" sizes="192x192">
<link rel="apple-touch-icon" href="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-180x180.png">
<meta name="msapplication-TileImage" content="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-270x270.png">
</head>

<body data-rsssl="1" class="post-template-default single single-post postid-337 single-format-standard custom-background wp-custom-logo no-sidebar">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-dark-grayscale"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 0.49803921568627"></fefuncr><fefuncg type="table" tableValues="0 0.49803921568627"></fefuncg><fefuncb type="table" tableValues="0 0.49803921568627"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-grayscale"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 1"></fefuncr><fefuncg type="table" tableValues="0 1"></fefuncg><fefuncb type="table" tableValues="0 1"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-purple-yellow"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.54901960784314 0.98823529411765"></fefuncr><fefuncg type="table" tableValues="0 1"></fefuncg><fefuncb type="table" tableValues="0.71764705882353 0.25490196078431"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-blue-red"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 1"></fefuncr><fefuncg type="table" tableValues="0 0.27843137254902"></fefuncg><fefuncb type="table" tableValues="0.5921568627451 0.27843137254902"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-midnight"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 0"></fefuncr><fefuncg type="table" tableValues="0 0.64705882352941"></fefuncg><fefuncb type="table" tableValues="0 1"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-magenta-yellow"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.78039215686275 1"></fefuncr><fefuncg type="table" tableValues="0 0.94901960784314"></fefuncg><fefuncb type="table" tableValues="0.35294117647059 0.47058823529412"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-purple-green"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.65098039215686 0.40392156862745"></fefuncr><fefuncg type="table" tableValues="0 1"></fefuncg><fefuncb type="table" tableValues="0.44705882352941 0.4"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-blue-orange"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.098039215686275 1"></fefuncr><fefuncg type="table" tableValues="0 0.66274509803922"></fefuncg><fefuncb type="table" tableValues="0.84705882352941 0.41960784313725"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><div id="page" class="site">
	<a class="skip-link screen-reader-text" href="https://cryptodeeptech.ru/endomorphism/#primary">Skip to content</a>

	
	    <header id="masthead" class="site-header style-1">

		    
	        <div id="header-image">
		        <div class="site-branding">
					<a href="https://cryptodeeptech.ru/" class="custom-logo-link" rel="home"><img width="1279" height="319" src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/cropped-header4.png" class="custom-logo" alt="«CRYPTO DEEP TECH»" srcset="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4.png 1279w, https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4-300x75.png 300w, https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4-1024x255.png 1024w, https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4-768x192.png 768w" sizes="(max-width: 1279px) 100vw, 1279px" title="Speed ​​up secp256k1 with endomorphism"></a>	<h2 class="site-title"><a href="https://cryptodeeptech.ru/" rel="home">«CRYPTO DEEP TECH»</a></h2>
		<p class="site-description">Cryptanalysis and data financial security services</p>
	        	</div>
				<div class="header-overlay"></div>
	        </div>

			<div class="nav-wrapper">
				 <div class="container">
					 <div class="d-flex">

						<div id="site-navigation" class="main-navigation col-lg-11" role="navigation">
							<ul id="menu-desktop" class="menu"><li id="menu-item-229" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-home menu-item-229"><a href="https://cryptodeeptech.ru/">HOME</a></li>
<li id="menu-item-225" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-225"><a href="https://cryptodeeptech.ru/publication/">PUBLICATIONS</a></li>
<li id="menu-item-226" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-226"><a href="https://cryptodeeptech.ru/study/">STUDY</a></li>
<li id="menu-item-227" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-227"><a href="https://cryptodeeptech.ru/resources/">RESOURCES</a></li>
<li id="menu-item-228" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-228"><a href="https://cryptodeeptech.ru/contacts/">CONTACTS</a></li>
<li id="menu-item-240" class="menu-item menu-item-type-post_type menu-item-object-post menu-item-240"><a href="https://cryptodeeptech.ru/lattice-attack/">BLOG</a></li>
</ul>						</div>

						<button href="#menu" class="menu-link mobile-nav-btn col-auto"><i class="fa fa-bars" aria-hidden="true"></i></button>

						<div id="search-wrapper" class="ml-auto col-auto d-flex">
							<button type="button" id="go-to-field" tabindex="-1"></button>
					    	<button class="search-btn-main"><i class="fa fa-search"></i></button>
					    	
<div class="itng-search-main">
	<form role="search" method="get" class="search-form" action="https://cryptodeeptech.ru/">
				<label>
					<span class="screen-reader-text">Найти:</span>
					<input type="search" class="search-field" placeholder="Поиск…" value="" name="s">
				</label>
				<input type="submit" class="search-submit" value="Поиск">
			</form>	<button type="button" id="go-to-btn" tabindex="-1"></button>
</div>
						</div>
					</div>
				</div>
			</div>

		</header><!-- #masthead -->
			<div id="content-wrapper" class="container row">
		
	<main id="primary" class="site-main container order-1">

		
<article id="post-337" class="post-337 post type-post status-publish format-standard hentry category-1">
	
	<header class="entry-header">
		<h1 class="entry-title">Speed ​​up secp256k1 with endomorphism</h1>	</header><!-- .entry-header -->
	
	
	
			<div class="entry-meta">
			<span class="posted-on" style="display: none;"><a href="https://cryptodeeptech.ru/endomorphism/" rel="bookmark"><time class="entry-date published" datetime="" style="display: none;"></time><time class="updated" datetime=""></time></a></span><span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>		</div><!-- .entry-meta -->
		
	
	<div class="entry-content">
		<div class="entry-meta"></div>
<div class="entry-content">
<p class="has-text-align-center"><iframe title="Youtube video player" src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/DH6FyNY-Gh0.html" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe></p>
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
<footer class="entry-footer">
<div class="cat-links"></div>
</footer>
	</div><!-- .entry-content -->

	<footer class="entry-footer">
		<div class="cat-links"><i class="fa fa-folder-open" aria-hidden="true"></i> <a href="https://cryptodeeptech.ru/category/%d0%b1%d0%b5%d0%b7-%d1%80%d1%83%d0%b1%d1%80%d0%b8%d0%ba%d0%b8/" rel="category tag">Без рубрики</a></div>	</footer><!-- .entry-footer -->
</article><!-- #post-337 -->

	<nav class="navigation post-navigation" aria-label="Записи">
		<h2 class="screen-reader-text">Навигация по записям</h2>
		<div class="nav-links"><div class="nav-previous"><a href="https://cryptodeeptech.ru/kangaroo/" rel="prev">Pollard’s Kangaroo find solutions to the discrete logarithm secp256k1 PRIVATE KEY + NONCES in a known range</a></div><div class="nav-next"><a href="https://cryptodeeptech.ru/reduce-private-key/" rel="next">Reducing the private key through scalar multiplication using the ECPy + Google Colab library</a></div></div>
	</nav>		<div id="itng_related_posts_wrapper">
			<h3 id="itng_related_posts_title">Related Posts</h3>
			<div class="itng-related-posts row">
				<article id="post-270" class="itng-blog col-md-6 col-lg-4 post-270 post type-post status-publish format-standard hentry category-1">
		<div class="itng-card-wrapper">
			<div class="itng-thumb">
							</div>
			
			<div class="itng-card-content">
				<div class="entry-meta">
					<a href="https://cryptodeeptech.ru/algorithms-for-secp256k/"></a>
					<span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>				</div><!-- .entry-meta -->
				
				<header class="entry-header">
					<h2 class="entry-title"><a href="https://cryptodeeptech.ru/algorithms-for-secp256k/">Useful and efficient algorithms for secp256k1 elliptic curve</a></h2>				</header><!-- .entry-header -->
				
				<div class="itng_excerpt">
					In this article, we will consider several useful and efficient algorithms for an elliptic curve&nbsp;&nbsp;E&nbsp;&nbsp;over a field&nbsp;&nbsp;GF(p)&nbsp;&nbsp;given by the short Weierstrass equation у^2&nbsp;= х^3&nbsp;+ Ах + В &nbsp;Algorithm for generating a point on curve&nbsp;&nbsp;E &nbsp;Algorithm for adding points &nbsp;Doubling Point Algorithm &nbsp;Algorithm for finding an integer multiple point &nbsp;Algorithm for finding an integer multiple point (scalar multiplication)…				</div>
				
				<div class="blog-footer">
					<div class="itng_cats">
						<a href="https://cryptodeeptech.ru/category/%d0%b1%d0%b5%d0%b7-%d1%80%d1%83%d0%b1%d1%80%d0%b8%d0%ba%d0%b8/" rel="category tag">Без рубрики</a>					</div>
					<div class="blog-comments">
						0					</div>
				</div>
			</div>
		</div>
</article><!-- #post-270 --><article id="post-71" class="itng-blog col-md-6 col-lg-4 post-71 post type-post status-publish format-standard hentry category-1">
		<div class="itng-card-wrapper">
			<div class="itng-thumb">
							</div>
			
			<div class="itng-card-content">
				<div class="entry-meta">
					<a href="https://cryptodeeptech.ru/lattice-attack/"></a>
					<span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>				</div><!-- .entry-meta -->
				
				<header class="entry-header">
					<h2 class="entry-title"><a href="https://cryptodeeptech.ru/lattice-attack/">With the help of Lattice Attack, we received a Private Key to BITCOIN</a></h2>				</header><!-- .entry-header -->
				
				<div class="itng_excerpt">
					What do we know about the lattice attack? To begin with, the&nbsp;&nbsp;elliptic curve digital signature algorithm&nbsp;(ECDSA)&nbsp;&nbsp;is a common digital signature scheme that we see in many of our code reviews.&nbsp;It has some desirable properties, but can also be very fragile to recover the private key with a side-channel attack that reveals less than one bit of the…				</div>
				
				<div class="blog-footer">
					<div class="itng_cats">
						<a href="https://cryptodeeptech.ru/category/%d0%b1%d0%b5%d0%b7-%d1%80%d1%83%d0%b1%d1%80%d0%b8%d0%ba%d0%b8/" rel="category tag">Без рубрики</a>					</div>
					<div class="blog-comments">
						0					</div>
				</div>
			</div>
		</div>
</article><!-- #post-71 --><article id="post-1" class="itng-blog col-md-6 col-lg-4 post-1 post type-post status-publish format-standard hentry category-1">
		<div class="itng-card-wrapper">
			<div class="itng-thumb">
							</div>
			
			<div class="itng-card-content">
				<div class="entry-meta">
					<a href="https://cryptodeeptech.ru/terminal-google-colab/"></a>
					<span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>				</div><!-- .entry-meta -->
				
				<header class="entry-header">
					<h2 class="entry-title"><a href="https://cryptodeeptech.ru/terminal-google-colab/">We create our own terminal in Google Colab for work in GitHub, GDrive, NGrok, etc.</a></h2>				</header><!-- .entry-header -->
				
				<div class="itng_excerpt">
					Currently, machine learning and deep learning have become the hottest trend in the computer science industry.&nbsp;Many developers create amazing projects with Google Colab. What is Google Colab? Google Colab was developed by Google to provide free access to GPUs and TPUs.&nbsp;Google Colab can be defined as an improved version of Jupyter Notebook. Features of Google Colab Google…				</div>
				
				<div class="blog-footer">
					<div class="itng_cats">
						<a href="https://cryptodeeptech.ru/category/%d0%b1%d0%b5%d0%b7-%d1%80%d1%83%d0%b1%d1%80%d0%b8%d0%ba%d0%b8/" rel="category tag">Без рубрики</a>					</div>
					<div class="blog-comments">
						0					</div>
				</div>
			</div>
		</div>
</article><!-- #post-1 -->			</div>
		</div>
			<div id="author_box" class="row no-gutters">
			<div class="author_avatar col-2">
							</div>
			<div class="author_info col-10">
				<h4 class="author_name title-font">
					Crypto Deep Tech				</h4>
				<div class="author_bio">
									</div>
			</div>
		</div>
	
	</main><!-- #main -->

<!--WCLEARFY_PAGE_TYPE_post--><!--WCLEARFY_FOOTER_START--></div><!-- #content-wrapper -->


 <div id="footer-sidebar" class="widget-area">
    <div class="container">
        <div class="row">
                    </div>
    </div>
</div>
	<footer id="colophon" class="site-footer">
		<div class="container">
			<div class="site-info">
				Donation Address: <a href="https://www.blockchain.com/btc/address/1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v" target="_blank">♥  BTC: 1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v</a>				<span class="sep"> | </span>
					Copyright © 2022 «CRYPTO DEEP TECH». 			</div><!-- .site-info -->
		</div>
	</footer><!-- #colophon -->
</div><!-- #page -->

<nav id="menu" class="panel" role="navigation" style="position: fixed; top: 0px; bottom: 0px; height: 100%; left: -15.625em; width: 15.625em;">
	<div class="menu-overlay"></div>
	<div id="panel-top-bar">
		<button class="go-to-bottom"></button>
		<button id="close-menu" class="menu-link"><i class="fa fa-chevron-left" aria-hidden="true"></i></button>
	</div>

	<ul id="menu-main" class="menu"><li class="page_item page-item-53"><a href="https://cryptodeeptech.ru/contacts/">CONTACTS</a></li>
<li class="page_item page-item-43"><a href="https://cryptodeeptech.ru/publication/">PUBLICATIONS</a></li>
<li class="page_item page-item-55"><a href="https://cryptodeeptech.ru/resources/">RESOURCES</a></li>
<li class="page_item page-item-49"><a href="https://cryptodeeptech.ru/study/">STUDY</a></li>
</ul>

	<button class="go-to-top"></button>
</nav>

<div id="sticky-navigation">
	<div class="nav-wrapper">
		 <div class="container">

			 <div class="row justify-content-end align-items-center justify-content-between no-gutters">


				<div class="main-navigation col-lg-9" role="navigation">
					<ul id="menu-desktop" class="menu"><li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-home menu-item-229"><a href="https://cryptodeeptech.ru/">HOME</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-225"><a href="https://cryptodeeptech.ru/publication/">PUBLICATIONS</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-226"><a href="https://cryptodeeptech.ru/study/">STUDY</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-227"><a href="https://cryptodeeptech.ru/resources/">RESOURCES</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-228"><a href="https://cryptodeeptech.ru/contacts/">CONTACTS</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-post menu-item-240"><a href="https://cryptodeeptech.ru/lattice-attack/">BLOG</a></li>
</ul>				</div>

				<button href="#menu" class="menu-link mobile-nav-btn"><i class="fa fa-bars" aria-hidden="true"></i></button>

				<button type="button" id="go-to-field" tabindex="-1"></button>

				<button class="search-btn-sticky ml-auto col-auto"><i class="fa fa-search"></i></button>
				
<div class="itng-search-sticky">
	<form role="search" method="get" class="search-form" action="https://cryptodeeptech.ru/">
				<label>
					<span class="screen-reader-text">Найти:</span>
					<input type="search" class="search-field" placeholder="Поиск…" value="" name="s">
				</label>
				<input type="submit" class="search-submit" value="Поиск">
			</form>	<button type="button" id="go-to-btn" tabindex="-1"></button>
</div>

			</div>
		</div>
	</div>
</div>

<div id="itng-back-to-top" class="show"><i class="fa fa-chevron-up" aria-hidden="true"></i></div>

		<script type="text/javascript">
							jQuery("#post-337 .entry-meta .date").css("display","none");
					jQuery("#post-337 .entry-date").css("display","none");
					jQuery("#post-337 .posted-on").css("display","none");
							jQuery("#post-270 .entry-meta .date").css("display","none");
					jQuery("#post-270 .entry-date").css("display","none");
					jQuery("#post-270 .posted-on").css("display","none");
							jQuery("#post-71 .entry-meta .date").css("display","none");
					jQuery("#post-71 .entry-date").css("display","none");
					jQuery("#post-71 .posted-on").css("display","none");
							jQuery("#post-1 .entry-meta .date").css("display","none");
					jQuery("#post-1 .entry-date").css("display","none");
					jQuery("#post-1 .posted-on").css("display","none");
				</script>
	<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_2b1ae4cca3cc8d12c39be42768565308.js" id="big-slide-js"></script>
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_ccdf893e7d8b26933af0c336bcc3943e.js" id="owl-js-js"></script>
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/jquery.magnific-popup.min.js" id="mag-lightbox-js-js"></script>
<script id="itng-custom-js-js-extra">
var itng = {"toTopEnable":"1","stickyNav":""};
</script>
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_ea8874ba65dbd53bf5c7fb5c619ac579.js" id="itng-custom-js-js"></script>
<script src="./Speed __up secp256k1 with endomorphism - «CRYPTO DEEP TECH»_files/wmac_single_6ec0e9b3201c83a442e24aba829a5f05.js" id="itng-navigation-js"></script>
<!-- Yandex.Metrika counter --> <script type="text/javascript"> (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)}; m[i].l=1*new Date();k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)}) (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym"); ym(89424273, "init", {  id:89424273, clickmap:true, trackLinks:true, webvisor:true, accurateTrackBounce:true }); </script> <noscript><div><img src="https://mc.yandex.ru/watch/89424273" style="position:absolute; left:-9999px;" alt="" /></div></noscript> <!-- /Yandex.Metrika counter -->
<!-- Yandex.Metrika counter -->
<script type="text/javascript">
   (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
   var z = null;m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(89995532, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true,
        webvisor:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/89995532" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->



<!--
Performance optimized by W3 Total Cache. Learn more: https://www.boldgrid.com/w3-total-cache/

Кэширование страницы с использованием disk: enhanced 

Served from: cryptodeeptech.ru @ 2022-08-25 22:06:47 by W3 Total Cache
--></body></html>