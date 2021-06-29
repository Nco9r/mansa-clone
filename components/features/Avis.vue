<template>
  <div class="avis">
      <div class="title_avis">
          <h2>Plus de 2000 indépendants ont déjà fait confiance à Mansa</h2>
          <p>Un service apprécié par les indépendants</p>
      </div>
      <div class="box">
          <div class="items_box">
              <p class="content_box">Excellente expérience crédit pour ma société. Un onboarding en quelques minutes. Une vérification des éléments financiers et le prêt accordé dans la foulée. Les fonds étaient sur le compte bancaire en 24h.</p>
              <div class="auteur">
                  <div class="name">
                      <p>A</p>
                  </div>
                  <div class="profession">
                      <p><strong>Arnaud G</strong></p>
                      <p class="pro">Entrepreneur</p>
                  </div>
              </div>
          </div>
          <div class="items_box">
              <p class="content_box">Je suis indépendant depuis 1 an et ce service est vraiment génial. On s'inscrit et Mansa appelle dans la journée, le dossier prend 10 minutes à faire en ligne et on a la réponse définitive en 24h.</p>
              <div class="auteur">
                  <div class="name">
                      <p>A</p>
                  </div>
                  <div class="profession">
                      <p><strong>Guillaume S</strong></p>
                      <p class="pro">Développeur web</p>
                  </div>
              </div>
          </div>
          <div class="items_box">
              <p class="content_box">Service pratique et équipe disponible. Un prêt qui m’a permis de renouveler mon matériel informatique.</p>
              <div class="auteur">
                  <div class="name">
                      <p>A</p>
                  </div>
                  <div class="profession">
                      <p><strong>Frédéric V</strong></p>
                      <p class="pro">Expert SEO</p>
                  </div>
              </div>
          </div>
      </div>
      <nuxt-link to='/'>Voir tous les avis</nuxt-link>

  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.avis {
    text-align: center;
    margin-top: 70px
}

.title_avis h2 {
    font-size: 32px;
    font-weight: 700;
    line-height: 32px;
    margin-bottom: 10px;
}

.title_avis p {
    color: var(--violet);
}

.box {
    display: flex; 
    flex-flow: row wrap; 
    justify-content: space-between; 
    align-items: center; 
    margin-top: 20px;
}

.items_box {
    text-align: left; 
    padding: 15px 25px;
    background-color: var(--white);
    box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 30px;
    margin-bottom: 15px;
    border-radius: 8px;
    width: 100%;
}

.items_box p {
    font-size: 14px;
    line-height: 18px;
}

.auteur {
    margin-top: 30px;
    margin-left: 5px;
    display: flex; 
    flex-flow: row wrap; 
}

.name p {
    width: 40px;
    height: 40px;
    background-color: rgb(100, 73, 209);
    color: rgb(250, 250, 250);
    border-radius: 50%;
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    align-items: center;
}

.profession {
    margin-left: 15px;
}

.pro {
    color: var(--violet);
}

a {
    text-decoration: none; 
    font-weight: 700; 
    margin-top: 10px;
    color: var(--violet);

}

@media screen and (min-width: 768px) { 
    .items_box {
        width: 49%;
        height: 180px;
    }

    .items_box .content_box{
        height: 80px;
    }
}

@media screen and (min-width: 1024px) {

    .avis {
        margin-top: 200px;
    }

    .box {
        margin-top: 50px;
    }
    .items_box {
        width: 32%;
        height: 190px;
    }

    .items_box .content_box{
        height: 110px;
    }

    .auteur {
        margin-top: 15px;
    }
}

@media screen and (min-width: 1440px) { 
    .avis {
        max-width: 1440px;
        margin: 50px auto; 
    }
}

</style>