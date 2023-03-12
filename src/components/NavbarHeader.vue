<template>
  <nav id='menu'>
  <input type='checkbox' id='responsive-menu' onclick='updatemenu()'><label></label>
  <ul class="left-menu" >
    <li><a href='http://'><img :src="require('@/assets/logo.png')" alt='HiveMed logo' style="margin-right: 10px;">HiveMed</a></li>
    <li><a href='http://'>Home</a></li>
    <li><a class='dropdown-arrow' href='http://'>Products</a>
      <ul class='sub-menus'>
        <li><a href='http://'>Products 1</a></li>
        <li><a href='http://'>Products 2</a></li>
        <li><a href='http://'>Products 3</a></li>
        <li><a href='http://'>Products 4</a></li>
      </ul>
    </li>
    <li><a href='http://'>About</a></li>
    <li><a class='dropdown-arrow' href='http://'>Services</a>
      <ul class='sub-menus'>
        <li><a href='http://'>Services 1</a></li>
        <li><a href='http://'>Services 2</a></li>
        <li><a href='http://'>Services 3</a></li>
      </ul>
    </li>
    <li><a href="#contact">Contact Us</a></li>
  </ul>
	<ul><li><a href='http://' style="margin-left: 320px;">Sign Up</a></li></ul>
	<ul class="login"><li><a href="#" class="">Login</a></li></ul> 
</nav>
</template>

<script>
export default {
  name: 'NavbarHeader',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#menu {
  z-index: 1000;
}

img {
  width: 40px;
  height: 40px;
  object-fit: cover;
}
#menu {
	background: #FFFFFF;
	color: #FFF;
	height: 50px;
	padding-left: 18px;
	border-radius: 8px;
	z-index: 1000;
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
}
#menu ul, #menu li {
	margin: 0 auto;
	padding: 0;
	list-style: none
}
#menu ul {
	width: 100%;
}
#menu li {
	float: left;
	display: inline;
	position: relative;
}
#menu a {
	display: block;
	line-height: 50px;
	padding: 0 14px;
	text-decoration: none;
	color: #000000;
	font-size: 20px;
}
#menu a.dropdown-arrow:after {
	content: "\25BE";
	margin-left: 5px;
}
#menu li a:hover {
	color: #0099CC;
	background: #F2F2F2;
}
#menu input {
	display: none;
	margin: 0;
	padding: 0;
	height: 50px;
	width: 100%;
	opacity: 0;
	cursor: pointer
}
#menu label {
	display: none;
	line-height: 50px;
	text-align: center;
	position: absolute;
	left: 35px
}
#menu label:before {
	font-size: 1.6em;
	content: "\2261"; 
	margin-left: 20px;
}
#menu ul.sub-menus{
	height: auto;
	overflow: hidden;
	width: 170px;
	background: #000000;
	position: absolute;
	z-index: 99;
	display: none;
}
#menu ul.sub-menus li {
	display: block;
	width: 100%;
}
#menu ul.sub-menus a {
	color: #FFFFFF;
	font-size: 15px;
}
#menu li:hover ul.sub-menus {
	display: block
}
#menu ul.sub-menus a:hover{
	background: #F2F2F2;
	color: #444444;
}
@media screen and (max-width: 800px){
	#menu {position:relative}
	#menu ul {background:#111;position:absolute;top:100%;right:0;left:0;z-index:3;height:auto;display:none}
	#menu ul.sub-menus {width:100%;position:static;}
	#menu ul.sub-menus a {padding-left:30px;}
	#menu li {display:block;float:none;width:auto;}
	#menu input, #menu label {position:absolute;top:0;left:0;display:block}
	#menu input {z-index:4}
	#menu input:checked + label {color:white}
	#menu input:checked + label:before {content:"\00d7"}
	#menu input:checked ~ ul {display:block}
}
.login a {
  background-color: black;
  color: #fff!important;
  padding: 10px 20px;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.login a:hover {
  background-color: #fff;
  color: black!important;
}


</style>
