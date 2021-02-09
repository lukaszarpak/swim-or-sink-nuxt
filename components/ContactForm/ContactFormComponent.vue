<template>
  <div class='col-10 col-md-5 mx-auto'>
    <form action='https://formspree.io/xzbejqgr' method='POST'>
      <label style='margin-top: 20px'>
        <span>Imię i nazwisko</span>
        <input type='text' class='name' name='Imię i nazwisko' />
      </label>
      <label>
        <span>E-mail</span>
        <input type='email' class='email' name='Email' />
      </label>
      <label>
        <span>Telefon</span>
        <input type='number' class='phone' name='Telefon' />
      </label>
      <div class='status'></div>
      <button type='submit' @click='submitForm'>Wyślij</button>
    </form>
  </div>
</template>
<script>
export default {
  methods: {
    submitForm (e) {
      const name = document.querySelector('.name').value
      const email = document.querySelector('.email').value
      const phone = document.querySelector('.phone').value
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
    span {
      display: block;
      margin: 10px 0 5px;
      font-weight: 700;
      color: #2d3681;
      letter-spacing: 1px;
    }
    input {
      width: 260px;
      border: none;
      border-radius: 30px;
      background-color: #0b70b8;
      padding: 10px 30px;
      color: #fff;
      letter-spacing: 1px;
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
    margin: 40px auto 0px;
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
