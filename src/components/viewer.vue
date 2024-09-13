<template>
  <div id="viewer">
    <img
      src="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcQMsjWNKKuIKkRCKanNnoNJdl73wsCEHsZ0ckzHqqgDy23V5-Fr"
      alt="Embedded Image"
    />
  </div>
  <div class="ming">원숭희</div>
</template>

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
