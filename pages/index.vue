<template>
  <div id="main">
    <div class="header">
      <h1><a href="/">SOMEPLACE</a></h1>
    </div>
    # A full screen video background that autoplays and loops
    <video autoplay loop muted :key="current_video">
      <source :src="current_video" type="video/mp4">
    </video>
    <div class="link-container">
      <!-- I need to add a mouseover that changes the current video to aarun.mp4     -->
      <h2 @mouseover="current_video='/aarun.mp4'">Documentary <p>|</p></h2>
      <h2 @mouseover="current_video='/knife%20turning%20test.mp4'">Narrative <p>|</p></h2>
      <h2>Corporate <p>|</p></h2>
      <h2>About Us <p>|</p></h2>
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

/* paragraph is inline */
p{
  display: inline;
}

a{
  text-decoration: none;
  color: white;
}

/* mobile site settings */
/* The h2's will align in the center and shrink down */

@media only screen and (max-width: 850px) {
  .link-container{
    align-items: center;
    justify-content: center;
    height: 100%;
    width: 100%;
    right: 0;
  }

  .header{
    left: 0;
    right: 0;
    top: 25px;
    text-align: center;
  }

  .header h1{
    font-size: 3em;
  }

  .link-container h2{
    text-align: center;
  }

  p{
    display: none;
  }
}

</style>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      current_video: '/aarun.mp4',

    }
  },
}
</script>
