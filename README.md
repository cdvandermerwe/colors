# colors

+<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Lab #4</title>
  <link rel="stylesheet" href="gridstyle.css">
</head>
<body>
<div class="container">
  <header>
    <h1 id="title">Colors!</h1>
    <h3>An overview of colors, including an in depth look at some of my favorites.</h3>
  </header>
  <nav>
    <ul>
      <li><a href="pink.png">Pink</a></li>
      <li><a href="blue.png">Blue</a></li>
      <li><a href="green.jpeg">Green</a></li>
      <li><a href="purple.png">Purple</a></li>
    </ul>
  </nav>
  <main>
  <section>
      <h2 id="pink">Pink</h2>
      <p>Pink is the color of a namesake flower that is a pale tint of red.[2][3] It was first used as a color name in the late 17th century.[4] According to surveys in Europe and the United States, pink is the color most often associated with charm, politeness, sensitivity, tenderness, sweetness, childhood, femininity, and romance. A combination of pink and white is associated with chastity and innocence, whereas a combination of pink and black links to eroticism and seduction.</p>
      <h2 id="blue">Blue</h2>
      <p>Blue is one of the three primary colours in the RYB colour model (traditional color theory), as well as in the RGB (additive) colour model. It lies between violet and cyan on the spectrum of visible light. The eye perceives blue when observing light with a dominant wavelength between approximately 450 and 495 nanometres. Most blues contain a slight mixture of other colours; azure contains some green, while ultramarine contains some violet. The clear daytime sky and the deep sea appear blue because of an optical effect known as Rayleigh scattering. An optical effect called Tyndall effect explains blue eyes. Distant objects appear more blue because of another optical effect called aerial perspective.</p>
      <h2 id="purple">Purple</h2>
      <p>Purple is any of a variety of colors with hue between red and blue.[1][2] In the RGB color model used in computer and television screens, purples are produced by mixing red and blue light. In the RYB color model historically used by painters, purples are created with a combination of red and blue pigments. In the CMYK color model used in printing, purples are made by combining magenta pigment with either cyan pigment, black pigment, or both.</p>
      <h2 id="green">Green</h2>
      <p>Green is the color between cyan and yellow on the visible spectrum. It is evoked by light which has a dominant wavelength of roughly 495–570 nm. In subtractive color systems, used in painting and color printing, it is created by a combination of yellow and cyan; in the RGB color model, used on television and computer screens, it is one of the additive primary colors, along with red and blue, which are mixed in different combinations to create all other colors. By far the largest contributor to green in nature is chlorophyll, the chemical by which plants photosynthesize and convert sunlight into chemical energy. Many creatures have adapted to their green environments by taking on a green hue themselves as camouflage. Several minerals have a green color, including the emerald, which is colored green by its chromium content.</p>
  </section>
  </main>
  <aside id="aside1">
    <h2>What are colors, anyway?</h2>
    <p>Color (American English) or colour (Commonwealth English) is the visual perceptual property deriving from the spectrum of light interacting with the photoreceptor cells of the eyes. Color categories and physical specifications of color are associated with objects or materials based on their physical properties such as light absorption, reflection, or emission spectra. By defining a color space colors can be identified numerically by their coordinates.</p>
  </aside>
  <aside id="aside2">
    <h2>Learn about colors...</h2>
    <p>Because perception of color stems from the varying spectral sensitivity of different types of cone cells in the retina to different parts of the spectrum, colors may be defined and quantified by the degree to which they stimulate these cells. These physical or physiological quantifications of color, however, do not fully explain the psychophysical perception of color appearance.</p>
  </aside>
  <footer>

    <small> Designed by Chloe van der Merwe</small>
  </footer>
</div>
</body>
</html>



@import url('https://fonts.googleapis.com/css2?family=Akaya+Telivigala&family=Bebas+Neue&family=Noto+Sans&family=Permanent+Marker&family=Redressed&family=Roboto+Slab:wght@500&family=Roboto:wght@100&display=swap');



body {
  background: white;
  font-family: 'Noto Sans';
  font-size: 18px;
}

h1,
h2 {
  font-family: 'Roboto Slab';
  font-size: 1.5em;
  padding: 1em 0;
}

h2 {font-size:1.2em;}


nav{
  font-family: 'Roboto Slab';
  font-size:20px;
}

header {
  grid-area: heady;
  background-color:#D7D1FF;
}

header,
footer {
  text-align: center;
}

nav {
  grid-area: navvy;
  background-color:#FFF7DD;
}

header,
nav,
main,
aside,
footer {
  padding: 1.3em;
  border: 5px white solid;
}

main {
  max-height: 100%;
  grid-area: mainy;
  background-color: #EBC9E0;
}

footer {
  grid-area: footy;
  background-color: white;
}

nav ul {
  justify-content: space-around;
  display: flex;
  flex-flow: row nowrap;

}

nav ul li {
  list-style: none
}



*,
*:before,
*:after {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  background-color:white;
  display: grid;
  width: 100vw;
  height: 100vh;
  grid-template-columns:
   1fr       2fr       1fr;
  grid-template-areas:
  "heady     heady     heady"
  "navvy     navvy     navvy"
  "aside1    mainy     aside2"
  "aside1    mainy     aside2"
  "aside1    mainy     aside2"
  "footy     footy     footy";
}



#title{
  font-size:30px;
}

#aside1 {
  grid-area: aside1;
  background-color: #AAC0F5;
}
#aside2 {
  grid-area: aside2;
  background-color: #C9F0DD;
}


@media screen
  and (min-width: 641px)
  and (max-width: 900px)  {
.container {
grid-template-columns:
   1fr 1fr;
grid-template-areas:
  "heady heady"
  "navvy navvy"
  "mainy mainy"
  "aside1 aside2"
  "footy footy";
}


@media screen
  and (max-width: 640px)  {
.container {
grid-template-columns: 1fr;
grid-template-areas:
  "heady"
  "mainy"
  "aside1"
  "aside2"
  "navvy"
  "footy";
}

