<template>
  <div class="my-body">
    <div class="flex flex-wrap justify-center items-center mt-48 p-8">
      <div class="w-full mx-auto">
        <div class="md:mx-16">
          <p class="main-title text-left text-white uppercase font-bold m-2">Have your  medical prescription delivered to your location</p>
          <p class="sub-title text-left mx-2 my-4">Your doctor generates the prescription and the drugs are delivered to your location</p>
                    <p class="main-title text-left text-white uppercase font-bold m-2">Have your  medical prescription delivered to your location</p>
          <p class="sub-title text-left mx-2 my-4">Your doctor generates the prescription and the drugs are delivered to your location</p>
        </div>
      </div>
    </div>
    <div></div>
  </div>
</template>

<script>


import HeaderComponent from "@/components/Header.vue";
    export default {
        components:{
            HeaderComponent
        }
    }

</script>

<style scoped>
.main-title {
  font-size: 48px;
  line-height: 65px;
  color: #fff;
  font-family: "Nunito";
}


.sub-title {
  font-size: 21px;
  line-height: 25px;
  color: #fff;
  font-family: "Nunito";
}


.sub-title2 {
  font-size: 18px;
  line-height: 25px;
  color: #fff;
  opacity: 0.7;
  font-family: "Nunito";
}

.order-btn {
  background-color: #fed67a;
  color: #835b00;
}

img{
  width:80%;
  margin: auto;
  overflow: hidden;
}

div{
  overflow: hidden;
}

.my-body {
  min-height: 100vh;
      background: linear-gradient(
      89.81deg,
      #646363 0.05%,
      rgba(17, 17, 17, 0.65) 41.25%
    ),
    url("https://res.cloudinary.com/dldd8ucby/image/upload/v1570283886/FlutterWave/WhatsApp_Image_2019-10-05_at_14.53.56.jpg");
    background-repeat: no-repeat;
    background-size: cover;
}
</style>