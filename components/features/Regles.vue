<template>
  <div class="regles">
      <h2>Mansa est une société règlementée</h2>
      <p>Mansa est une entreprise française régulée auprès de l’Orias sous le numéro 19008106.</p>
      <div class="regles_img">
          <img src="@/assets/img/svg/orias.png" alt="">
        <img src="@/assets/img/svg/acpr.png" alt="">
      </div>
      
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
    .regles {
        margin-top: 250px;
        background-color: #EFEDF9;
        display: flex;
        flex-flow: column; 
        padding: 40px 30px;
        margin: auto;
        text-align: center;
        margin-bottom: 100px;
    }

     .regles h2 {
         font-size: 32px; 
         color: var(--violet);
         font-weight: 700;
         line-height: 32px;
         margin-bottom: 30px;
     }

      .regles p {
         line-height: 20px;
         margin-bottom: 30px;
     }

     .regles_img {
         display: flex; 
         flex-flow: row;
         justify-content: center;
         align-items: center; 
     }

      .regles_img img {
         width: 100px;
    }

@media screen and (min-width: 1024px) {
    .regles {
        padding: 40px 330px;
    }
}

@media screen and (min-width: 1440px) { 
    .regles {
        max-width: 1440px;
        margin: 50px auto; 
    }
}


</style>