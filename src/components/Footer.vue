<template>
  <div class="footer">
    <div class="socials">
      <a href="https://www.facebook.com/kellysalterations/"><i class="fab fa-facebook-f"></i></a>
      <a href="https://www.instagram.com/kellys.alterations"><i class="fab fa-instagram"></i></a>
      <!-- <a href="https://www.yelp.com"><i class="fab fa-yelp"></i></a> -->
    </div>
    <div>
      <p>&copy; Copyright Kelly's Alterations 2021</p>
    </div>
  </div>
  <!-- <div class="contact-modal">
    <div class="modal">
      <p>Contact</p>
    </div>
    <div class="contact-link">
      <p>Book Now</p>
    </div>
  </div> -->
</template>

<style lang="scss" scoped>
.footer {
  padding-top: 2rem;
  font-size: 3rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  height: 8rem;
}
.socials {
  color: #2f2f2f;
  margin: 0 auto;
  display: flex;
  justify-content: space-evenly;
  width: 15%;

  & a {
    font-size: 3rem;
    cursor: pointer;
    text-decoration: none;
    color: inherit;
    font-family: inherit;
  }
}

.contact-modal {
  position: relative;
}

.modal {
  position: absolute;
  display: flex;
  justify-content: center;
  right: 11%;
  bottom: -2rem;
  width: 20rem;
  height: 13rem;
  background-color: #2f2f2f;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;

  & p {
    font-size: 2rem;
    color: #fcecdd;
    padding-top: 1rem;
  }
}
@media screen and (max-width: 900px) {
  .footer {
    padding-left: 3rem;
  }
  .socials {
    width: 25%;
  }
}
@media screen and (max-width: 750px) {
  .footer {
    padding-left: 6rem;
  }
  .socials {
    width: 35%;
  }
}
@media screen and (max-width: 600px) {
  .footer {
    padding-left: 8rem;
    padding-top: 6rem;
  }
}
@media screen and (max-width: 500px) {
  .footer {
    padding-left: 12rem;
    padding-top: 5rem;
  }
  .socials {
    width: 40%;
  }
}
</style>
