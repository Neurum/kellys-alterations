<template>
  <div class="star-rating">
    <div class="stars">
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
    </div>
    <div class="star-content">
      <h4>Based on 41 ratings</h4>
    </div>
  </div>
  <div class="testimonials">
    <div class="carousel-view">
      <div class="carousel" tag="div">
        <div class="card" v-for="test in testimonials" :key="test.id" v-show="displayCard === test.id">
          <h3>{{ test.name }}</h3>
          <p>{{ test.testimonial }}</p>
        </div>
      </div>
      <div class="carousel-controls">
        <button class="carousel-controls__button" @click="previous">
          <i class="fas fa-chevron-left"></i>
        </button>

        <button class="carousel-controls__button " @click="next">
          <i class="fas fa-chevron-right"></i>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Testimonials',
  data() {
    return {
      displayCard: 0,
      testimonials: [
        {
          id: 0,
          name: 'Ariel Cherry',
          testimonial: "Very friendly and super quick turn around on a hem for a bridesmaid dress. It's now prefect!",
        },
        {
          id: 1,
          name: 'Bobbie Darnell',
          testimonial:
            'Kelly did an awesome job on transforming my bridesmaid dress into a Modest but stylish dress that I get comfortable in! She was very accommodating to all my needs and requests! I would definitely use her again for any alteration needs! Thank you Kelly!',
        },
        {
          id: 2,
          name: 'Nicole Fox',
          testimonial:
            'It was my first time getting alterations and I couldn’t of asked for a better experience. Bringing my dress in was a fast and easy process, she was able to work with my deadline and finished it before that time anyway!! The dress looks great and it’s just what I needed! Thank you so much!',
        },
        {
          id: 3,
          name: 'Barbara Williams',
          testimonial: 'Best alterations around.  I had a lot of pants that needed hemming and she was able to get them all done in a very timely manner.',
        },
        {
          id: 4,
          name: 'Heather House',
          testimonial:
            'Thank you so much for the alterations to my pants.  I highly recommend her. I have gone to several places in the past that couldn’t get it right. She did a superb job. Quality work, great communication and she will always be my go to for alterations.',
        },
        {
          id: 5,
          name: "Tim O'Briant",
          testimonial:
            'Hey guys and girls,Kelly is great. She replaced a zipper in a old leather gun sleeve for me and replaced a zipper in a 2xxl Carhart jacket .Perfect.  She is so professional.  Give her a call.',
        },
        {
          id: 6,
          name: 'Mary Kimbrough',
          testimonial:
            'Kelly is great. She is a top notch seamstress. From prom dresses, to a simple hem, to a costume from scratch she is very talented, and did I mention sweet and easy going. My daughter and I both love Kelly.',
        },
        {
          id: 7,
          name: 'Veronica Mae Pruitt',
          testimonial:
            "Wonderful woman! She worked with me with my schedule so I could make sure my dress was how I wanted it for my bridal pics. She does amazing work, and gave me a great idea of using material from my dress to make a garter that will be exactly what I want. I can't wait to see my dress when we finish it for my big day!",
        },
        {
          id: 8,
          name: 'Amy Hall',
          testimonial: "Kelly is awesome.  She fixed my dress and made it fit perfect and you could never tell it didn't come that way.",
        },
        {
          id: 9,
          name: 'Samantha Sellers Morris',
          testimonial: 'She literally took my dress apart, pulled the lace and put it back together in no time! My dress fit perfect and was everything I wanted it to be.',
        },
      ],
    };
  },
  methods: {
    next() {
      if (this.displayCard >= 0 && this.displayCard <= this.testimonials.length - 2) {
        this.displayCard++;
      } else {
        this.displayCard = 0;
      }
    },
    previous() {
      if (this.displayCard === 0) {
        this.displayCard = 9;
      } else {
        this.displayCard--;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
h3 {
  font-size: 5rem;
  font-family: 'Dancing Script', cursive;
}
h4 {
  font-size: 2rem;
}
p {
  font-size: 2.5rem;
}
.star-rating {
  padding-top: 3rem;
  padding-bottom: 5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.stars {
  display: flex;
  justify-content: space-evenly;
  color: #2f2f2f;

  & svg {
    width: 3rem;
    height: 3rem;
  }
}
.testimonials {
  display: flex;
  justify-content: center;
  height: calc(100vh - 33.7rem);
  color: #2f2f2f;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  padding: 3rem;
  height: 25rem;
  width: 75rem;
  background-color: white;
  border-radius: 10px;
  -webkit-box-shadow: 1px 8px 24px 1px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 1px 8px 24px 1px rgba(0, 0, 0, 0.75);
  box-shadow: 1px 8px 24px 1px rgba(0, 0, 0, 0.75);
  transform: scale(0.8);

  & h3 {
    text-align: center;
  }

  & p {
    text-align: justify;
  }
}
.carousel {
  width: 85%;
  height: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding-bottom: 3rem;
  transition: all 1s ease-in-out;

  &-view {
    width: 75%;
    height: 75%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  &-controls {
    width: 40%;
    display: flex;
    align-items: center;
    justify-content: space-between;

    &__button {
      width: 2rem;
      height: 4rem;
      border: none;
      background-color: #fcecdd;
      cursor: pointer;
      color: #2f2f2f;

      & svg {
        width: 100%;
        height: 100%;
      }
    }
  }
}
.markers {
  width: 70%;
  display: flex;
  justify-content: center;
  align-items: center;

  & svg {
    width: 1rem;
    height: 1rem;
    padding-left: 1rem;
    padding-right: 1rem;
  }
}
@media screen and (max-width: 850px) {
  h3 {
    font-size: 3.5rem;
  }
  p {
    font-size: 2rem;
  }
}
@media screen and (max-width: 750px) {
  .star-rating,
  .carousel-view {
    padding-left: 7rem;
  }
  .card {
    width: 100%;
  }
  .carousel {
    width: 135%;

    &-controls {
      width: 65%;
    }
  }
}
@media screen and (max-width: 600px) {
  .star-rating,
  .carousel-view {
    padding-left: 10rem;
  }
}
@media screen and (max-width: 450px) {
  .testimonials {
    padding-bottom: 15rem;
  }
  h4 {
    font-size: 1.9rem;
  }
  .star-rating,
  .carousel-view {
    padding-left: 7rem;
    padding-right: 7rem;
  }
  .carousel {
    width: 170%;
    padding-top: 6rem;
    padding-bottom: 10rem;
    &-controls {
      padding-top: 4rem;
    }
    &-view {
      padding-bottom: 5rem;
    }
  }
  .card {
    height: 190%;
  }
}
/* @media screen and (max-height: ); */
</style>
