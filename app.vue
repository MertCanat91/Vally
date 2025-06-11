<template>
  <!--  Başlık, Logo, Seyahat Planı, Seyahatlerim Listesi-->
<link rel="stylesheet" type="text/css" href="">

<div class="logo">
  <img src="/Travel.png" width= "200px" height="150px"/>

</div>
<div class="travel-list">
<h3 v-if="isTitleVisible === true">Seyahat Listem</h3>
<ul class="list-container">
<li v-for="item in travelList">{{ item.title }}<button>Detay</button></li>
</ul>
</div>

</template>

<script> 
export default{


data(){
  return{
    isTitleVisible: false,
travelList: [
  {
  title: "Antalya 17.01.2024"
  },
  {
  title: "Bursa 06.08.2024"
  },
   {
  title: "Amsterdam 14.10.2024"
  },
   {
  title: "Konya 02.01.2015"
  }
]

  }
}

}
</script>

<style> 
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.logo{
  text-align: center;
  margin-top: 50px;
}

.travel-list{
  text-align: center;
  margin-top: 50px;
}

.list-container{
  margin-top: 20px;
}

.list-container li{
  border-bottom: 1px solid #ccc;
  padding: 10px;
}

body{
  font-family: 'Poppins',sans-serif;
}


.cointainer{
  width: 80%;
  margin: auto;
}

/*Header Start*/
header{
  height: 100 px;
  border-bottom: 2px solid rgba(255, 255, 255, 0.06);
}

header nav{
  display: flex;
  justify-content: space-between;
}

header nav .logo a{
  color: black;
  text-decoration: none;
  font-weight: 700;
  font-size: 2opx;
}

nav ul{
list-style: none;
display: flex;
column-gap: 30px;
}

nav ul li a{
color: black;
text-decoration: none;
transition: color .25s ease;
}

nav ul li a:hover{
  color: #0ba2c0;

}

nav menu{
  display: flex;
  align-items: center;
  column-gap: 48px;
}

nav .menu .menu-button{
  color: #0ba2c0;
  text-decoration: none;
  background-color: rgba(255, 255,255,0.08);
  padding: 12px 24px;
  border-radius: 56 px ;
  transition: all .25s ease;
}

nav .menu .menu-button:hover{
background-color: #0ba2c0;
color: white;  
}

/*Header End*/

/*Section Start*/
.content{
  color: white;
}


/*Section Start*/


/* Responsive Start */
@media(max-width:576px){
  container {
    width: 100%;
    padding-left: 12px;
    padding-right: 12px;
  }

  .menu ul{
    column-gap: 20px;
  }

  .menu .menu-button{
    display: none;
  }
}






/* Responsive End*/

</style>

