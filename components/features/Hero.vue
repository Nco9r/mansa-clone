<template>
  <div class="hero">
      <div class="background">
          <img src="@/assets/img/svg/background_mansa.svg" alt="">
      </div>
      <div class="title_hero">
          <h1>Le crédit aux indépendants, enfin.</h1>
          <p class="content_title"> Nous faisons confiance aux indépendants et aux freelances.</p>
          <div class="cta"><button>Obtenir mon crédit</button></div>
      </div>
      <div class="left">
      <div class="simulation">
          <div class="title_simulation">
              <h2>Simulez votre prêt professionnel</h2>
          </div>
          <div class="content_simulation">
              <p><strong>Montant</strong> du prêt (entre 500€ et 10 000€)</p>
              <p class="montant">{{value | nombre}}€</p>
              <vue-slider ref="slider" v-model="value" v-bind="options"/>
          </div>
          <div class="content_simulation">
              <p>Nombre de <strong>mois</strong> (entre 3 mois et 12 mois)</p>
              <p class="montant">{{month}}</p>
              <vue-slider ref="slider" v-model="month" v-bind="options_month"/>
          </div>
          <div class="resultat">
              <div class="label">
                  <p>Mensualité</p>
              </div>
              <div class="montant_simulation">
                  <p><strong>{{ value / month | round | nombre }}</strong>€</p>
              </div>
          </div>
          <div class="resultat">
              <div class="label">
                  <p>Coût du crédit</p>
              </div>
              <div class="montant_simulation">
                  <p><strong>{{ (value * 1.032) - (value) | round 0| nombre  }}</strong>€</p>
              </div>
          </div>
          <div class="resultat">
              <div class="label">
                  <p>Montant total à rembourser</p>
              </div>
              <div class="montant_simulation">
                  <p><strong>{{value * 1.032| round 0| nombre  }}</strong>€</p>
              </div>
          </div>
          <div class="cta_simulation">
              <button>Continuer <span class="uppercase"> (sans engagement)</span></button>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import VueSlider from 'vue-slider-component/dist-css/vue-slider-component.umd.min.js'
import 'vue-slider-component/dist-css/vue-slider-component.css'
import 'vue-slider-component/theme/default.css'
import round from 'vue-round-filter';


export default {
  components: {
    VueSlider
  },
  data () {
    return {
      value: 3000,
       options: {
        dotSize: 18,
        width: 'auto',
        height: 6,
        contained: false,
        direction: 'ltr',
        min: 500,
        max: 10000,
        interval: 100,
        disabled: false,
        duration: 0.5,
        tooltip: 'none',
        processStyle: {backgroundColor: '#ff0d39'},
        dotStyle: {backgroundColor: '#ff0d39'},
      },
      total: '',
      month: 6,
       options_month: {
        dotSize: 18,
        width: 'auto',
        height: 6,
        contained: false,
        direction: 'ltr',
        min: 3,
        max: 12,
        interval: 1,
        disabled: false,
        duration: 0.5,
        tooltip: 'none',
        processStyle: {backgroundColor: '#ff0d39'},
        dotStyle: {backgroundColor: '#ff0d39'},
      },
    } 
  },
  methods: {
      total() {
          return this.value * 1.12;
      }
  },
  filters: {
      round,
      nombre(number) {
      return new Intl.NumberFormat().format(number);
    }
  }
}
</script>

<style scoped>


.hero {
    display: flex; 
    flex-flow: row wrap; 
    margin-top: 10px;
    align-items: center; 
    justify-content: center; 
}

.background {
    display: none;
}

.title_hero {
    display: flex;
    margin: 30px auto;
    flex-flow: column;
    text-align: center;
}

.title_hero h1 {
    font-size: 48px;
    line-height: 50px;
}

.content_title {
    display: none; 
}

.cta button {
    background-color: var(--rouge);
    border: none; 
    width: 180px;
    display: flex;
    margin: 30px auto;
    padding: 14px 24px; 
    color: var(--white);
    border-radius: 8px;
    font-size: 14px;
    font-weight: 700;
    text-align: center;
}

.simulation {
    width: 100%;
    padding: 30px 22px;
    display: flex;
    flex-direction: column;
    text-align: center;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 30px;
    border-radius: 8px;
    background-color: var(--white);
    z-index: 2;
}

.title_simulation h2{
    font-size: 32px; 
    line-height: 36px;
    margin-bottom: 30px;
}

.content_simulation {
    text-align: left; 
    margin-bottom: 10Px;
}

.montant {
    font-size: 32px;
    margin-top: 5px;
    color: var(--violet); 
    font-weight: 700;
}

.resultat {
    text-align: left;
    display: flex; 
    justify-content: space-between;
}

.montant_simulation {
    color: var(--violet);
    margin-bottom: 10px;
}

.cta_simulation button {
    background-color: var(--rouge);
    border: none; 
    width: 230px;
    display: flex;
    margin: 30px auto;
    padding: 14px 14px; 
    color: var(--white);
    border-radius: 8px;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    transition: all .3s;
}

.cta_simulation button:hover {
    opacity: .8;
    
}

.uppercase {
    text-transform: uppercase;
    font-size: 10px!important;
    margin-left: 15Px;
    margin-top: 3Px;
    font-weight: 700;
}

.vue-slider-process {
    background-color: var(--rouge)!important;
    border-radius: 15px;
}


@media screen and (min-width: 768px) {

    .left {
        width: 100%;
    }
   
    
}




@media screen and (min-width: 1024Px) {
    .background {
        display: inline;
    }

    .background img {
        position: absolute; 
        top: -150px;
        right: 0;
        width: 500px;
        z-index: 0;
    }

    .hero {
        padding-top: 130px;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        
    }
    
    .title_hero {
        width: 50%;
        text-align: left 
    }

    .title_hero h1 {
    font-size: 76px;
    line-height: 82px;
    margin-bottom: 40px;
    }

    .title_hero button {
    font-weight: 700;
    margin-top: 50px;
    display: flex; 
    margin: 60px 0px;
    
    }

    .content_title {
        display: inline;
    }

    .left {
        width: 50%;
        z-index: 2;
        display: flex;
        justify-content: flex-end;
        margin-top: 50px;
    }

    .simulation {
        width: 80%;
        margin-top: -80px;
        z-index: 2;
        padding: 30px 30px;
        background-color: white;


    }

    .content_simulation {
        margin-bottom: 10px;
    }
    
    .cta_simulation button {
        background-color: var(--rouge);
        border: none; 
        display: flex;
        margin: 30px auto 10px auto;
        padding: 14px 14px; 
        color: var(--white);
        border-radius: 8px;
        font-size: 14px;
        font-weight: 700;
    }   
}

@media screen and (min-width: 1440px) {
  .title_hero h1 {
    font-size: 92px;
    line-height: 100px;
  }
  
    .hero {
        max-width: 1440px;
        margin: 50px auto; 
    }

}



</style>