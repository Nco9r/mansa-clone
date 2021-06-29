<template>
  <div class="faq">
      <div class="title_faq">
          <h2>Les questions les plus fréquentes</h2>
          <p>Nous sommes également joignables au 09 70 70 03 78 ou via la bulle de contact</p>
      </div>
      <div class="content_faq">
          <div class="title_content">
              <div class="title">
                  <h4 :class="{ violet: open }">Comment faire ma demande de prêt en ligne ?</h4>
              </div>
              <div class="open" @click="open = !open">
                 <svg :class="{ rotate: open }" width="100%" height="100%" viewBox="0 0 32 34" fill="" xmlns="http://www.w3.org/2000/svg"><path :class="{ color: open }" d="M18.982 13.6321H32V19.2453H18.982V34H13.018V19.2453H0V13.6321H13.018V0H18.982V13.6321Z" fill="#D9D9D9"></path></svg>
              </div>
          </div>
          <div class="content" v-if="open">
              <p>Inscrivez vous sur getmansa.com et suivez les étapes sur votre espace. Il vous suffit de connecter votre compte bancaire de manière entièrement sécurisée et de répondre à quelques questions sur votre entreprise. L’inscription prend 10 minutes et vous obtenez une réponse définitive en 48h.</p>
          </div>
          <hr>
      </div>

      <div class="content_faq">
          <div class="title_content">
              <div class="title">
                  <h4 :class="{ violet: open_1 }">Quel est le taux d’intérêt ?</h4>
              </div>
              <div class="open" @click="open_1 = !open_1">
                  <svg :class="{ rotate: open_1 }" width="100%" height="100%" viewBox="0 0 32 34" fill="" xmlns="http://www.w3.org/2000/svg"><path :class="{ color: open_1 }" d="M18.982 13.6321H32V19.2453H18.982V34H13.018V19.2453H0V13.6321H13.018V0H18.982V13.6321Z" fill="#D9D9D9"></path></svg>
              </div>
          </div>
          <div class="content" v-if="open_1">
              <p>Le taux d’intérêt d’un prêt Mansa se situe entre 2 et 8% selon votre profil</p>
          </div>
          <hr>
      </div>

      <div class="content_faq">
          <div class="title_content">
              <div class="title" >
                  <h4 :class="{ violet: open_2 }">Quelles sont les conditions d’éligibilité pour un prêt Mansa ?</h4>
              </div>
              <div class="open" @click="open_2 = !open_2">
                  <svg :class="{ rotate: open_2 }" width="100%" height="100%" viewBox="0 0 32 34" fill="" xmlns="http://www.w3.org/2000/svg"><path :class="{ color: open_2 }" d="M18.982 13.6321H32V19.2453H18.982V34H13.018V19.2453H0V13.6321H13.018V0H18.982V13.6321Z" fill="#D9D9D9"></path></svg>
              </div>
          </div>
          <div class="content" v-if="open_2">
              <p>Les conditions minimales pour être éligible à un prêt Mansa sont un revenu moyen supérieur à 1500€ par mois ainsi qu’un numéro de Siren depuis plus d’1 an. L'éligibilité du dossier est ensuite évaluée par nos outils d'analyse de crédit.</p>
          </div>
          <hr>
      </div>


      <div class="content_faq">
          <div class="title_content">
              <div class="title">
                  <h4 :class="{ violet: open_3 }">Puis-je utiliser mon crédit pour des besoins personnels ?</h4>
              </div>
              <div class="open" @click="open_3 = !open_3">
                  <svg :class="{ rotate: open_3 }" width="100%" height="100%" viewBox="0 0 32 34" fill="" xmlns="http://www.w3.org/2000/svg"><path :class="{ color: open_3 }" d="M18.982 13.6321H32V19.2453H18.982V34H13.018V19.2453H0V13.6321H13.018V0H18.982V13.6321Z" fill="#D9D9D9"></path></svg>
              </div>
          </div>
          <div class="content" v-if="open_3">
              <p>Mansa dispose à la fois d’une offre de prêt professionnel mais aussi d’une offre de crédit personnel. Vous pouvez donc choisir cette offre et réaliser tous vos projets personnels avec nous </p>
          </div>
          <hr>
      </div>


      <div class="content_faq">
          <div class="title_content">
              <div class="title">
                  <h4 :class="{ violet: open_4 }">Puis-je rembourser sur plus de 12 mois ?</h4>
              </div>
              <div class="open" @click="open_4 = !open_4">
                  <svg :class="{ rotate: open_4 }" width="100%" height="100%" viewBox="0 0 32 34" fill="" xmlns="http://www.w3.org/2000/svg"><path :class="{ color: open_4 }" d="M18.982 13.6321H32V19.2453H18.982V34H13.018V19.2453H0V13.6321H13.018V0H18.982V13.6321Z" fill="#D9D9D9"></path></svg>
              </div>
          </div>
          <div class="content" v-if="open_4">
              <p>12 mois est le maximum que nous puissions proposer pour l’instant mais nous avons comme projet d’augmenter le nombre de mensualités d’ici fin 2020 🚀</p>
          </div>
          <hr>
      </div>

       <div class="content_faq">
          <div class="title_content">
              <div class="title">
                  <h4 :class="{ violet: open_5 }">Puis-je tout rembourser d'un coup ? (remboursement par anticipation)</h4>
              </div>
              <div class="open" @click="open_5 = !open_5">
                  <svg :class="{ rotate: open_5 }" width="100%" height="100%" viewBox="0 0 32 34" fill="" xmlns="http://www.w3.org/2000/svg"><path :class="{ color: open_5 }" d="M18.982 13.6321H32V19.2453H18.982V34H13.018V19.2453H0V13.6321H13.018V0H18.982V13.6321Z" fill="#D9D9D9"></path></svg>
              </div>
          </div>
          <div class="content" v-if="open_5">
              <p>Oui. Il suffit de nous le notifier et il n'y a pas de frais supplémentaires.</p>
          </div>
          <hr>
      </div>
      <div class="lien">
      <nuxt-link to='/'>Voir tous les questions</nuxt-link>
      </div>


  </div>
</template>

<script>
export default {
    data() {
        return {
            open: false,
            open_1: false,
            open_2: false,
            open_3: false, 
            open_4: false, 
            open_5: false, 
        }
    }
}
</script>

<style scoped>

.title_faq {
    text-align: center;
    padding: 0 30px;
    margin-bottom: 50px;
}

.title_faq h2{
    font-size: 32px;
    font-weight: 700;
    line-height: 32px;
    margin-bottom: 10px;

}

.title_faq p {
    color: var(--violet);
    line-height: 20px;
}

.title_content {
    display: flex; 
    flex-flow: row; 
    justify-content: space-between; 
    align-items: flex-start;
    padding: 20px 11px 20px 10px; 
}

.title {
    width: 80%; 
}

.title h4 {
    font-weight: bold; 
    font-size: 20px;
}

.violet {
    color: var(--violet);
}

.open {
    width: 20%;
    display: flex; 
    justify-content: flex-end;
    cursor: pointer;

}

.open svg {
    width: 20%;
    fill: none; 
    transition: all .4s ease 0s;  
    
}

.rotate {
    transform: rotate(45deg);
    fill: red; 
}

.color {
    fill: red; 
}

.content p {
    padding: 0 50px 30px 10px;
    line-height: 20px;
}

hr {
    border: none; 
    height: 1px;
    width: 100%;
    background-color: rgb(208, 208, 208);
}

.lien {
    margin-top: 40px;
    margin-bottom: 50px;
    text-align: center;
   
    
}

a {
    color: var(--violet);
    font-weight: 700; 
    text-decoration: none;
    text-align: center;
}

@media screen and (min-width: 768px) {
    .open svg {
    width: 8%;
    fill: none; 
    transition: all .4s ease 0s;  
    } 
}
@media screen and (min-width: 1024px) {
    .open svg {
    width: 5%;
    fill: none; 
    transition: all .4s ease 0s;  
    }   

    .lien {
    margin-top: 40px;
    margin-bottom: 150px;
    text-align: left;
    }  
}

@media screen and (min-width: 1440px) { 
    .faq {
        max-width: 1440px;
        margin: 50px auto; 
    }
}

</style>