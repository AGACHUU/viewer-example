<template>
  <div class="image-container" @mousemove="handleMouseMove" @mouseleave="handleMouseLeave">
    <img
      ref="img"
      class="magnifiable-image"
      src="https://mblogthumb-phinf.pstatic.net/MjAyMTEyMjJfNDcg/MDAxNjQwMTUwOTUzODg2.ywMUl6KPyDdljDTufa1npucGWF5Wyl41Q9NhFyM0Xdog.ntOsJiNdGgz7Hd8VQxk1w7onoPz6ztcDPvsie3hsrzog.JPEG.41minit/1640142789090.jpg?type=w800"
      alt="Magnifiable image"
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'

const img = ref(null)

const handleMouseMove = (e) => {
  if (img.value) {
    //이건 뷰포트에 상대적인 정보를 제고ㅓㅇ하는 객체를 반환함
    //https://developer.mozilla.org/ko/docs/Web/API/Element/getBoundingClientRect
    //left, top, right, bottom, x, y, width, height 등값을 픽셀단위로 반환.
    const rect = img.value.getBoundingClientRect()
    const x = ((e.clientX - rect.left) / rect.width) * 100
    const y = ((e.clientY - rect.top) / rect.height) * 100

    img.value.style.transformOrigin = `${x}% ${y}%`
    img.value.style.transform = 'scale(2)'
    console.log(e.clientX)
  }
}

const handleMouseLeave = () => {
  if (img.value) {
    img.value.style.transform = 'scale(1)'
  }
}
</script>

<style scoped>
.image-container {
  width: 400px;
  height: 300px;
  overflow: hidden;
}

.magnifiable-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}
</style>
