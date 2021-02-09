<template>
  <div class="wrap">
    <h2>Nasi Trenerzy</h2>
    <div class="container mx-auto">
      <div class="row wrapper">
        <Trainer
          :trainer-photo="trainerPhoto1"
          :trainer-name="trainerName1"
          :trainer-description="trainerDescription1"
        />
        <Trainer
          :trainer-photo="trainerPhoto2"
          :trainer-name="trainerName2"
          :trainer-description="trainerDescription2"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Trainer from './Trainer.vue'
export default {
  components: {
    Trainer
  },
  data: () => ({
    trainerPhoto1: require('../../assets/KubaSOS.jpg'),
    trainerPhoto2: require('../../assets/KamilSOS.jpg'),
    trainerName1: 'Jakub Sobala',
    trainerName2: 'Kamil Szulik',
    trainerDescription1:
      'Instruktor Pływania od roku 2015, trener sekcji pływackiej MKS Piaseczno od roku 2017, ratownik WOPR. Były zawodnik sekcji pływackiej GOSiR Piaseczno. Wielokrotny medalista mistrzostw Polski w pływaniu w tym mistrz Polski, dzieci  10-11 letnich na dystansach 50, 100 metrów stylem klasycznym. Były reprezentant klubu piłki wodnej UKPW 44 Warszawa (obecnie Legia Warszawa), z którym zdobył dwukrotnie srebrny medal mistrzostw Polski juniorów. Poza basenem wielokrotny mistrz Polski w Kick-boxingu juniorów. ',
    trainerDescription2:
      'Absolwent Akademii Wychowania Fizycznego i Wyższej Szkoły Edukacji w Sporcie w Warszawie. Trener pływania klasy II PZP, pracujący od 2013 roku w klubie pływackim MKS Piaseczno. W przeszłości przez 8 lat trenował pływanie. Od 10-ciu lat pracuje jako instruktor pływania, doświadczenie w nauczaniu zdobywał w licznych szkółkach pływania oraz prowadząc indywidualne zajęcia.'
  })
}
</script>

<style lang="scss" scoped>
.wrap {
  background: rgba(16, 44, 79, 1);
  text-align: center;
  color: #fff;
  padding: 100px 0 0 0;
  > h2 {
    margin-bottom: 30px;
  }
  > p {
    width: 80%;
    max-width: 600px;
    margin: 0 auto 30px;
    text-align: justify;
  }
}
.wrapper {
  margin-top: 80px;
}
</style>
