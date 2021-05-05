<template>
  <div class="gallery">
    <figure class="gallery__item gallery__item--1" @click.prevent="lightbox">
      <img src="../assets/images/gallery-1.jpg" alt="gallery image 1" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--2" @click.prevent="lightbox">
      <img src="../assets/images/gallery-2.jpg" alt="gallery image 2" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--3" @click.prevent="lightbox">
      <img src="../assets/images/gallery-3.jpg" alt="gallery image 3" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--4" @click.prevent="lightbox">
      <img src="../assets/images/gallery-4.jpg" alt="gallery image 4" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--5" @click.prevent="lightbox">
      <img src="../assets/images/gallery-5.jpg" alt="gallery image 5" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--6" @click.prevent="lightbox">
      <img src="../assets/images/gallery-6.jpg" alt="gallery image 6" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--7" @click.prevent="lightbox">
      <img src="../assets/images/gallery-7.jpg" alt="gallery image 7" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--8" @click.prevent="lightbox">
      <img src="../assets/images/gallery-8.jpg" alt="gallery image 8" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--9" @click.prevent="lightbox">
      <img src="../assets/images/gallery-9.jpg" alt="gallery image 9" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--10" @click.prevent="lightbox">
      <img src="../assets/images/gallery-10.jpg" alt="gallery image 10" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--11" @click.prevent="lightbox">
      <img src="../assets/images/gallery-11.jpg" alt="gallery image 11" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--12" @click.prevent="lightbox">
      <img src="../assets/images/gallery-12.jpg" alt="gallery image 12" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--13" @click.prevent="lightbox">
      <img src="../assets/images/gallery-13.jpg" alt="gallery image 13" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--14" @click.prevent="lightbox">
      <img src="../assets/images/gallery-14.jpg" alt="gallery image 14" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--15" @click.prevent="lightbox">
      <img src="../assets/images/gallery-15.jpg" alt="gallery image 15" class="gallery__img" />
    </figure>
    <figure class="gallery__item gallery__item--16" @click.prevent="lightbox">
      <img src="../assets/images/gallery-16.jpg" alt="gallery image 16" class="gallery__img" />
    </figure>

    <transition name="zoom" type="animation" appear>
      <div class="lightbox" v-show="clicked" @click="close">
        <div class="photo">
          <img :src="clickedImg" />
          <div class="close">
            <button class="close-icon" @click="close">
              <i class="far fa-times-circle "></i>
            </button>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'Gallery',
  data() {
    return {
      clickedImg: '',
      clicked: false,
    };
  },
  methods: {
    lightbox(e) {
      this.clickedImg = e.target.src;
      console.log(this.clickedImg);
      this.clicked = true;
    },
    close() {
      this.clicked = false;
    },
  },
};
</script>

<style lang="scss" scoped>
.gallery {
  height: calc(100vh - 22rem);
  display: grid;
  grid-template-columns: repeat(15, 1fr);
  grid-template-rows: repeat(12, 5.58vh);
  grid-gap: 1rem;
  padding: 1rem;

  &__item {
    &--1 {
      grid-row: 1 / span 6;
      grid-column: 1 / span 3;
    }
    &--2 {
      grid-row: 6 / span 7;
      grid-column: 7 / span 4;
    }
    &--3 {
      grid-row: 1 / span 7;
      grid-column: 4 / span 3;
    }
    &--4 {
      grid-row: 1 / span 5;
      grid-column: 7 / span 3;
    }
    &--5 {
      grid-row: 1 / span 5;
      grid-column: 10 / span 2;
    }
    &--6 {
      grid-row: 7 / span 6;
      grid-column: 1 / span 3;
    }
    &--7 {
      grid-row: 6 / span 4;
      grid-column: 11 / span 2;
    }
    &--8 {
      grid-row: 1 / span 5;
      grid-column: 12 / span 1;
    }
    &--9 {
      grid-row: 1 / span 5;
      grid-column: 15 / span 1;
    }
    &--10 {
      grid-row: 8 / span 5;
      grid-column: 4 / span 2;
    }
    &--11 {
      grid-row: 6 / span 2;
      grid-column: 15 / span 1;
    }
    &--12 {
      grid-row: 4 / span 4;
      grid-column: 13 / span 2;
    }
    &--13 {
      grid-row: 1 / span 3;
      grid-column: 13 / span 2;
    }
    &--14 {
      grid-row: 10 / span 3;
      grid-column: 11 / span 2;
    }
    &--15 {
      grid-row: 8 / span 5;
      grid-column: 6 / span 1;
    }
    &--16 {
      grid-row: 8 / span 5;
      grid-column: 13 / span 3;
    }
  }

  &__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 10px;
    -webkit-box-shadow: 1px 8px 20px 1px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 1px 8px 20px 1px rgba(0, 0, 0, 0.75);
    box-shadow: 1px 8px 20px 1px rgba(0, 0, 0, 0.75);
  }
}
.lightbox {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  width: calc(100% - 2rem);
  height: calc(100vh - 20rem);
  background-color: rgba(0, 0, 0, 0.8);
  border-radius: 10px;
}
.photo {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50%;

  & img {
    height: 100%;
    border-radius: 10px;
  }
}
.close {
  position: absolute;
  top: 1.2%;
  right: 23.2%;

  & button {
    border: none;
    background: transparent;
    cursor: pointer;
  }
  & svg {
    width: 30px;
    height: 30px;
    color: lightgray;
  }
}

/* Animations */
.zoom-enter-active {
  animation: zoom-in 0.2s;
  transition: all 0.3s;
}
.zoom-leave-active {
  animation: zoom-out 0.2s;
  transition: all 0.3s;
}
.zoom-enter-from {
  transform: scale(0);
}
.zoom-leave-to {
  transform: scale(0);
}
@keyframes zoom-in {
  from {
    transform: scale(0);
  }
  to {
    transform: scale(1);
  }
}
@keyframes zoom-out {
  from {
    transform: scale(1);
  }
  to {
    transform: scale(0);
  }
}
@media screen and (max-width: 1200px) {
  .gallery {
    grid-template-columns: repeat(15, 1fr);
    grid-template-rows: repeat(30, 5.58vh);
    height: 100%;
    width: calc(100vw - 2rem);

    &__item {
      &--1 {
        grid-row: 1 / span 6;
        grid-column: 1 / span 5;
      }
      &--2 {
        grid-row: 13 / span 7;
        grid-column: 1 / span 8;
      }
      &--3 {
        grid-row: 1 / span 7;
        grid-column: 6 / span 5;
      }
      &--4 {
        grid-row: 1 / span 5;
        grid-column: 11 / span 5;
      }
      &--5 {
        grid-row: 20 / span 5;
        grid-column: 1 / span 4;
      }
      &--6 {
        grid-row: 7 / span 6;
        grid-column: 1 / span 5;
      }
      &--7 {
        grid-row: 14 / span 4;
        grid-column: 11 / span 5;
      }
      &--8 {
        grid-row: 13 / span 5;
        grid-column: 9 / span 2;
      }
      &--9 {
        grid-row: 20 / span 5;
        grid-column: 5 / span 4;
      }
      &--10 {
        grid-row: 8 / span 5;
        grid-column: 6 / span 5;
      }
      &--11 {
        grid-row: 23 / span 7;
        grid-column: 13 / span 3;
      }
      &--12 {
        grid-row: 10 / span 4;
        grid-column: 11 / span 5;
      }
      &--13 {
        grid-row: 6 / span 4;
        grid-column: 11 / span 5;
      }
      &--14 {
        grid-row: 25 / span 5;
        grid-column: 1 / span 8;
      }
      &--15 {
        grid-row: 23 / span 7;
        grid-column: 9 / span 4;
      }
      &--16 {
        grid-row: 18 / span 5;
        grid-column: 9 / span 7;
      }
    }
  }
  .lightbox {
    width: 100vw;
    height: 100%;
    position: fixed;
    top: 50%;
    left: 50%;
    border-radius: 0;
    transform: translate(-50%, -50%);
  }
}

@media screen and (max-width: 850px) {
  .gallery {
    width: calc(100vw - 2.5rem);
  }
  .lightbox {
    left: 48.7%;
  }
}
@media screen and (max-width: 775px) {
  .lightbox {
    left: 47.6%;
  }
}
@media screen and (max-width: 420px) {
  .lightbox {
    left: 38.2%;
  }
  .photo {
    width: 90%;
    & img {
      width: 100%;
    }
  }
}
</style>
