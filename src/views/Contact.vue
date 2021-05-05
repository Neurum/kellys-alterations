<template>
  <div class="contact-section">
    <div class="row">
      <div class="contact">
        <div class="contact-form">
          <form id="fs-frm" class="form" name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/f/xeqvejnb" method="post">
            <h2>Book now and see what I can do for you!</h2>
            <fieldset class="form-group">
              <input type="text" name="name" id="name" class="form__input" placeholder="Full Name" autocomplete="off" required />
              <label for="name" class="form__label">Full Name</label>
              <input type="email" name="_replyto" class="form__input" id="email-address" placeholder="Email" autocomplete="off" required />
              <label for="email-address" class="form__label">Email Address</label>
              <textarea rows="5" name="message" id="message" class="form__textarea" placeholder="Message" autocomplete="off" required></textarea>
              <label for="message" class="form__label">Message</label>
              <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission" />
            </fieldset>
            <input type="submit" value="Submit" class="form-submit" />
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
};
</script>

<style lang="scss" scoped>
.contact-section {
  height: calc(100vh - 20rem);
}

.row {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 5rem;
}

.contact {
  width: 61.9%;
  height: 60rem;
  background-image: linear-gradient(105deg, rgba(255, 255, 255, 0.9) 0%, rgba(255, 255, 255, 0.9) 50%, transparent 50.1%),
    url(../assets/images/office.jpg);
  background-size: contain;
  border-radius: 10px;
  -webkit-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);
  box-shadow: 1px 8px 24px 3px rgba(0, 0, 0, 0.75);

  &-form {
    width: 50%;
    padding: 3rem 6rem;
  }
}
h2 {
  font-size: 3rem;
  padding-bottom: 3rem;
  padding-top: 5rem;
  color: #2f2f2f;
}
fieldset {
  display: flex;
  flex-direction: column;
  border: none;
}
.form {
  display: flex;
  flex-direction: column;

  &-submit {
    font-family: 'Nunito', sans-serif;
    font-size: 1.5rem;
    border: none;
    background-color: #2f2f2f;
    color: #fcecdd;
    width: 67%;
    border-radius: 5px;
  }
  &-group {
    width: 100%;
    margin-bottom: 2rem;
  }

  &__input {
    font-family: 'Nunito', sans-serif;
    font-size: 1.5rem;
    padding: 1.5rem 2rem;
    border-radius: 5px;
    width: 60%;
    background-color: rgba(255, 255, 255, 0.9);
    border: none;
    color: #2f2f2f;
    border-bottom: 3px solid transparent;

    &:focus {
      outline: none;
      box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.3);
      border-bottom: 3px solid #2f2f2f;

      &:invalid {
        border-bottom: 3px solid red;
      }
    }
  }

  &__input:placeholder-shown + &__label {
    opacity: 0;
    visibility: hidden;
    transform: translateY(-4rem);
  }

  &__textarea:placeholder-shown + &__label {
    opacity: 0;
    visibility: hidden;
    transform: translateY(-4rem);
  }

  &__label {
    padding-bottom: 2rem;
    font-size: 1.2rem;
    font-weight: bold;
    margin-left: 2rem;
    margin-top: 0.7rem;
    transition: all 0.3s;
  }

  &__textarea {
    font-family: 'Nunito', sans-serif;

    font-size: 1.5rem;
    padding: 1.5rem 2rem;
    border-radius: 5px;
    width: 60%;
    background-color: rgba(255, 255, 255, 0.9);
    border: none;
    border-bottom: 3px solid transparent;
    resize: none;

    &:focus {
      outline: none;
      box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.3);
      border-bottom: 3px solid #2f2f2f;
    }
  }
}
@media screen and (max-width: 1800px) {
  .contact {
    background-image: linear-gradient(105deg, rgba(255, 255, 255, 0.9) 0%, rgba(255, 255, 255, 0.9) 70%, transparent 50.1%),
      url(../assets/images/office.jpg);

    &-form {
      width: 70%;
    }
  }
}
@media screen and (max-width: 1275px) {
  .contact {
    height: 80rem;
    background-size: cover;
  }
}
@media screen and (max-width: 1200px) {
  .contact {
    width: 95%;
    &-section {
      padding-bottom: 30rem;
    }
  }
}
</style>
