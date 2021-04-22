<template>
  <div class="gallery">
    <h1>Gallery</h1>
  </div>
</template>

<script>
export default {
  name: 'Gallery',
};
</script>

<style lang="scss" scoped>
.gallery {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #fcecdd;
  height: calc(100vh - 20rem);
}

h1 {
  font-size: 6rem;
}
</style>
