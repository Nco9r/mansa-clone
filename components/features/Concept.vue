<template>
  <div class="concept">
      <div class="items_concept">
          <div class="concept_img">
              <img src="@/assets/img/svg/concept_1.svg" alt="">
          </div>
          <div class="content_concept">
              <div class="concept_title">
                  <h2>Une expérience utilisateur fluide et rapide</h2>
              </div>
              <div class="description">
                    <div class="description_content">
                        <p>Notre ambition est de rendre le crédit simple et rapide. L’inscription se fait en ligne, sans paperasse et vous obtenez une réponse de principe en 10 minutes.</p>
                    </div>
                    <div class="icons_content_box">
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_1.svg" alt="">
                        <p class="icons">Vérification de votre identité</p>
                        </div>
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_2.svg" alt="">
                        <p class="icons">Analyse de vos finances</p>
                        </div>
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_3.svg" alt="">
                        <p class="icons">Validation du montant</p>
                        </div>
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_4.svg" alt="">
                        <p class="icons">Signature d'office du contrat</p>
                        </div>
                    </div>
                </div>
                <button>Obtenir mon prêt</button>
            </div>
         </div>



        <div class="items_concept_reverse">
          <div class="concept_img_reverse">
              <img src="@/assets/img/svg/concept_2.svg" alt="">
          </div>
          <div class="content_concept">
              <div class="concept_title">
                  <h2>Un véritable partenaire financier</h2>
              </div>
              <div class="description">
                    <div class="description_content">
                        <p>Mansa finance à la fois vos projets personnels (achat de véhicule, travaux) ainsi que vos projets de développement professionnels (besoin de trésorerie, investissement, achat de matériel).</p>
                    </div>
                    <div class="icons_content_box">
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_5.svg" alt="">
                        <p class="icons">Ligne de crédit</p>
                        </div>
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_6.svg" alt="">
                        <p class="icons">Achat de véhicule</p>
                        </div>
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_7.svg" alt="">
                        <p class="icons">Investissement</p>
                        </div>
                        <div class="icons_content">
                        <img src="@/assets/img/svg/icon_8.svg" alt="">
                        <p class="icons">Avance de cash</p>
                        </div>
                    </div>
                </div>
                <button>Obtenir mon prêt</button>
            </div>
         </div>



         <div class="items_concept">
          <div class="concept_img">
              <img src="@/assets/img/svg/concept_3.svg" alt="">
          </div>
          <div class="content_concept">
              <div class="concept_title">
                  <h2>Partenaire de vos plateformes préférées</h2>
              </div>
              <div class="description">
                    <div class="description_content">
                        <p>Vos plateformes préférées travaillent avec Mansa et proposent nos prêts à leurs utilisateurs. Plus de 35 plateformes offrent des prêts Mansa à leurs indépendants.</p>
                    </div>
                    <div class="icons_content_box">
                        <div class="icons_content_">
                        <img src="@/assets/img/svg/commet.png" alt="">
                        </div>
                        <div class="icons_content_">
                        <img src="@/assets/img/svg/shine.png" alt="">
                        </div>
                        <div class="icons_content_">
                        <img src="@/assets/img/svg/wemind.png" alt="">
                        </div>
                        <div class="icons_content_">
                        <img src="@/assets/img/svg/georges.png" alt="">
                        </div>
                    </div>
                </div>
                <div class="lien">
                <nuxt-link to='/'>Découvrir les partenaires</nuxt-link>
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

.concept {
    margin-top: 100px;
}

.items_concept {
    display: flex; 
    flex-flow: row wrap; 
    justify-content: space-between; 
    align-items: center; 
    text-align: center;
    margin-bottom: 50px;
}

.items_concept_reverse {
    display: flex; 
    flex-flow: row-reverse wrap; 
    justify-content: space-between; 
    align-items: center; 
    text-align: center;
    margin-bottom: 50px;
    
}

.concept_img_reverse {
    
    justify-content: flex-end;
}

.concept_img_reverse img {
    width: 80%;
}

.concept_img {
    width: 100%; 

}

.concept_img img {
    width: 80%;
}

.concept_title h2 {
    font-size: 32px; 
    margin-top: 15px;
    line-height: 32px;
}

.description {
    display: flex; 
    flex-flow: column-reverse;
}

.description_content {
    padding: 4px 0px;
    line-height: 20px;
}

.icons {
    display: none; 
}

.icons_content_ img {
    width: 70px;
}

.icons_content_box {
    display: flex; 
    flex-flow: row wrap; 
    justify-content: space-between; 
    align-items: center;
    margin: 30px 10px;
}

button {
    background-color: var(--rouge);
    border: none; 
    display: flex;
    margin: 30px auto;
    padding: 14px 24px; 
    color: var(--white);
    border-radius: 8px;
    font-size: 14px;
    font-weight: 700;
}

.lien {
    margin-top: 30px;
}

a {
    color: var(--violet);
    font-weight: 700; 
    text-decoration: none; 
}

@media screen and (min-width: 768px) {
    .concept_img img {
    width: 50%;
    }

    .concept_img_reverse {
    
    }   
}

@media screen and (min-width: 1024px) {

    .items_concept {
        text-align: left;
        margin-bottom: 100px;
    }

    .items_concept_reverse {
        text-align: left;
        margin-bottom: 100px;
    }

    .concept_img {
        width: 50%;
    }

     .concept_img img {
        width: 65%;
    }

    .content_concept {
        width: 50%;
    }

    .description {
        flex-flow: column;
    }

    .description_content {
        margin-top: 20px;
    }

    .icons_content_box {
        margin-left: 0px;
    }

    .icons_content {
        display: flex;
        flex-flow: column;
        width: 24%;
        align-content: center;
        justify-content: center;
        text-align: center;
    }

    .icons_content img {
        width: 40px;
        display: flex; 
    }

    .icons {
        display: inline;
        margin-top: 10px;

    }

    button {
        margin: 30px 0;
    }

    .lien {
    margin-top: 10px;
    }
}

@media screen and (min-width: 1440px) { 
    .concept {
        max-width: 1440px;
        margin: 50px auto; 
    }
}




</style>