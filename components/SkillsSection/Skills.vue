<template>
  <div class="wrap">
    <h2>Nasze specjalności</h2>
    <p>Zajęcia w naszej szkole pływania prowadzimy w trzech grupach zaawansowania. Na bieżąco tworzymy nowe grupy i staramy się dobierać grupy tak, aby efekty naszej i Waszej pracy były jak najbardziej satysfakcjonujące. W zależności od liczebności oraz poziomu zaawansowania grupy zajęcia prowadzone są przez jednego lub dwóch trenerów, zarówno bezpośrednio z wody, jak i z lądu.</p>
    <div class="container mx-auto">
      <div class="row">
        <Skill
          :skillimg="skillimg1"
          :text-on-skill="textOnSkill1"
          :text-on-skill-bottom="textOnSkillBottom1"
        />
        <Skill
          :skillimg="skillimg2"
          :text-on-skill="textOnSkill2"
          :text-on-skill-bottom="textOnSkillBottom2"
        />
        <Skill
          :skillimg="skillimg3"
          :text-on-skill="textOnSkill3"
          :text-on-skill-bottom="textOnSkillBottom3"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Skill from './Skill.vue'
export default {
  name: 'Skills',
  components: {
    Skill
  },
  data () {
    return {
      skillimg1: require('../../assets/skill1.png'),
      skillimg2: require('../../assets/skill2.png'),
      skillimg3: require('../../assets/skill3.png'),
      textOnSkill1: 'Grupa początkująca',
      textOnSkill2: 'Grupa średniozaawansowana',
      textOnSkill3: 'Grupa zaawansowana',
      textOnSkillBottom1:
        'Nauka pływania od podstaw, oswajanie z wodą poprzez zróżnicowane ćwiczenia, gry i zabawy, nauka prawidłowego oddechu, nurkowania, pracy nóg oraz podstawowych elementów technicznych. a także nauka podstawowych zasad bezpieczeństwa i zachowania nad wodą. Zajęcia odbywają się na ,,małym,, basenie.',
      textOnSkillBottom2:
        'Nauka elementów technicznych pływania kraulem, grzbietem i żabą. Nauka pływania bez sprzętu pomocniczego (deska, makaron). Grupa idealna dla dzieci, które potrafią pływać z deską, znają prawidłową pracę nóg do kraula, oswojonych z wodą. Zajęcia odbywają się na ,,dużym’’ basenie. ',
      textOnSkillBottom3:
        'Nauka pływania sportowego wszystkimi stylami pływackimi. Poznawanie elementów technicznych: nawrotów i skoków. Przeznaczona dla osób, które potrafią pływać minimum trzema stylami i czują się jak ,,ryba’’ w wodzie, a także dla osób chcących doskonalić technikę oraz zainteresowanych wstąpieniem do sekcji pływackiej. '
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  background: linear-gradient(
    180deg,
    rgba(16, 44, 79, 1) 0%,
    rgba(33, 75, 124, 1) 80%
  );
  text-align: center;
  color: #fff;
  padding: 100px 0;
  > h2 {
    margin-bottom: 30px;
  }
  > p {
    width: 80%;
    max-width: 600px;
    margin: 0 auto 50px;
    text-align: justify;
  }
}
</style>
