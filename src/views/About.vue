<template>
  <div class="about">
    <div class="title">
      <h1>About Me</h1>
    </div>
    <div class="content">
      <img src="../assets/images/kelly-working.jpg" alt="kelly-working" />
      <p>
        Clothing alterations can make a huge difference in your appearance and even minor alterations can make a huge impact. I have been sewing for
        20 years as a hobby and turned my passion into a career 8 years ago. I can alter clothing for men, women and children and have completed a
        wide variety of projects. Creativity is my strength so I can take your loved ones clothing and make memory bears and memory pillows, as well
        as memory t-shirts, quilts or blankets. I am open Tuesday- Saturday and book by appointment only.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
};
</script>

<style lang="scss" scoped>
.about {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  background: #fcecdd;
  height: calc(100vh - 20rem);

  & h1 {
    font-size: 6rem;
  }
}

.content {
  display: flex;
  justify-content: space-evenly;
  padding: 10rem;

  & img {
    width: 30%;
    border-radius: 10px;
    -webkit-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
    box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
  }

  & p {
    width: 50%;
    font-size: 3rem;
  }
}
@media screen and (max-width: 1920px) {
  .about {
    & h1 {
      padding-top: 5rem;
    }
  }
  .content {
    & p {
      font-size: 2.5rem;
    }
  }
}
@media screen and (max-width: 1700px) {
  .content {
    padding: 5rem;
  }
}

@media screen and (max-width: 1500px) {
  .content {
    & p {
      font-size: 2.25rem;
    }
  }
}
@media screen and (max-width: 1300px) {
  .about {
    & h1 {
      font-size: 5rem;
    }
  }
  .content {
    padding-top: 2rem;
    & p {
      font-size: 2rem;
    }
  }
}
@media screen and (max-width: 1200px) {
  .about {
    & h1 {
      padding-top: 0;
    }
  }
  .content {
    & img {
      width: 40%;
    }
    & p {
      width: 40%;
    }
  }
}
@media screen and (max-width: 1000px) {
  .content {
    flex-direction: column;
    align-items: center;
    & img {
      width: 50%;
    }
    & p {
      width: 80%;
      padding-top: 5rem;
    }
  }
}
@media screen and (max-width: 900px) {
  .content {
    & img {
      width: 60%;
    }
    & p {
      font-size: 1.75rem;
    }
  }
}
@media screen and (max-width: 750px) {
  .about {
    padding: 5rem 0 5rem 5rem;
  }
}
@media screen and (max-width: 600px) {
  .about {
    padding: 5rem 0 5rem 10rem;
  }
  .content {
    & img {
      width: 90%;
    }
    & p {
      width: 125%;
    }
  }
}
@media screen and (max-width: 500px) {
  .content {
    & img {
      width: 140%;
    }
    & p {
      width: 170%;
    }
  }
}
@media screen and (max-width: 400px) {
  .content {
    & img {
      width: 180%;
    }
    & p {
      width: 180%;
    }
  }
}
@media screen and (max-height: 700px) {
  .about {
    padding: 10rem 0 10rem 15rem;
    & h1 {
      font-size: 3.5rem;
    }
  }
  .content {
    & img {
      width: 300%;
    }
    & p {
      font-size: 1.75rem;
      width: 350%;
    }
  }
}
@media screen and (max-height: 600px) {
  .about {
    padding: 10rem 0 10rem 15rem;
    & h1 {
      font-size: 3.5rem;
    }
  }
  .content {
    & img {
      width: 350%;
    }
    & p {
      font-size: 1.5rem;
      width: 400%;
    }
  }
}
</style>
