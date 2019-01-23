<template>
  <div class="app">
    <div class="demo-content align-center morphing-demo">
      <svg width="140" height="140" viewBox="0 0 140 140">
        <g fill="none" fill-rule="evenodd">
          <g fill="#5f41f4" fill-opacity=".35" transform="translate(0 6)">
            <polygon points="70 0 136.574 48.369 111.145 126.631 28.855 126.631 3.426 48.369"></polygon>
            <polygon points="70 18 119.455 53.931 100.565 112.069 39.435 112.069 20.545 53.931"></polygon>
            <polygon points="70 34.86 101.727 57.911 89.609 95.209 50.391 95.209 38.273 57.911"></polygon>
            <polygon points="70 50.898 84.864 61.697 79.186 79.171 60.814 79.171 55.136 61.697"></polygon>
          </g>
          <polygon class="polymorph" stroke-width="1" stroke="#f4e541" points="70 39.21620268803271 118.67892925364514 59.47392925364513 109.99077820990351 131.05706119532297 59.80570746354864 86.41479731196729 18.642202688032704 59.73942447812919 "></polygon>
        </g>
      </svg>
    </div>
  </div>
</template>

<script>
import anime from 'animejs'
export default {
  mounted () {
    anime({
      targets: '.morphing-demo .polymorph',
      points: [
        { value: [
          '70 24 119.574 60.369 100.145 117.631 50.855 101.631 3.426 54.369',
          '70 41 118.574 59.369 111.145 132.631 60.855 84.631 20.426 60.369']
        },
        { value: '70 6 119.574 60.369 100.145 117.631 39.855 117.631 55.426 68.369' },
        { value: '70 57 136.574 54.369 89.145 100.631 28.855 132.631 38.426 64.369' },
        { value: '70 24 119.574 60.369 100.145 117.631 50.855 101.631 3.426 54.369' }
      ],
      easing: 'easeOutQuad',
      duration: 2000,
      loop: true
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="css" scoped>
.app {
  height: 400px;
  width: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
