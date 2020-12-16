<template>
  <div id="" class="flex-container center ">
    <img alt="Vue logo" src="./assets/logo.png" style="width: 20%;" class="center">

    <CookieConsent/>


    <h1 class="center" style="font-size: 2rem;">Övning Cookies</h1>
    <h3 class="center" style="font-size:.7rem;">Här har jag bygg en cookie, fick du upp ett jobbig 
      meddelande så vet du att den funkar</h3>
  </div>
  
</template>

<script>
import CookieConsent from './components/CookieConsent'


export default {
  components: {
    CookieConsent
  }
}
</script>

<style>

.flex-container {
  display: flex;
  display: row;
}

.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
  color: blueviolet;

}

</style>
