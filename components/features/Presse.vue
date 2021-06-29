<template>
  <div class="presse">
      <div class="title_presse">
          <h2>La presse parle de Mansa</h2>
          <p>Efficacité, sécurité et rapidité</p>
      </div>
      <div class="content_presse">
          <div class="img_presse">
              <img src="@/assets/img/svg/presse.svg" alt="">
          </div>
          <div class="description_presse">
              <div class="text_presse">
                  <p class="quote">La promesse est une expérience utilisateur adaptée à cette nouvelle génération de travailleurs indépendants, extrêmement fluide, avec une réponse quasi instantanée et l'envoi des fonds en 24h.</p>
                  <p class="echos"><strong>Les Echos</strong></p>
              </div>
              <div class="logo_presse">
                  <img src="@/assets/img/svg/echos.svg" alt="">
                  <img src="@/assets/img/svg/tribune.svg" alt="">
                  <img src="@/assets/img/svg/bfm.svg" alt="">
              </div>
          </div>
      </div>

  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.presse {
    text-align: center; 
    margin-top: 120px;
}

.title_presse h2 {
    font-size: 32px;
    font-weight: 700;
    line-height: 32px;
    margin-bottom: 10px;
}

.title_presse p {
    color: var(--violet);
}

.content_presse {
    display: flex; 
    flex-flow: row wrap;
    margin-top: 50px; 

}

.img_presse {
    margin-bottom: 50px;
}

.img_presse img{
    width: 80%;
}

.description_presse {
    text-align: left;
}

.text_presse .quote {
    line-height: 18px;
    margin-bottom: 20px;
}

.text_presse .quote::before {
    content: "“";
    margin-right: 0.25em;
    font-size: 3em;
    font-weight: bold;
    color: rgb(100, 73, 209);
}

.text_presse .echos {
    text-align: center; 
    font-size: 18px;
}

.logo_presse {
    margin-top: 30px;
    display: flex; 
    justify-content: space-around;
}

@media screen and (min-width: 768px) {
    .content_presse {
    display: flex; 
    flex-flow: column;
    margin-top: 50px; 
    align-content: center;
    }  
    .content_presse img {
        width: 20%;
    } 
    .img_presse img{
    width: 55%;
}
}

@media screen and (min-width: 1024px) {

    .content_presse {
        flex-flow: row-reverse;
        align-items: center;
    }
    .img_presse {
        width: 50%;
        display: flex; 
        justify-content: flex-end;
    }

    .img_presse img {
        width: 60%;
    }

    .description_presse {
        width: 50%;
    }

    .text_presse .echos {
        text-align: left; 
        font-size: 18px;
    }   
}

@media screen and (min-width: 1440px) { 
    .presse {
        max-width: 1440px;
        margin: 50px auto; 
    }
}



</style>