<div class="header">
  <span class="top">The</span>
  <span class="middle">Mr. Fruit</span>
  <span class="bottom">Font</span>
</div>

<div class="content">
<p>The Mr. Fruit Font is an homage to the handwritten produce signs that populate the storefronts of Mr. Fruit bodegas across Brooklyn (Mr. Kiwi, Mr. Kale, Mr. Lemon, Mr. Mango, & more).
</p>
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

.header {
  margin: auto;
  position: relative;
  height: 250px;
  width: 90%;
  max-width: 600px;
}


.content {
  margin: auto;
  position: relative;
  height: 200px;
  width: 90%;
  max-width: 600px;
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
  position: absolute;
}

p{
	font-size: 20px;
	font-weight: 600;
	/* font-family: 'Mr Fruit', sans-serif; */
}

.top {
  top: 0;
  left: 0;
  color: #df1b0d;
}

.middle {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 90px;
  text-align: center;
  white-space: nowrap;
}

.bottom {
  bottom: 0;
  right: 0;
  color: #df1b0d;
}

/* 🔽 Media Queries for responsiveness */
@media (max-width: 600px) {
  .header {
    width: 100%;
    height: 220px; /* Optional: adjust if space is tight */
  }

  .middle {
    font-size: 12vw; /* Scale with screen width */
  }

  .top,
  .bottom {
    font-size: 6vw;
  }
}
</style>
