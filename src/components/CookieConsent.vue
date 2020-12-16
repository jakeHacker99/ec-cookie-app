<template>
  <div class="cookie-container"  >
    <p>
      the Detecify website uses cookie to make your online experience easier and
      better. By using our website, you consent to our use of cookies. For more
      information, see our <a href="#">privacy policy</a>
    </p>

    <button class="cookie-btn" @click="agree" >agree</button>
  </div>
</template>

<script>

export default {
  
  data() {return {
      consented:false,
    }},
    methods:{
      agree(){
        localStorage.setItem("cookieConsented", "true")
        this.consented= true
        
      }
    },
    created(){
      if(localStorage.getItem("cookieConsented")){
        this.consented =true
      }
    }
};
</script>


<style scoped>
.cookie-container {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: #2f3;
  color: black;
  padding: 0 32px;
  box-shadow: 0 -2px 16px rgba(47, 54, 64);

}

.cookie-container a {
  color: black;
}

.cookie-btn {
  background: blueviolet;
  border: 0;
  color: black;
  padding: 12px 48px;
  font-size: 18px;
  margin-bottom: 16px;
  border-radius: 8px;
  cursor: pointer;
}
</style>