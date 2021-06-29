<template>
  <div class="explication">
      <div class="items_box">
          <img src="@/assets/img/svg/1.svg" alt="">
          <h4>Des offres transparentes</h4>
          <p>Un taux clair. Aucuns frais cachés. Jamais</p>
      </div>
      <div class="items_box">
        <img src="@/assets/img/svg/2.svg" alt="">
          <h4>Une réponse immédiate</h4>
          <p>Une réponse de principe en 10 minutes et une décision définitive en 48h maximum</p>
      </div>
      <div class="items_box">
            <img src="@/assets/img/svg/3.svg" alt="">
            <h4>Pour tous types de besoin</h4>
            <p>Pour vos besoins pro (trésorerie, investissement, avance de cash) et vos besoins personnels (travaux, véhicule, meubles).</p>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.explication {
    display: flex;
    flex-flow: row wrap; 
    justify-content: space-between; 
    align-items: flex-start; 
    width: 100%; 
    margin-top: 60px;
}

.items_box {
    width: 100%; 
    background-color: var(--white);
    box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 30px;
    margin: 20px 0px;
    border-radius: 8px;
    text-align: center;
    padding: 30px 20px;
}

.items_box img {
    width: 36%;
}

.items_box h4 {
    margin: 20px auto;
}

.items_box p {
    line-height: 20px;
}

@media screen and (min-width: 768px) {

    .explication {
        justify-content: center; 
    }

    .items_box {
        width: 75%;
    }

    .items_box img {
        width: 20%;
    }
   
    
}


@media screen and (min-width: 1024Px) {
    .explication {
        margin-top: 100px;
        justify-content: space-between; 

    }

    .items_box {
        width: 31%;
        height: 330px;
    }


    .items_box img {
        width: 40%;
        height: 100px; 
    }
}

@media screen and (min-width: 1440px) { 
    .explication {
        max-width: 1440px;
        margin: 50px auto; 
    }
}


</style>