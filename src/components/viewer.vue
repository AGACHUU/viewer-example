<template>
  <div>
    <div class="wrap">
      <img
        src="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcQMsjWNKKuIKkRCKanNnoNJdl73wsCEHsZ0ckzHqqgDy23V5-Fr"
        alt="monkey ukkikki"
        ref="target"
        class="target"
      />
      <div
        class="target"
        data-scale="2"
        data-image="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcQMsjWNKKuIKkRCKanNnoNJdl73wsCEHsZ0ckzHqqgDy23V5-Fr"
      ></div>
      <div class="photo" ref="photo"></div>
    </div>
  </div>
</template>

<script setup></script>

<style>
.wrap {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.target {
  position: relative;
  width: 500px;
  height: 500px;
  margin: 0 auto;
}
.photo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  transition: transform 0.5s ease-out;
}
</style>

<script>
export default {
  name: 'Viewer'
}
</script>

<style scoped>
#viewer {
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
}
img {
  width: 100%;
  height: auto;
}
div.ming {
  color: pink;
  font-size: 30px;
}
</style>
