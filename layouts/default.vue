<template>
  <div>
    <the-header/>
    <nuxt />
    <the-footer/>
  </div>
</template>


<script>

import TheHeader from '../components/features/TheHeader'
import TheFooter from '../components/features/TheFooter'

export default {
    components : {
      TheHeader,
      TheFooter
    }
}
</script>

<style>
html {
  font-family: 'Assistant', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  font-weight: 400;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background-color: rgb(250, 250, 250);
  color: rgb(27, 27, 27);
  overflow-x: hidden;

}

body {
  overflow-x: hidden;
}

h1 {
  font-family: 'Playfair Display', serif;
  font-weight: 900;
}

:root {
  --violet: #644ad1;
  --rouge: #ff0d39;
  --white: #fafafa;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

</style>
