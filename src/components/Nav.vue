<template>
  <nav class="nav">
    <div class="nav__links">
      <div class="nav__logo">
        <a href="#project-1">
          <img src="~@/assets/images/art-logo.svg" alt="ART logo">
        </a>
      </div>
      <div class="nav__links__inner">
        <ul>
          <li><a href="#" class="active">Art works</a></li>
          <li><a href="#">Aucnions</a></li>
          <li><a href="#">Galleries</a></li>
          <li><a href="#">Fairs</a></li>
        </ul>
      </div>
    </div>
    <div class="nav__buttons">
      <button type="button" class="nav__button"><svg-icon icon="home" /></button>
      <button type="button" class="nav__button"><svg-icon icon="menu" /></button>
    </div>
  </nav>
</template>

<script>
export default {}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .nav{
    position: absolute;
    top: 0;
    left: 0;
    display: flex;
    justify-content: space-between;
    width: 100%;
    z-index: 99;
    padding: 0 10%;
    margin-top: 60px;
    
  }
  .nav__links__inner ul{
    display: flex;
    align-items: center;
  }
  .nav__links__inner{
    margin-left: 10%;
  }
  .nav__links__inner li{
    margin: 0 15px;
  }
  .nav__links__inner li a{
    font-size: 1em;
    font-family: "Poppins", sans-serif;
    color: #fff;
    text-decoration: none;
    white-space: nowrap;
    transition: color 0.4s;
  }
  .nav__links__inner li a:hover{
    transition: color 0.4s;
    color: #06B7FA;
  }
  .nav__links__inner li a.active{
    color: #5F6E76;
  }
  .nav__links{
    display: flex;
    align-items: center;
  }
  .nav__logo img{
    width: 80px;
  }
  .nav__button{
    border: none;
    font-size: 1.2em;
    background: transparent;
    color: #fff;
    padding: 5px;
    cursor: pointer;
    transition: 0.3s color;
  }
  .nav__button:hover{
    color: #06B7FA;
    transition: 0.3s color;
  }
  .nav__button:last-of-type{
    font-size: 1.5em;
    margin-left: 10px;
  }
</style>
