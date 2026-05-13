## style.css structure:
- Css Reset
- Variables (colors, spacing, radius)
- Typography
- Links
- Buttons
- Inputs
- Layout
- Helpers (utility classes)

#Example of Variables:
:root{

  /* Colors */
  --primary: #0f0c3d;
  --primary-light:#221d5b;
  --primary-dark:#0d041d;
  --secondary:#dbd8e5;
  --accent: #f5b790;

  /* Typography */
  --font-primary: 'Montserrat';
  --font-secondary: 'Montserrat';

  /* Gap */
  --gap-xs:0.25rem;
  --gap-s:0.5rem;
  --gap-m:1rem;
  --gap-l:1.25rem;
  --gap-xl:1.5rem;
  --gap-xxl:2rem;
  --gap-3xl:3rem;

  /* Margin */
  --margin-xs:0.25rem;
  --margin-s:0.5rem;
  --margin-m:1rem;
  --margin-l:1.25rem;
  --margin-xl:1.5rem;
  --margin-xxl:2rem;
  --margin-3xl:3rem;

  /* Padding */
  --spacing-unit: 1rem;
  --padding-s: clamp(2rem, 1.614rem + 1.928vw, 4rem);
  --padding-m: clamp(4rem, 3.824vw + 0.776rem, 6rem);
  --padding-l: clamp(6rem, 3.824vw + 0.776rem, 8rem);

  /* Radius */
  --radius-s:0.25rem;
  --radius-m:0.5rem;
  --radius-l:1rem;
  --radius-xl:2rem;
  --radius-2xl:3rem;
  --radius-full: 100rem;

  /* Shadows */
  --shadow-s: 0 0.25rem 1rem -1rem var(--primary);
  --shadow-m: 0 0.5rem 1.25rem -1rem var(--primary);
  --shadow-l: 0 0.8rem 1.8rem -1rem var(--primary);
  --shadow-xl: 0 1rem 2rem -1rem var(--primary);
 
  /* Transitions */
  --transition-fast: .35s;
  --transition-med: .6s;
  --transition-slow: 1s;
  --transition-veryslow: 1.5s;

}

#Example of Typography:
@font-face {
    font-family: 'Montserrat';
    src: url('/wp-content/themes/ditto-1.2/assets/fonts/Montserrat-Regular.woff2') format('woff2');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
}

h1, .h1{
  font-weight: 600;
  font-size: clamp(1.5rem, 1.185rem + 3.333vw, 2.488rem);
}

#Example of Links:
a{
  color: var(--accent);
  transition: var(--transition-fast);
}

Example of buttons:
a.button,
.button a,
.wp-block-button__link
{
	font-family: var(--font-primary);
	font-size:1rem;
	font-weight:400;
	letter-spacing: 0.5px;
  text-align: center;
	color: var(--primary);
	background-color: var(--accent);
	padding: 1rem 1.5rem;
	border: 1px solid transparent;
	display:inline-block;
	width: fit-content;
	transition: all var(--transition-fast);
	cursor: pointer;
	position: relative;
	border-radius: var(--radius-2xl);
  -webkit-font-smoothing: initial;
}

#Example of Inputs:
input[type="checkbox"],
input[type="radio"]
{
    appearance: none !important;
    -webkit-appearance: none !important;
    min-width:18px;
    height: 18px;
    padding: 0;
    border: 1px solid var(--primary);
    cursor: pointer;
    position: relative;
    border-radius: 4px;
}

input[type="checkbox"],
input[type="radio"]:checked
{
    border-color: var(--accent);
}

input[type="checkbox"]:before,
input[type="radio"]:before
{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 2.5px solid #fff;
    border-radius: 4px;
    background: var(--accent);
    opacity: 0;
    transition: var(--transition-fast);
}

input[type="radio"],
input[type="radio"]:before
{
    border-radius: 100px;
}

input[type="checkbox"]:checked:before,
input[type="radio"]:checked:before
{opacity: 1;}


#Example of Layout:
.container,
.row
{
  max-width: 1320px;
  margin: 0 auto;
  position: relative;
}

.container {
  display: flex;
  flex-wrap: wrap;
  gap: var(--gap-3xl);
  width: 100%;
  padding: var(--padding-s) var(--padding-m);
  z-index: 1;
}

.row{
  width: 100%;
}


#Example of Helpers:

/* columns */
.col-20 {width:20%}
.col-25 {width:25%}
.col-30 {width:30%}
.col-33 {width:33.33%}
.col-40 {width:40%}
.col-50 {width:50%}
.col-60 {width:60%}
.col-66 {width:66.66%}
.col-70 {width:70%}
.col-75 {width:75%}
.col-80 {width:80%}
.col-90 {width:90%}
.col-100 {width:100%}

/* Flex */
.flex{display: flex;}
.flex-col{flex-direction: column;}
.flex-col-rev{flex-direction: column-reverse;}
.flex-row{flex-direction: row;}
.flex-row-rev{flex-direction: row-reverse;}
.flex-wrap{flex-wrap: wrap;}
.nowrap{flex-wrap: nowrap;}
.items-c{align-items: center;}
.content-c{justify-content: center;}
.space-between{justify-content:space-between;}
.space-evenly{justify-content:space-evenly;}
.flex-start{align-items: flex-start;}
.flex-end{align-items: flex-end;}
.justify-stretch{justify-content: stretch;}

/* Grid */
.grid{display:grid;}
.grid-2{grid-template-columns: repeat(2, 1fr);}
.grid-3{grid-template-columns: repeat(3, 1fr);}
.grid-4{grid-template-columns: repeat(4, 1fr);}
.grid-5{grid-template-columns: repeat(5, 1fr);}
.grid-6{grid-template-columns: repeat(6, 1fr);}
.grid-7{grid-template-columns: repeat(7, 1fr);}
.grid-8{grid-template-columns: repeat(8, 1fr);}
.grid-auto{grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));}

/* Width */
.w100{width: 100%;}
.wfit{width: fit-content;}
.wauto{width: auto;}
.max-320{max-width: 320px;}
.max-480{max-width: 480px;}
.max-540{max-width: 540px;}
.max-640{max-width: 640px;}
.max-720{max-width: 720px;}
.max-960{max-width: 960px;}
.max-full{max-width:100%;}
.min-320{min-width: 320px;}
.min-full{min-width:100%;}

/* Height */
.h100{height: 100%;}
.hauto{height: auto;}
.mh60{min-height: 60vh;}

/* Margin */
.mta{margin-top: auto;}
.mt0{margin-top:0;}
.mt1{margin-top:1rem;}
.mt2{margin-top:2rem;}

.mla{margin-left:auto;}
.mra{margin-right:auto;}
.mrla{margin-right: auto; margin-left: auto;}

.mb0{margin-bottom:0;}
.mb1{margin-bottom:1rem;}
.mb2{margin-bottom:2rem;}

/* Padding */
.pt0{padding-top:0;}
.pl0{padding-left: 0;}
.p0{padding: 0;}

.pt1{padding-top: 1rem;}
.pt2{padding-top: 2rem;}
.pb0{padding-bottom:0;}
.pb1{padding-bottom: 1rem;}
.pb2{padding-bottom: 2rem;}

.p0{padding:0;}
.p-s{padding: var(--padding-s);}
.p-m{padding: var(--padding-m);}
.p-l{padding: var(--padding-l);}

/* Display */
.none{display:none;}
.block{display: block;}
.hidden{visibility:hidden;}

/* Text */
.uppercase{text-transform:uppercase;}
.lowercase{text-transform: lowercase;}
.italic{font-style:italic;}
.t-center{text-align: center;}
.ws-nowrap{white-space: nowrap;}
.fw400{font-weight:400;}
.fw700{font-weight:700;}

/** Radius **/
.radius-m{border-radius: var(--radius-m);}
.radius-l{border-radius: var(--radius-l);}
.radius-xl{border-radius: var(--radius-xl);}
.radius-full{border-radius: var(--radius-full);}

/* Object */
.fit-contain{object-fit: contain;}
.fit-cover{object-fit: cover;}

/* Background */
.bg-none{background:none;}
.bg-white{background-color:#fff;}
.bg-accent{background-color:var(--accent);}
.bg-primary{background-color:var(--primary);}

/* Position */
.p-rel{position: relative;}
.p-abs{position: absolute;}

/* Gap */
.gap0{gap: 0;}
.gap-xs{gap: var(--gap-xs);}
.gap-s{gap: var(--gap-s);}
.gap-m{gap: var(--gap-m);}
.gap-l{gap: var(--gap-l);}
.gap-xl{gap: var(--gap-xl);}
.gap-xxl{gap: var(--gap-xxl);}
.gap-3xl{gap: var(--gap-3xl);}
