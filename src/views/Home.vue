<template>
  <div class="home">
    <div class="photos">
      <img src="../assets/images/photo-1.jpg" alt="photo1" class="photo-1" />
      <img src="../assets/images/photo-2.jpg" alt="photo2" class="photo-2" />
      <img src="../assets/images/photo-3.jpg" alt="photo3" class="photo-3" />
      <img src="../assets/images/photo-4.jpg" alt="photo4" class="photo-4" />
      <img src="../assets/images/photo-5.jpg" alt="photo5" class="photo-5" />
    </div>
    <div class="title"><h1>Kelly's Alterations</h1></div>
    <div class="info-container">
      <img src="../assets/images/kelly-portrait.jpg" alt="portrait-image" />

      <h2>
        Alterations for men, women and children. If you can imagine it, I will
        create it.
      </h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  background: #fcecdd;
  height: calc(100vh - 20rem);

  & div {
    width: 33%;
  }
}

.photos {
  position: relative;

  & img {
    background: #2f2f2f;
    width: 40%;
    border-radius: 10px;
    -webkit-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
    box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
  }
}

.photo {
  &-1 {
    position: absolute;
    top: 80px;
    left: 100px;
    transition: all 0.2s ease-in-out;

    &:hover {
      transform: scale(1.5);
      z-index: 10;
    }
  }
  &-2 {
    position: absolute;
    top: 180px;
    left: 250px;
    transition: all 0.2s ease-in-out;

    &:hover {
      transform: scale(1.5);
      z-index: 10;
    }
  }
  &-3 {
    position: absolute;
    top: 280px;
    left: 150px;
    transition: all 0.2s ease-in-out;

    &:hover {
      transform: scale(1.5);
      z-index: 10;
    }
  }
  &-4 {
    position: absolute;
    top: 380px;
    left: 300px;
    transition: all 0.2s ease-in-out;

    &:hover {
      transform: scale(1.5);
      z-index: 10;
    }
  }
  &-5 {
    position: absolute;
    top: 480px;
    left: 125px;
    transition: all 0.2s ease-in-out;

    &:hover {
      transform: scale(1.5);
      z-index: 10;
    }
  }
}

.title {
  display: flex;
  padding-top: 15rem;
  font-family: 'Dancing Script', cursive;
  font-size: 25rem;

  & h1 {
    padding-left: 3rem;
  }
}
.info-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;

  & img {
    width: 50%;
    margin-top: 3rem;
    border-radius: 10px;
    -webkit-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
    box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
  }

  & h2 {
    font-size: 3rem;
    width: 60%;
    text-align: justify;
  }
}
</style>
