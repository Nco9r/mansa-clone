<template>
  <div>
      <header class="mobile">
          <div class="top_bar" :class="{top_bar_color: scrollPosition > 1}">
            <div class="logo_header">
                <p>Mansa<span class="red">.</span></p>
            </div>
            <div class="hamburger" @click="open = !open">
                <span></span>
            </div>
          </div>
          <transition name="open" appear>
          <div class="menu" v-if='open'>
              <div class="items_menu">
                  <nuxt-link to='/'>FAQ</nuxt-link>
                  <nuxt-link to='/'>Blog</nuxt-link>
                  <button>S'identifier</button>
              </div>
          </div>
          </transition>
      </header>

      <header class="desktop">
          <div class="top_bar" :class="{top_bar_color: scrollPosition > 1}">
            <div class="logo_header">
                <p>Mansa<span class="red">.</span></p>
            </div>
           <div class="menu_desktop">
              <div class="items_menu">
                  <nuxt-link to='/'>FAQ</nuxt-link>
                  <nuxt-link to='/'>Blog</nuxt-link>
                  <button>S'identifier</button>
              </div>
          </div>
          </div>
      </header>
  </div>
</template>

<script>
export default {
    data() {
        return {
            open: false,
            scrollPosition: null
        }
    },
    mounted() {
        window.addEventListener('scroll', this.updateScroll);
    },
    methods: {
        updateScroll() {
            this.scrollPosition = window.scrollY
        }
    }


}
</script>

<style>

.desktop {
    display: none;
}

.mobile {
    padding: 15px 12px; 
    display: flex;  
}

.top_bar {
    display: flex; 
    justify-content: space-between; 
    align-items: center;
    position: fixed; 
    top: 0px; 
    left: 0px;
    right: 0px;
    z-index: 9;
    padding: 15px 12px 7px 12px;
    background-color: var(--white);
}

.top_bar_color {
    box-shadow: rgba(48, 41, 41, 0.1) 0px 12px 12px -10px;
    border-bottom: 1px solid rgba(48, 41, 41, 0.1);
}

.logo_header p {
    color: var(--violet); 
    font-size: 32px; 
    font-weight: bold;
}

.red {
    color: var(--rouge);
}

.hamburger {
    display: flex; 
    flex-flow: column; 
    cursor: pointer;
    
}

.hamburger span {
    height: 3Px;
    border: none; 
    background-color: var(--violet); 
    width: 28px;
    border-radius: 4px;
    z-index: 30;
    outline: none;
}

.hamburger span::before {
    content: '';
    height: 3Px;
    border: none; 
    background-color: var(--violet); 
    width: 28px;
    position: absolute;
    border-radius: 4px;
    margin-top: -10px;
}

.hamburger span::after {
    content: '';
    height: 3Px;
    border: none; 
    background-color: var(--violet); 
    width: 28px;
    position: absolute;
    border-radius: 4px;
    margin-top: 10px;
}

.menu {
    background-color: var(--violet);
    height: 320px;
    width: 210px;
    display: flex;
    position: fixed; 
    top: 0; 
    right: 0;
    border-radius: 0 0px 0px 10px;
    box-shadow: rgba(0, 0, 0, 0.4) 0px 10px 30px;
    z-index: 100;
   
}

.items_menu {
    display: flex; 
    flex-flow: column; 
    margin: auto;
    text-align: center;
}

.items_menu a {
    color: var(--white);
    text-decoration: none; 
    cursor: pointer; 
    font-weight: 700;
    margin: 24px 0;
}

.items_menu button {
    padding: 12px 20px;
    color: var(--rouge);
    border: 1px solid var(--rouge);
    border-radius: 10px;
    font-size: 15px;
    font-weight: 500;
    min-height: fit-content;
    outline: none; 
    background-color: var(--white);
}

/* TRANSITION */

@keyframes open {
    from{
        transform: translateX(100%);
    }
    to {
        transform: translateX(0%);
    }
}

@keyframes close {
    from{
        transform: translateX(0%);
    }
    to {
        transform: translateX(100%);
    }
}

.open-enter-active {
    animation: open .3s; 
}

.open-leave-active {
    animation: close .3s; 
}

@media screen and (min-width: 1024px) {

    a {
        transition: all .5s;
    }
    a:hover {
    opacity: .5;
    }
   

    .mobile {
        display: none; 
    }
    .desktop {
        padding: 0 150px;
        display: flex;
    }

    .top_bar {
        padding: 0px 50px;
    }

    .items_menu {
        display: flex;
        flex-flow: row;
    }

    .items_menu a {
        color: var(--violet);
        margin-right: 70px;
    }

    .items_menu button { 
    color: var(--rouge);
    border: none;
    border-radius: 10px;
    font-size: 15px;
    font-weight: 700;
    outline: none; 
    background-color: var(--white);
}
}


</style>