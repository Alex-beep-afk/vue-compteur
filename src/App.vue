<script setup>

</script>

<template>
  <body>
     <span class="counter-title">Compteur Title</span>
    <div class='container'>
        
      <div class='counter-container' >
        <span class="counter-display">0</span>
      </div>

      <div class='buttons-container'>
          <button id='moins'>-</button>
          <button id='plus'>+</button>
      </div>
    </div>
  </body>
 
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');

body{

	display:flex;
  flex-direction: column;
	align-items: center;
	justify-content: center;
	height:100vh;
	margin:0;

}


.container{
	box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
	height:530px;
	width:500px;
	border-radius:5px;
}


.counter-title{
	font-size: large;
	font-size: 3em;
	color: rgb(105, 11, 65);
	font-family: 'Bebas Neue', cursive;
}

.counter-container{
	height:500px;
	display:flex;
	justify-content: space-evenly;
	align-items: center;
}

.counter-display{
	font-size: 24em;
	font-family: 'Bebas Neue', cursive;
}

.buttons-container{
	display:flex;
	justify-content: space-between;
}

.buttons-container button{
	background-color: rebeccapurple;
	color:white;
	border:none;
	font-size: 1.5em;
	cursor:pointer;
	width:49%;
}

.buttons-container button:hover{
	opacity:0.8;
}
</style>
