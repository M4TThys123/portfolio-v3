<template>
  <figure class="footer-image__mask">
    <img class="footer-image" :src="imageUrl" :alt="altText">
  </figure>
</template>

<script>
export default {
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    altText: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
.footer-image__mask {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  overflow: hidden;
  margin-bottom: 28px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.16);
}

.footer-image {
  width: 100%;
  transform: scale(1.5);
  padding-top: 5px;
}
</style>
