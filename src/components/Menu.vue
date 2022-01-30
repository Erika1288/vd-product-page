<template>
  <section>
    <div id="menu-principal">
      <a href="#">INICIO</a>
      <a href="#">TOCADOS</a>
      <a href="#">PAMELAS</a>
      <a href="#">TOCADOS NOVIA</a>
      <a href="#">PAJARITAS</a>
    </div>
    <div>
      <form @submit.prevent="handleEnviar">
          <input type="text" placeholder="Buscar productos...">
          <button id="login"><i class="fas fa-search"></i></button>
      </form>
    </div>
    <div id="registro">
      <button >
        <i class="fas fa-user-circle" id="login"></i>
      </button>
      <i class="fas fa-angle-down"></i>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
section {
  
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  
  
}
div{
  display: flex;
  align-items: center;
}
div a{
  display: flex;
  font-size:20px;
  text-decoration: none;
  margin: 10px;
  color: white;
  font-family: monospace;
}
#registro {
  color: pink;
  padding-right: 40px;
  
}
a:hover{
  background-color: rgb(5, 5, 5);
  padding: 10px;
}
form{
  display: flex;
  justify-content: center;
  align-items: center;
}
input{
  margin: 1rem;
    padding: 3px 18px;
    border-style: solid;
    border: 2px solid pink;
    outline: none;
    line-height: 1.4rem;
    border-radius: 25px;
    font-size: 14px;
    background-color: rgb(125 125 199);
    
}
button{
  background-color: rgb(125 125 199);
  border: none;
  cursor: pointer;
}
i{
  color: pink;
  font-weight: bold;
  font-size: 20px;
}
#login{
  font-size: 40px;
}
::placeholder{
  color: white;
}

</style>