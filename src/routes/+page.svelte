<script>
	import Sandbox from "$components/Sandbox.svelte";
</script>


<div class="header">
  <span class="top">The</span>
  <span class="middle">Mr. Fruit</span>
  <span class="bottom">Font</span>
</div>


<div class="content">
<p>The Mr. Fruit Font is an homage to the handwritten produce signs that populate several of the bodegas within the
	Mr. Fruit chain across Brooklyn (Mr. Kiwi, Mr. Kale, Mr. Lemon, Mr. Mango, & more).</p><p>
  When I moved to Brooklyn after college in 2021, Mr. Kiwi was the first grocery store I visited during my first night in the city.
  In every apartment I've lived in since, I've had a Mr. Fruit bodega within a 5-minute walk, and have continued to shop each one on a near-daily basis.
  </p>

  <p>Everything about these stores has become familiar, and in a sense, comforting. I've shopped in them after insane days at work and after going out,
    after long runs and in cooking emergencies. Over time, it became impossible to not notice and appreciate the unique handwritten signage all around the store:</p>
<img src="/imgs/banner.png"/>


  <p>This project hopes to capture the mundane gorgeousness of these signs in a typeface. I hope you enjoy!

  </p>
  <span class="content-3">- Annie</span><br/><br/>
  <p class="sub">
	In addition to this font, the chain has also inspired <a href="https://hellgatenyc.com/mr-marathon-tribute-to-cheap-produce/">a marathon</a>
	and received copious press coverage (<a href="https://www.nytimes.com/2023/10/04/nyregion/mr-fruit-bodega-brooklyn.html">Hellgate</a>,
	<a href="https://www.grubstreet.com/article/brooklyn-fruit-bodegas-mr-lemon-mr-kiwi.html">Grub Street</a>,
	<a href="https://www.wnyc.org/story/mr-fruit-beloved-bodegas-of-brooklyn/">WNYC</a>).
</p><br/><br/>

<div class="sandbox">
<span class="content-2">Try out the font</span>
<Sandbox /></div><br/><br/>

<span class="content-2">The glyph set</span>
<img src="/imgs/glyphs.png"/><br/><br/>

<span class="content">image gallery</span>
</div>

<div class="gallery">
  <img src="/imgs/IMG_0221.JPG" alt="Mr. Fruit Gallery Image 1">
  <img src="/imgs/IMG_0220.JPG" alt="Mr. Fruit Gallery Image 3">
  <img src="/imgs/IMG_0223.JPG" alt="Mr. Fruit Gallery Image 3">
  <img src="/imgs/IMG_0222.JPG" alt="Mr. Fruit Gallery Image 2">
  <img src="/imgs/IMG_0224.JPG" alt="Mr. Fruit Gallery Image 4">
  <img src="/imgs/IMG_0214.JPG" alt="Mr. Fruit Gallery Image 3">
  <img src="/imgs/IMG_0225.JPG" alt="Mr. Fruit Gallery Image 5">
  <img src="/imgs/IMG_0226.JPG" alt="Mr. Fruit Gallery Image 6">
  <img src="/imgs/IMG_0227.JPG" alt="Mr. Fruit Gallery Image 7">
</div>
<br/><br/>
<style>
@font-face {
  font-family: "Mr Fruit";
  src: url("/assets/MrFruit3-Regular.woff2") format("woff2");
  font-display: swap;
}


@font-face {
	font-family: "Tiempos Text";
	src: url("https://pudding.cool/assets/fonts/tiempos/TiemposTextWeb-Regular.woff2") format("woff2");
	font-weight: 300;
	font-style: normal;
	font-stretch: normal;
	font-display: swap;
}


@font-face {
	font-family: "Tiempos Headline";
	src: url("https://pudding.cool/assets/fonts/tiempos/TiemposHeadlineWeb-Regular.woff2") format("woff2");
	font-weight: 400;
	font-style: normal;
	font-stretch: normal;
	font-display: swap;
}
.sub{
  font-style: italic;
}

.header {
  margin: auto;
  position: relative;
  height: 250px;
  width: 90%;
  max-width: 870px;
}

.sandbox{
	display: block;
	height: auto;

}

.content {
  margin: auto;
  position: relative;
  /* height: 200px; */
  width: 90%;
  max-width: 600px;
}

.content-2{
	font-size: 42px;
}

.content-3{
	font-size: 32px;
  color: red;
  text-align: right;
  width: 100%;
  float: right;
}
.gallery {
  margin: auto;
  position: relative;
  width: 90%;
  max-width: 1000px;
  column-count: 3;
  column-gap: 1rem;
}

.gallery img {
  width: 100%;
  margin-bottom: 1rem;
  break-inside: avoid;
  display: block;
}


span {
  font-family: 'Mr Fruit', sans-serif;
  font-size: 48px;
  /* position: absolute; */
}

p{
	font-size: 20px;
	font-weight: 600;
	/* font-family: 'Mr Fruit', sans-serif; */
}

.top {
  top: 0;
  left: 0;
  display: block;
  color: #df1b0d;
}

.middle {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 95px;
  text-align: center;
  white-space: nowrap;
  position: absolute;
}

.bottom {
  bottom: 0;
  right: 0;
  position: absolute;
  color: #df1b0d;
}

/* 🔽 Media Queries for responsiveness */
@media (max-width: 600px) {
  .header {
    width: 100%;
    height: 150px; /* Optional: adjust if space is tight */
  }

  .middle {
    font-size: 12vw; /* Scale with screen width */
  }

  .top,
  .bottom {
    font-size: 6vw;
  }
}


@media (max-width: 450px) {
  .header {
    width: 100%;
    height: 120px; /* Optional: adjust if space is tight */
  }
}
</style>
