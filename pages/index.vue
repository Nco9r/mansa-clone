<template>
  <div class="container">
    <hero/>
    <explication/>
    <avis/>
    <concept/>
    <presse/>
    <team/>
    <regles/>
    <faq/>

  </div>
</template>

<script>
import Hero from '../components/features/Hero'
import Explication from '../components/features/Explication'
import Avis from '../components/features/Avis'
import Concept from '../components/features/Concept'
import Presse from '../components/features/Presse'
import Team from '../components/features/Team'
import Regles from '../components/features/Regles'
import Faq from '../components/features/Faq'

export default {
  components: {
    Hero,
    Explication,
    Avis,
    Concept,
    Presse,
    Team,
    Regles,
    Faq,
  }
}
</script>

<style>

.container {
  padding: 0 20px;
}

@media screen and (min-width: 1200px) {
  .container {
    padding: 0px 50px;
  }
}

@media screen and (min-width: 1640px) {
  .container {
    padding: 0px 350px;
  }
}



</style>
