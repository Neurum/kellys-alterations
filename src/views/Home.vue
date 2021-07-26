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
        Alterations for men, women and children. If you can imagine it, I will create it.
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
@media screen and (max-width: 1700px) {
  .title {
    font-size: 20rem;
  }
}
@media screen and (max-width: 1600px) {
  .photos img {
    width: 30%;
  }
}
@media screen and (max-width: 1400px) {
  .title {
    font-size: 15rem;
  }
  .photos img {
    width: 30%;
  }
}
@media screen and (max-width: 1200px) {
  .home {
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    & div {
      width: 80%;
    }
  }
  .title {
    justify-content: center;
    padding-top: 1rem;
    & h1 {
      text-align: center;
      padding-left: 2rem;
    }
  }
  .info-container {
    flex-direction: row;
    justify-content: space-between;
    & img {
      width: 35%;
    }
  }
  .photos {
    visibility: hidden;
  }
}
@media screen and (max-width: 900px) {
  .home {
    height: calc(100vh - 18rem);
    justify-content: flex-start;
  }
  .title {
    padding-top: 0;
  }
}
@media screen and (max-width: 750px) {
  .info-container {
    padding-top: 5rem;
  }
}
@media screen and (max-width: 600px) {
  .title {
    & h1 {
      padding-left: 8rem;
    }
  }
  .info-container {
    padding-left: 8rem;
    & img {
      width: 50%;
    }
    & h2 {
      padding-left: 3rem;
    }
  }
}
@media screen and (max-width: 500px) {
  h1 {
    padding-right: 15rem;
    width: 120%;
    font-size: 7rem;
  }
  .home {
    height: 100vh;
  }
  .info-container {
    flex-direction: column;
    padding-right: 8rem;
    & img {
      margin-top: 0;
      margin-bottom: 1rem;
      width: 60%;
    }
    & h2 {
      padding-right: 4rem;
      padding-top: 2rem;
      width: 100%;
    }
  }
  .title {
    & h1 {
      padding-left: 15rem;
    }
  }
}
@media screen and (max-height: 700px) {
  .info-container {
    & h2 {
      padding-top: 2rem;
      font-size: 2rem;
    }
  }
}
</style>
