# Bharath-Intern
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Personal Portfolio Website 2022</title>
<style>
*{
	padding: 0;
	margin: 0;
	box-sizing: border-box;
	font-family: 'Jost', sans-serif;
	list-style: none;
	text-decoration: none;
	scroll-behavior: smooth;
}
:root{
	--bg-color: #ffffff;
	--text-color: #000;
	--secound-color: #a09dab;
	--main-color: #f75023;
	--big-font: 5rem;
	--h2-font: 3rem;
	--p-font: 1.1rem;
}
body{
	background: var(--bg-color);
	color: var(--text-color);
}
header{
	position: fixed;
	width: 100%;
	top: 0;
	right: 0;
	z-index: 1000;
	display: flex;
	align-items: center;
	justify-content: space-between;
	background: transparent;
	padding: 30px 18%;
	transition: .3s;
}
.logo img{
	max-width: 100%;
	width: 130px;
	height: auto;
}
.navlist{
	display: flex;
}
.navlist li{
	position: relative;
}
.navlist a{
	font-size: var(--p-font);
	color: var(--text-color);
	font-weight: 500;
	padding: 10px 27px;
}
.navlist a::after{
	content: '';
	position: absolute;
	width: 0;
	height: 2px;
	background: var(--main-color);
	bottom: -3px;
	left: 0;
	transition: ease .40s;
}
.navlist a:hover::after{
	width: 100%;
}
#menu-icon{
	font-size: 35px;
	color: var(--text-color);
	z-index: 10001;
	cursor: pointer;
	display: none;
}
.top-btn{
	display: inline-block;
	padding: 9px 30px;
	background: transparent;
	border: 2px solid var(--main-color);
	border-radius: 30px;
	color: var(--text-color);
	letter-spacing: 1px;
	font-size: var(--p-font);
	font-weight: 500;
	transition: ease .50s;
}
.top-btn:hover{
	transform: scale(1.1);
	background: var(--main-color);
	border: 2px solid var(--main-color);
	color: var(--bg-color);
}

section{
	padding: 100px 18%;
}
.home{
	min-height: 100vh;
	height: 100%;
	width: 100%;
	background: url(../img/background.jpg);
	background-size: cover;
	background-position: center;
	position: relative;
	display: grid;
	grid-template-columns: repeat(2, 1fr);
	align-items: center;
	grid-gap: 4rem;
}
.home-text h1{
	margin: 10px 0px 25px;
	font-size: var(--big-font);
	line-height: 1;
	font-weight: 500;
}
.home-text h5{
	margin-bottom: 23px;
	font-size: 19px;
	font-weight: 500;
}
span{
	color: var(--main-color);
}
.home-text h3{
	color: var(--main-color);
	font-size: 20px;
	font-weight: 500;
}
.home-text p{
	font-size: var(--p-font);
	color: var(--secound-color);
	line-height: 28px;
	margin-bottom: 20px;
}
.social a{
	width: 35px;
	height: 35px;
	border-radius: 50%;
	display: inline-flex;
	align-items: center;
	justify-content: center;
	background: rgba(128,103,240,1);
	font-size: 17px;
	color: var(--bg-color);
	margin-right: 22px;
	margin-bottom: 30px;
}
.social a:hover{
	transform: scale(1.1);
	background: var(--main-color);
	transition: .5s;
}
.btn{
	display: inline-block;
	color: var(--bg-color);
	background: var(--main-color);
	font-size: var(--p-font);
	padding: 10px 40px;
	font-weight: 500;
	line-height: 24px;
	border-radius: 30px;
	transition: ease .40s;
}
.btn:hover{
	transform: scale(1.1);
}
.home-img img{
	max-width: 100%;
	width: 540px;
	height: auto;
}
header.sticky{
	background: var(--bg-color);
	padding: 13px 18%;
	box-shadow: 0px 0px 10px rgb(0 0 0 / 10%);
}

.items{
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(220px, auto));
	grid-gap: 2rem;
	align-items: center;
	text-align: center;
}
.sub-box{
	padding: 45px 45px 45px 45px;
	transition: ease .50s;
	cursor: pointer;
}
.sub-img img{
	max-width: 100%;
	width: 60px;
	height: auto;
	margin-bottom: 20px;
}
.sub-box h3{
	margin-bottom: 20px;
	font-size: 24px;
	font-weight: 500;
}
.sub-box p{
	font-size: var(--p-font);
	color: var(--secound-color);
	line-height: 29px;
}
.sub-box:hover{
	background: #ffffff;
	box-shadow: 18px 0px 87px 0px rgb(10 15 70 / 7%);
	border-radius: 12px;
	will-change: transform;
	transform: perspective(1000px) rotateX(4.80deg) rotateY(10.23deg) scale3d(1.05,1.05,1.05);
}

.about{
	display: grid;
	grid-template-columns: repeat(2, 2fr);
	align-items: center;
	grid-gap: 2rem;
}
.about-img img{
	max-width: 100%;
	width: 540px;
	height: auto;
}
.about-text h2{
	font-size: var(--h2-font);
	font-weight: 500;
	margin: 8px 0px 25px;
	line-height: 1.1;
}
.about-text h3{
	color: var(--main-color);
	font-size: 20px;
	font-weight: 500;
}
.about-text p{
	max-width: 550px;
	font-size: var(--p-font);
	color: var(--secound-color);
	line-height: 28px;
	margin-bottom: 45px;
}

.heading{
	text-align: center;
}
.heading h2{
	font-size: var(--h2-font);
	font-weight: 500;
	margin: 7px 0px 20px;
	line-height: 1.1;
}
.heading h3{
	color: var(--main-color);
	font-size: 20px;
	font-weight: 500;
}
.heading p{
	font-size: var(--p-font);
	color: var(--secound-color);
	line-height: 28px;
}
.portfolio-content{
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(350px, auto));
	grid-gap: 2rem;
	align-items: center;
	margin-top: 5rem;
	text-align: center;
	cursor: pointer;
}
.col{
	position: relative;
}
.col img{
	max-width: 100%;
	width: 550px;
	height: auto;
	object-fit: cover;
	border-radius: 12px;
}
.layer{
	background: transparent;
	height: 100%;
	width: 100%;
	position: absolute;
	top: 0;
	left: 0;
	border-radius: 12px;
	transition: all .40s;
}
.layer:hover{
	background: linear-gradient(rgba(0,0,0,0.5) 0%, #191919);
}
.layer h3{
	position: absolute;
	width: 100%;
	font-size: 25px;
	font-weight: 500;
	color: var(--bg-color);
	bottom: 0;
	left: 50%;
	transform: translateX(-50%);
	opacity: 0;
	transition: all .40s;
}
.layer:hover h3{
	bottom: 52%;
	opacity: 1;
}

.layer h5{
	position: absolute;
	width: 100%;
	font-size:17px;
	font-weight: 500;
	color: var(--bg-color);
	bottom: 0;
	left: 50%;
	transform: translateX(-50%);
	opacity: 0;
	transition: all .40s;
}
.layer:hover h5{
	bottom: 48%;
	opacity: 1;
}

.service-content{
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(400px, auto));
	grid-gap: 2rem;
	align-items: center;
	margin-top: 5rem;
}
.row{
	background: #ffffff;
	box-shadow: 18px 0px 87px 0px rgb(10 15 70 / 7%);
	border-radius: 12px;
	padding: 45px 45px 45px 45px;
	transition: ease .45s;
	cursor: pointer;
}
.s img{
	height: 65px;
	width: 65px;
	background: #f75124;
	padding: 15px;
	border-radius: 50%;
	margin-bottom: 20px;
}
.s.s-tow img{
	background: #baebcd;
}
.s.s-three img{
	background: #d9d1fa;
}
.s.s-four img{
	background: #faedce;
}
.row h3{
	font-size: 24px;
	font-weight: 500;
	margin-bottom: 2px;
}
.row h5{
	font-size: 17px;
	font-weight: 500;
	margin-bottom: 19px;
}
.row p{
	font-size: var(--p-font);
	color: var(--secound-color);
	line-height: 28px;
}
.row:hover{
	will-change: transform;
	transform: perspective(1000px) rotateX(4.80deg) rotateY(10.23deg) scale3d(1.05,1.05,1.05);
}

.cta-box{
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(220px, auto));
	grid-gap: 2rem;
	align-items: center;
	margin-top: 5rem;
	text-align: center;
}
.wrap{
	background: #ffffff;
	box-shadow: 18px 0px 87px 0px rgb(10 15 70 / 7%);
	border-radius: 12px;
	padding: 50px 50px 50px 50px;
	transition: ease .40s;
	cursor: pointer;
}
.one{
	background: #baebcd;
}
.two{
	background: #D9D1FA;
}
.three{
	background: #faedce;
}
.wrap h3{
	font-size: 24px;
	font-weight: 500;
	margin-bottom: 2px;
}
.wrap p{
	font-size: var(--p-font);
}

.contact{
	background: #8067f0eb;
	width: 64%;
	margin: 100px auto;
	padding: 70px 150px;
	display: flex;
	align-items: center;
	justify-content: center;
	text-align: center;
	border-radius: 12px;
	background-image: url(../img/intro.png);
	background-size: cover;
}
.center h3{
	font-size: 30px;
	font-weight: 500;
	margin-bottom: 3px;
	color: var(--bg-color);
}
.center p{
	font-size: var(--p-font);
	color: var(--bg-color);
	line-height: 26px;
	margin-bottom: 25px;
}
.contact .action form input[type="email"] {
	max-width: 100%;
	width: 470px;
	padding: 12px 15px;
	background: var(--bg-color);
	color: var(--text-color);
	border: none;
	outline: none;
	margin: 0 10px 20px 0;
	border-radius: 30px;
}
.contact .action form input[type="submit"] {
	padding: 12px 40px;
	background: var(--main-color);
	color: var(--bg-color);
	border: none;
	outline: none;
	margin: 0 10px 20px 0;
	border-radius: 30px;
	cursor: pointer;
}

.ends{
	text-align: center;
	padding: 40px;
}
.ends p{
	font-size: var(--p-font);
	letter-spacing: 1px;
}

@media (max-width: 1425px){
	header{
		padding: 16px 3%;
		transition: .3s;
	}
	header.sticky{
		padding: 10px 3%;
		transition: .3s;
	}
	section{
		padding: 70px 3%;
		transition: .3s;
	}
	.contact{
		width: 95%;
		transition: .3s;
	}
	:root{
		--big-font: 4rem;
		--h2-font: 2.3rem;
		--p-font: 1rem;
		transition: .3s;
	}
}

@media (max-width: 970px){
	#menu-icon{
		display: block;
	}
	.home{
		min-height: 80vh;
	}
	.navlist{
		position: absolute;
		top: -600px;
		left: 0;
		right: 0;
		flex-direction: column;
		background: var(--main-color);
		text-align: right;
		transition: all .40s;
	}
	.navlist a{
		display: block;
		padding: 1.2rem;
		margin: 1.5rem;
		border-right: 2px solid var(--bg-color);
		color: var(--bg-color);
	}
	.navlist a:hover{
		background: var(--bg-color);
		color: var(--main-color);
	}
	.navlist a::after{
		display: none;
	}
	.navlist.active{
		top: 100%;
	}
}

@media (max-width: 800px){
	.home{
		grid-template-columns: 1fr;
		min-height: 130vh;
		grid-gap: 1rem;
	}
	.home-text{
		padding-top: 55px;
	}
	.home-img{
		text-align: center;
	}
	.home-img img{
		width: 440px;
		height: auto;
	}
	.about{
		grid-template-columns: 1fr;
	}
	.about-img{
		text-align: center;
		margin-bottom: 30px;
	}
	:root{
		--big-font: 3.4rem;
		--h2-font: 2rem;
	}
	section{
		padding: 65px 3%;
		transition: .3s;
	}
}
@media (max-width: 540px){
	.contact .action form input[type="email"] {
		width: 310px;
	}
}
</style>

	<link rel="stylesheet"
  href="https://unpkg.com/boxicons@latest/css/boxicons.min.css">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Jost:wght@100;200;300;400;500;600;700;800;900&display=swap" rel="stylesheet">

</head>
<body>
	<!--------header---->
	<header>
		<a href="#" class="logo"></a>
		<h2>PORTFOLIO</h2>
		<div class="bx bx-menu" id="menu-icon"></div>

		<ul class="navlist">
			<li><a href="#home">Home</a></li>
			<li><a href="#about">About</a></li>
			<li><a href="#portfolio">Projects</a></li>
			<li><a href="#contact">Contact</a></li>
		</ul>
	</header>
	<!--------home---->
	<section class="home" id="home">
		<div class="home-text">
			<h3>Hello, I'm</h3>
			<h1>Bethi Vaishnavi</h1>
			<h5>A Student from<span> SR University</span></h5>
			<p>I'm currently persuing B TECH,I'm very passionate <br> and dedicated to my work.</p>
			
			<a href="https://schooltutoring.com/help/wp-content/uploads/sites/2/2014/07/high-res-student-smiling.jpg" class="btn">About Me</a>
		</div>

		<div class="home-img">
			<img src="https://schooltutoring.com/help/wp-content/uploads/sites/2/2014/07/high-res-student-smiling.jpg"></img>
		</div>
	</section>

	<!--------About---->
	<section class="about" id="about">
		<div class="about-img">
			<img src="https://warringtonwebdesign.co.uk/wp-content/uploads/2019/01/ways-to-become-a-web-designer.jpg">
		</div>

		<div class="about-text">
			<h3>I'm a Web Designer</h3>
			<h2>I Can Design Anything You Want</h2>
			<p>Through my academic and personal experiences,I have cultivated <B>teamwork</B> and<b> problem solving skills</b>.I look forward to begin my career that will allow me to utilise upon the knowledge and experience that i have developedd in my studies..</p>
		</div>
		
	</section>

	<!--------portfolio---->
	<section class="portfolio" id="portfolio">
		<div class="heading">
			<h3>Projects</h3>
			<h2>My Amazing Work</h2>
			<p><br></p>
		</div>

		<div class="portfolio-content">
			<div class="col">
				<img src="https://getgrubly.com/wp-content/uploads/2020/10/Restaurant-Management-System.png">
				<div class="layer">
					<h3>Restaurant Management System</h3>
					<h5></h5>
				</div>
			</div>

			<div class="col">
				<img src="https://i.pinimg.com/originals/08/af/65/08af6552f10e4d2443f9e201bd81d4fe.jpg">
				<div class="layer">
					<h3>Grocery Website</h3>
					<h5></h5>
				</div>
			</div>

            <div class="col">
				<img src="https://i0.wp.com/launchspace.net/wp-content/uploads/2021/04/best-online-shopping-websites.jpg?fit=1000%2C500&ssl=1">
				<div class="layer">
					<h3>Online Shopping Website</h3>
					<h5></h5>
				</div>
			</div>

			<div class="col">
				<img src="https://tse1.mm.bing.net/th?id=OIP.a0Bs6RXRyBAvz-zEJB4g3wHaEK&pid=Api&P=0&h=180">
				<div class="layer">
					<h3>Movie Recommendation System</h3>
					<h5></h5>
				</div>
			</div>

			
			<div class="col">
				<img src="https://i.pinimg.com/736x/8f/4d/24/8f4d24c3ad0f337b2db9760ffce1ec9a.jpg">
				</img>
				<div class="layer">
					<h3>Pet Shop</h3>
					<h5></h5>
				</div>
			</div>
			<div class="col">
				<img src="https://tse4.mm.bing.net/th?id=OIP.ePzHAs6hoAOl1fXOuBF8wwAAAA&pid=Api&P=0&h=180">
				</img>
				<div class="layer">
					<h3>Human Following Robot</h3>
					<h5></h5>
				</div>
			</div>
	</section>
	
	<!--------work---->
	<section class="cta">
		<div class="heading">
		<h2>Achievements</h2>
			<h3>Completed 10+ Certifications <br> Successfully</h3>
		</div>

		<div class="cta-box">
			<div class="wrap one">
				<h3>NPTEL SWAYAM</h3>
				<p>Problem Solving Through C</p>
			</div>

			<div class="wrap two">
				<h3>Java Fundamentals And Programming</h3>
				<p>EDX</p>
			</div>

			<div class="wrap three">
				<h3>Python Programming</h3>
				<p>EDX</p>
			</div>

		</div>
	</section>

	<!--------contact---->
	<section class="contact" id="contact">
		<div class="container">
			<div class="center">
				<h3>Let's talk about everything</h3>
				<p>Don't like forms? Send me an email.</p>
			</div>

			<div class="action">
				<form>
					<input type="email" name="email" placeholder="Enter Your email" required>
					<input type="submit" name="submit" value="Submit">
				</form>
			</div>
		</div>
	</section>

	<!--------ends---->
	<div class="ends">
		<p></p>
	</div>

	<script src="https://unpkg.com/scrollreveal"></script>

	<!--------Link to js---->
	<script type="text/javascript" src="js/pscript.js"></script>
	
</body>
<script>
const header = document.querySelector("header");

window.addEventListener ("scroll", function() {
	header.classList.toggle ("sticky", window.scrollY > 0);
});

let menu = document.querySelector('#menu-icon');
let navlist = document.querySelector('.navlist');

menu.onclick = () => {
	menu.classList.toggle('bx-x');
	navlist.classList.toggle('active');
};

window.onscroll = () => {
	menu.classList.remove('bx-x');
	navlist.classList.remove('active');
};

const sr = ScrollReveal ({
	distance: '45px',
	duration: 2700,
	reset: true
})

sr.reveal('.home-text',{delay:350, origin:'left'})
sr.reveal('.home-img',{delay:350, origin:'right'})

sr.reveal('.sub-service,.about,.portfolio,.service,.cta,.contact',{delay:200, origin:'bottom'})
</script>
</html>
