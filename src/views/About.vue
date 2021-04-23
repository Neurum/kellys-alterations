<template>
  <div class="about">
    <div class="title">
      <h1>About Me</h1>
    </div>
    <div class="content">
      <img src="../assets/images/kelly-working.jpg" alt="kelly-working" />
      <p>
        Clothing alterations can make a huge difference in your appearance and
        even minor alterations can make a huge impact. I have been sewing for 20
        years as a hobby and turned my passion into a career 8 years ago. I can
        alter clothing for men, women and children and have completed a wide
        variety of projects. Creativity is my strength so I can take your loved
        ones clothing and make memory bears and memory pillows, as well as
        memory t-shirts, quilts or blankets. I am open Tuesday- Saturday and
        book by appointment only.
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
</style>
