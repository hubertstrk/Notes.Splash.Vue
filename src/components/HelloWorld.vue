<template>
  <div class="content">
    <div class="circle color1"></div>
    <div class="circle color2"></div>
    <div class="circle color3"></div>
    <div class="circle color4"></div>
    <div class="circle color5"></div>
    <svg>
      <circle cx="300" cy="100" r="40" stroke="white" stroke-width="0" fill="white" />
    </svg>
    <div class="title">
      <kbd class="letter color1"><span>N</span></kbd>
      <kbd class="letter color2"><span>O</span></kbd>
      <kbd class="letter color3"><span>T</span></kbd>
      <kbd class="letter color4"><span>E</span></kbd>
      <kbd class="letter color5"><span>S</span></kbd>
    </div>
  </div>
</template>

<script>
import anime from 'animejs'
export default {
  mounted () {
    var path1 = anime.path('.content circle')

    anime({
      targets: '.content .circle',
      translateX: path1('x'),
      translateY: path1('y'),
      easing: 'easeInOutSine',
      duration: 1000,
      loop: true,
      delay: anime.stagger(120)
    })

    anime({
      targets: '.title .letter',
      translateY: 300,
      direction: 'reverse',
      easing: 'easeInOutBack',
      delay: anime.stagger(300)
    })
  }
}
</script>

<style lang="css">
:root {
  --circle-perimeter: 20px;
  --background-color: #FFFFFF;
}

.content {
  overflow: hidden;
  height: 300px;
  width: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  background-color: var(--background-color);
}

.progress-bar {
  /* height: 10px; */
  background-color: black;
  width: 600px;
}

.title {
  display: flex;
  background-color: var(--background-color);
  letter-spacing: 3px;
}

.letter {
  color: #ddd;
  font-size: 40px;
}

.circle {
  position: absolute;
  border-radius: 50%;
  height: var(--circle-perimeter);
  width: var(--circle-perimeter);
  top: calc(var(--circle-perimeter) / 2 * (-1));
  left: calc(var(--circle-perimeter) / 2 * (-1));
}


.color1 {
  background-color: rgb(255, 84, 84);
} 
.color2 {
  background-color: rgb(255, 240, 84);
} 
.color3 {
  background-color: rgb(0, 219, 116);
} 
.color4 {
  background-color: rgb(84, 200, 255);
} 
.color5 {
  background-color: rgb(175, 84, 255);
} 
</style>
