<template>

</template>

<script>
export default {
  name: "TechStackComponent"
}
</script>

<style scoped>
/* TECH STACK */
.language__list {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
}

.language {
  width: 25%;
  display: flex;
  align-items: center;
  flex-direction: column;
  position: relative;
}

.language__img--wrapper {
  display: flex;
  align-content: center;
  justify-content: center;
  padding: 25px 16px;
}

.language__img {
  width: 100%;
  /* max-width: 100px; */
  transition: all 300ms;
}

.language:hover .language__img {
  filter: brightness(80%);
  opacity: 0.86;
  transform: scale(0.9);
}

.language__name {
  position: absolute;
  bottom: 0;
  transform: scale(0);
  transition: all 300ms;
  font-size: 20px;
}
.language:hover .language__name {
  transform: scale(1);
}
</style>