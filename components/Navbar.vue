  <template>
    <div>
        <nav class="navbar">
            <img src="../images/logo.png" alt="Company Logo">
            <div class="menu-toggle" id="mobile-menu" @click="toggleClass()">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
            </div>
            <ul class="nav" :class=" mobilePoint ? 'mobile-nav is-active': ''">
                
            <li class="nav-item"><a href="#">Home</a></li>
            <li class="nav-item"><a href="#">About</a></li>
            <li class="nav-item"><nuxt-link :to="{path:'/employee'}">Employee</nuxt-link></li>
            <li class="nav-item"><a href="#">Careers</a></li>
            <li class="nav-item"><a href="#">Contact Us</a></li>
            </ul>
            <ul class="nav_2">
            <li class="nav-item"><div class="iconImage"><img src="../images/icon-img.png"/></div></li>
            <li class="nav-item"><div class="iconImage"><img src="../images/icon-bell.png"/></div></li>
            </ul>
        </nav>
    </div>
  </template>
    <script>
    export default {
        data(){
        
            return {
        mobilePoint : false
            }
        },
        methods :{
        toggleClass(){
            this.mobilePoint = !this.mobilePoint;
        },
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Lato', 'Arial', sans-serif;
  
}
/* HEADINGS */

h1, p {
  color: #fff;
  text-align: center;
  line-height: 1.4;
}

h1 {
  font-size: 2.2rem;
}

h2 {
  color: #000;
  font-size: 1.3rem;
  text-align: center;
  line-height: 1.4;
  margin-bottom: 10px;
}

/* BASIC SETUP */
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .page-wrapper {
  background-image:url('../images/background_image_1.png');
  width: 98%;
  margin:0 1%;
  height: auto;
    -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .page-wrapper {
  background-image:url('../images/background_image_1.png');
  width: 98%;
  margin:0 1%;
  height: auto;
    -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .page-wrapper {
  background-image:url('../images/background_image_1.png');
  width: 90%;
  margin:0 5%;
  height: auto;
    -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .page-wrapper {
  background-image:url('../images/background_image_1.png');
  width: 80%;
  margin:0 10%;
  height: auto;
    -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .page-wrapper {
  background-image:url('../images/background_image_1.png');
  width: 80%;
  margin:0 10%;
  height: auto;
    -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
}


.nav-wrapper {
  width: 100%;
  height:auto;
  position: relative;
  top: 0;
  background-color: #fff;
}



/* NAVIGATION */

.navbar {
     display: flex;
    justify-content: space-between;
    align-items: center;
    height: auto;
}

.navbar img {
  height: 40px;
  width: auto;
  justify-self: start;
  margin-left: 20px;
}

.navbar ul {
  list-style: none;
  display: flex;
  flex-direction:row;

  
}

.nav-item a {
  color: #000;
  display:inline-block;
  font-size: 0.9rem;
  padding:20px 0;
  margin:0 20px;
  font-weight: 400;
  text-decoration: none;
  transition: color 0.3s ease-out;
}
.nuxt-link-exact-active{
 border-bottom:3px solid lightseagreen;
}
.nav_2{
align-self:flex-end;
}
.nav_2 .nav-item{
  display:flex;
  align-content: center;
}
.iconImage{
  width:30px;
  margin-right:5px;
  height:auto;
}
.iconImage img{
  display:inline-block;
  width:100%;
  margin:auto;
  height:auto
}
/* SECTIONS */
.body-top{
    width:100%;
    height:auto;
    padding:20px 3%;
    display:flex;
    flex-direction:row;
    justify-content: space-between;
    align-items: flex-end;
}
.body-top p{
    font-weight:600;
    font-size:23px;
    color:black;
    margin:auto 20px;
}

.body-top button{
    margin:auto 0;
    padding:10px 20px;
    color:#fff;
    border-radius:15px;
    background:#0ec9ae;
    border:none;
}
.body-top button.click{
    margin:auto 0;
    padding:10px 20px;
    color:#fff;
    border-radius:15px;
    background:lightblue;
    border:none;
}
.body-mid{
    display:flex;
    flex-direction:row;
}



.features {
  width: 100%;
  padding:0 2%;
  height: auto;
  display: flex;
  justify-content: space-around;
}

.feature-container {
  flex-basis: 35%;
  padding:0 10px;
}
.feature-container_2 {
  flex-basis: 65%;
}

.feature-container p {
  color: #000;
  text-align: center;
  line-height: 1.4;
  margin-bottom: 15px;
}

.feature-container img {
  width: 100%;
  margin-bottom: 15px;
}

.nav-side .nav-side-bar{
    height:500px;
    border-radius:15px;
    padding:40px 20px;
    background:#fff;
    display:flex;
    flex-direction:column;
    -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
.nav-side{
  position:relative;
    width: 100%;
    padding:5%;
    height:500px;
}
.nav-side .nav-side-bar .nav-side-bar-image{
    display:flex;
    flex-direction:row;
    justify-content: flex-start;
    align-content: center;
}

.nav-side .nav-side-bar .nav-side-bar-image .side-img{
    width:40px;
    display:flex;
    margin-right:8px;
    align-content:center;
}

.nav-side .nav-side-bar .nav-side-bar-notice p {
  text-align:left;
    color:lightgrey;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul{
    list-style-type: none;
    padding-inline-start: 0 !important;
    width:100%;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul li a{
    display: flex;
    text-decoration:none;
    width:100%;
    margin:10px auto;
    padding:5px 10px;
    border-radius:10px;
    flex-direction:row;
    align-content: center;
    justify-content: flex-start;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul li a:hover , a:active{
    background:#f5f4f2;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul li .side-icon{
    display: flex;
    text-transform: uppercase;
    align-content: center;
    justify-content: center;
    text-align: center;
    font-size:15px;
    width:40px;
    height:40px;
    margin:auto 1px;
    margin-right: 10px;
    border:1px solid lightgrey;
    border-radius:60px;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul li .side-icon p{
    margin:auto;
    float:left;
    text-decoration: none;
    color:black;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul li .side-name{
    display: flex;
    align-content: center;
    justify-content: center;
}
.nav-side .nav-side-bar .nav-side-bar-notice ul li .side-name p{
    color:black;
}
.main-content{
    width:100%;
    height:500px;
    color:black;
}
.main-content-table{
    width:100%;
    /* height:600px; */
}
.main-content-table table{
    width:100%;
    border-collapse: separate;
    border-spacing: 0 10px;
    text-align:left;
}
.main-content-table table thead  p{
    font-size:12px;
    display:block;
    color:black;
    text-align:left;
    margin:0;
}
.main-content-table table tbody {
    margin-top:50px 0; 
    background:#fff;
    color:black
}
.main-content-table table tbody tr{
     background:#fff;
-webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
.main-content-table table tbody td{
     padding:10px 2px;
}
.main-content-table table tbody tr td,th{
}
.main-content-table table tbody tr td:first-child{  -webkit-border-radius:10px 0 0 10px ;padding-top:25px;display:flex;align-content:center;justify-content: center;}
.main-content-table table tbody tr  td:nth-child(2), th:nth-child(2) { width:20px ;}
.main-content-table table tbody tr td:last-child{  -webkit-border-radius:0 10px 10px 0;}
.main-content-table table thead tr th:first-child{ display:flex;align-content:center;justify-content: center;}
.main-content-table table thead tr th:first-child .main{bottom:-12px;}

.main-content-table table tbody td p{
    margin:0;
    text-align:left;
    color:black;
    font-size:13px
}
.main-content-table table tbody td span{
    color:lightgrey;
    font-size:12px;
}
.main-content-table table tbody td .main-content-image{
    width:50px;
    height:auto;
}
.main {
    display: flex;
    position: relative;
    cursor: pointer;
    font-size: 10px;
  }
  /* Hiding the initial checkbox */
  input[type=checkbox] {
    visibility: hidden;
  }
  /* Creating a custom checkbox based on demand */
  .main-checkbox {
    position: absolute;
    top: 0;
    left: 0;
    height: 20px;
    border-radius:5px;
    border:1px solid lightgrey;
    width: 20px;
    background-color: white;
  }
  /* Specify the background color to be shown when hovering over checkbox */
  .main:hover input ~ .main-checkbox {
    border:1px solid black;
  }
  
@media 
only screen and (max-width: 760px),
(min-device-width: 768px) and (max-device-width: 1024px)  {

	table { 
	  	width: 100%; 
      margin-top:50px;
      height:auto;
      display:inline-block;
	}
	table, thead, tbody, th, td, tr { 
		display: block; 
    padding:0 10px;
    
	}
	
	thead tr th { 
		position: absolute;
		top: -9999px;
		left: -9999px;
	}
		thead tr td { 
		position: absolute;
		top: -9999px;
		right: -9999px;
    text-align:right;
	}
	
	td { 
		border: none;
		position: relative;
		padding-left: 50%; 
	}
.main-content-table table tbody td p{
    margin:0;
    text-align:right;
    color:black;
    font-size:13px
}
 .actionClass{
   float:right
}
.main-content-table table tbody td span{
    color:lightgrey;
    font-size:12px;
}
.main{
  display: flex;
    position: relative;
    cursor: pointer;
    bottom: -20px;
    right: 0;
    font-size: 10px;
}
	td:before { 
		position: absolute;
		top: 6px;
		left: 6px;
		width: 45%; 
		padding-right: 10px; 
		white-space: nowrap;
		content: attr(data-column);

		color: #000;
		font-weight: bold;
	}

}
  /* Specify the background color to be shown when checkbox is active */
  .main input:active ~ .main-checkbox {
    background-color: black;
  }
  /* Specify the background color to be shown when checkbox is checked */
  .main input:checked ~ .main-checkbox {
    background-color: white;
  }
  /* Checkmark to be shown in checkbox */
  /* It is not be shown when not checked */
  .main-checkbox:after {
    content: "";
    position: absolute;
    display: none;
  }
  /* Display checkmark when checked */
  .main input:checked ~ .main-checkbox:after {
    display: block;
  }
  /* Styling the checkmark using webkit */
  /* Rotated the rectangle by 45 degree and 
  showing only two border to make it look
  like a tickmark */
  .main .main-checkbox:after {
    left: 4px;
    bottom: 5px;
    width: 6px;
    height: 12px;
    border: solid black;
    border-width: 0 2px 2px 0;
    -webkit-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
  }
input {
  border: 0;
  border-left: 1px solid #ccc;
  border-radius: 0; /* FOR SAFARI */
  outline: 0;
  padding: 5px;
}

/* MOBILE MENU & ANIMATION */

.menu-toggle .bar{
  width: 25px;
  height: 3px;
  background-color: #3f3f3f;
  margin: 5px auto;
  -webkit-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}

.menu-toggle {
  justify-self: end;
  margin-right: 25px;
  display: none;
}

.menu-toggle:hover{
  cursor: pointer;
}

#mobile-menu.is-active .bar:nth-child(2){
  opacity: 0;
}

#mobile-menu.is-active .bar:nth-child(1){
  -webkit-transform: translateY(8px) rotate(45deg);
  -ms-transform: translateY(8px) rotate(45deg);
  -o-transform: translateY(8px) rotate(45deg);
  transform: translateY(8px) rotate(45deg);
}

#mobile-menu.is-active .bar:nth-child(3){
  -webkit-transform: translateY(-8px) rotate(-45deg);
  -ms-transform: translateY(-8px) rotate(-45deg);
  -o-transform: translateY(-8px) rotate(-45deg);
  transform: translateY(-8px) rotate(-45deg);
}

/* KEYFRAME ANIMATIONS */

@-webkit-keyframes gradbar {
	0% {
		background-position: 0% 50%
	}
	50% {
		background-position: 100% 50%
	}
	100% {
		background-position: 0% 50%
	}
}

@-moz-keyframes gradbar {
	0% {
		background-position: 0% 50%
	}
	50% {
		background-position: 100% 50%
	}
	100% {
		background-position: 0% 50%
	}
}

@keyframes gradbar {
	0% {
		background-position: 0% 50%
	}
	50% {
		background-position: 100% 50%
	}
	100% {
		background-position: 0% 50%
	}
}

/* Media Queries */

  /* Mobile Devices - Phones/Tablets */

@media only screen and (max-width: 720px) { 
  .features {
    flex-direction: column;
    padding: 20 50px;
  }
  
  /* MOBILE HEADINGS */
  
  h1 {
    font-size: 1.9rem;
  }
  
  h2 {
    font-size: 1rem;
  }
  
  p {
    font-size: 0.8rem;
  }
  
  /* MOBILE NAVIGATION */
     
  .navbar ul {
    display: flex;
    flex-direction: column;
    position: fixed;
    justify-content: flex-start;
    top: 42px;
    background-color: #fff;
    width: 100%;
    height: calc(100vh - 55px);
    transform: translate(-101%);
    text-align: center;
    overflow: hidden;
  }
  
  .navbar li {
    padding: 15px;
  }
  
  .navbar li:first-child {
    margin-top: 50px;
  }
  
  .navbar li a {
    font-size: 1rem;
  }
   
  .menu-toggle, .bar {
    display: block;
    cursor: pointer;
  }
  
  .mobile-nav {
  transform: translate(0%)!important;
}
  
  /* SECTIONS */
  
  .headline {
    height: 20vh;
  }
    
  .feature-container p {
    margin-bottom: 25px;
  }
  
  .feature-container {
    margin-top: 20px;
  }
  
  .feature-container:nth-child(2) {
    order: -1;
  }
  
  .search-input {
  display: none;
 }
  
}

.form-error{
    border:1px solid lightsalmon;
}
.form-wrappper{
    width:100%;
}
.form-wrappper p{
    text-align: center;
    font-size:30px;
    color:grey;
}
.form-container{
 display: grid;
 width:50%;
 margin:20px auto;
  grid-template-columns: auto auto ;
  border-radius :10px;
  border:1px lightgrey;
  padding: 10px;
   -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}
.form-item{
    display:flex;
    height:auto;
    flex-direction:column;
    margin:10px;
}
input{background: white;
    height: 40px;
    padding: 10px;
    font-size: 15px;
    border: 1px lightgrey;
    border-radius: 10px;
}
label{color:grey}
button{
    margin:10px auto;
    display: flex;
    padding:10px 20px;
    color:#fff;
    border-radius:15px;
    background:#0ec9ae;
    border:none;
    
}
button:focus{background-color:grey;border:1px solid white !important;}

@media 
only screen and (max-width: 760px),
(min-device-width: 768px) and (max-device-width: 1024px)  {
.form-container{
 display: grid;
 width:100%;
 margin:20px auto;
  grid-template-columns: auto  ;
  border-radius :10px;
  border:1px lightgrey;
  padding: 10px;
   -webkit-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
-moz-box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
box-shadow: 0px 6px 10px -6px rgba(186,184,186,1);
}

}
a{
 text-decoration:none !important;
 color:white ;
 font-size:12px;
}
a.btn{
  text-decoration:none !important;
  padding:10px 20px;
  text-align:center;
  background:#0ec9ae;
  border-radius:20px;
}
a.btn2{
  position:absolute;
  left:100px;
  bottom:-35px;
  text-decoration:none !important;
  padding:15px 40px;
  text-align:center;
  background:#8454df;
  border-radius:20px;
}
a.btn:active{
  opacity:0.5
}
a.btn:hover{
  border:1px solid green
}
.actionClass{
  display:flex;
  flex-direction:row;
}
.actionClass div{
  width:25px;height:25px;
}
.actionClass a img{
  width:100%;height:auto;
  margin:auto;
}
</style>