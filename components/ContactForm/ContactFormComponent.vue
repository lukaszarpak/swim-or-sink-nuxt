<template>
  <div class="col-10 col-md-5 mx-auto">
    <form action="https://formspree.io/xzbejqgr" method="POST">
      <label style="margin-top: 20px">
        <span>Imię i nazwisko</span>
        <input type="text" class="name" name="Imię i nazwisko">
      </label>
      <label>
        <span>E-mail</span>
        <input type="text" class="email" name="Email">
      </label>
      <label>
        <span>Telefon</span>
        <input type="number" class="phone" name="Telefon">
      </label>
      <div class="status" />
      <label class="checkobox">
        <input type="checkbox" name="Zgoda" class="agreement">
        <span class="agree">Wyrażam zgodę na przetwarzanie moich danych osobowych, podanych za pośrednictwem powyższego formularza kontaktowego celem skontaktowania się ze mną. Oświadczam, że zapoznałem(am) się z <nuxt-link to="/dokumenty/klauzula">Klauzulą informacyjną</nuxt-link>.</span>
      </label>
      <button type="submit" @click="submitForm">
        Wyślij
      </button>
    </form>
  </div>
</template>
<script>
export default {
  data: () => ({
    test: 'test1'
  }),
  methods: {
    submitForm (e) {
      const name = document.querySelector('.name').value
      const email = document.querySelector('.email').value
      const phone = document.querySelector('.phone').value
      const agreement = document.querySelector('.agreement').checked
      const status = document.querySelector('.status')

      status.innerHTML = ''

      if (name.length >= 3) {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Imię jest poprawne')
        innerStatus.style.color = 'rgb(41, 173, 48)'
      } else {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Imię jest niepoprawne')
        innerStatus.style.color = 'red'
        e.preventDefault()
      }
      if (email.length >= 5 && email.includes('@') && email.includes('.')) {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Email jest poprawny')
        innerStatus.style.color = 'rgb(41, 173, 48)'
      } else {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Email jest niepoprawny')
        innerStatus.style.color = 'red'
        e.preventDefault()
      }
      if (phone.length >= 8) {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Numer jest poprawny')
        innerStatus.style.color = 'rgb(41, 173, 48)'
      } else {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Numer jest niepoprawny')
        innerStatus.style.color = 'red'
        e.preventDefault()
      }
      if (agreement) {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Zgada jest poprawna')
        innerStatus.style.color = 'rgb(41, 173, 48)'
      } else {
        const innerStatus = document.createElement('div')
        status.append(innerStatus)
        innerStatus.append('Zgada jest wymagna')
        innerStatus.style.color = 'red'
        e.preventDefault()
      }
    }
  }
}
</script>
<style lang='scss' scoped>
form {
  background-color: white;
  color: #000;
  width: 250px;
  border-radius: 30px;
  margin: 5px auto 0;
  label {
    margin: 10px 0 0 30px;

    &.checkobox {
      margin: 15px;
    }

    span {
      display: block;
      margin: 10px 0 5px;
      font-weight: 700;
      color: #2d3681;
      letter-spacing: 1px;

      &.agree {
        display: inline;
        font-weight: 400;
        color: #2d3681;
        letter-spacing: initial;
        font-size: 13px;
      }
    }
    input {
      width: 260px;
      border: none;
      border-radius: 30px;
      background-color: #0b70b8;
      padding: 10px 30px;
      color: #fff;
      letter-spacing: 1px;

      &[type='checkbox'] {
        width: 30px;
      }
    }
    input:focus {
      outline: none;
    }
    input::-webkit-inner-spin-button {
      -webkit-appearance: none;
    }
  }
  button {
    display: block;
    width: 100%;
    height: 45px;
    margin: 20px auto 0px;
    border: none;
    border-radius: 30px;
    color: #fff;
    background-color: #ff0066;
    font-weight: 700;
    letter-spacing: 1px;
    transition: 0.2s;
  }
  button:hover {
    background-color: #ca0353;
  }
  button:focus {
    outline: none;
  }
  .status {
    margin: 20px 0 0 30px;
    font-weight: 600;
  }
}
</style>
