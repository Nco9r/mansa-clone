<template>
  <div class="presse">
      <div class="title_presse">
          <h2>La team Mansa</h2>
      </div>
      <div class="content_presse">
          <div class="img_presse">
              <img src="@/assets/img/svg/team.svg" alt="">
          </div>
          <div class="description_presse">
              <div class="text_presse">
                  <p >Grâce à la confiance de nos clients, nous sommes désormais plus de 20 personnes à Mansa travaillant chaque jour à remplir notre mission : rendre le crédit simple pour les indépendants.</p>
              </div>
          </div>
      </div>
        <div class="lien">
            <nuxt-link to='/'>Découvrir la team Mansa</nuxt-link>
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
    margin-top: 100px;
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
    width: 95%;
}

.description_presse {
    text-align: left;
}

.text_presse p {
    line-height: 20px;
    margin-bottom: 20px;
    display: none;
}

.lien {
    margin-top: 10px;
    margin-bottom: 150px;
    text-align: center;
   
    
}

a {
    color: var(--violet);
    font-weight: 700; 
    text-decoration: none;
    text-align: center;

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
        flex-flow: row;
        align-items: center;
    }
    .img_presse {
        width: 50%;
        display: flex; 
        justify-content: flex-start;
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

    .text_presse p {
    line-height: 20px;
    display: inline;
}
}

@media screen and (min-width: 1440px) { 
    .presse {
        max-width: 1440px;
        margin: 50px auto; 
    }
}



</style>