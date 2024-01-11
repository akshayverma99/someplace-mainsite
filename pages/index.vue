<template>
  <div id="main">
    <div class="header">
      <h1>SOMEPLACE</h1>
    </div>
    # A full screen video background that autoplays and loops
    <video autoplay loop muted>
      <source src="/knife%20turning%20test.mp4" type="video/mp4">
    </video>
    <div class="link-container">
      <h2>Documentary |</h2>
      <h2>Narrative |</h2>
      <h2>Corporate |</h2>
      <h2>About Us |</h2>
    </div>
  </div>
</template>

<style>
* {
  font-family: 'Bebas Neue', sans-serif;
  /*font-family: 'Oswald', sans-serif;*/
  /*font-family: 'Roboto Mono';*/
  font-weight: 500;
}

#main {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

#main video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  background-color: black;
  z-index: 1;
}

.header{
  position: fixed;
  top: 20px;
  left: 80px;
  color: white;
  font-size: 1em;
  color: white;
  z-index: 2;
}

.link-container{
  position: fixed;
  top: 50%;
  right: 10%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: center;
  height: 50%;
  width: 50%;
  z-index: 2;
}

.link-container h2{
  font-size: 5em;
  color: white;
  margin: 0;
  padding: 0;
  margin-bottom: 20px;
  cursor: pointer;
}

.link-container h2:hover{
  font-size: 5.2em;
}

</style>

<script>
export default {
  name: 'IndexPage'
}
</script>
