
<template>
<<<<<<< HEAD
<v-parallax src="/pic/back.jpg" height="649" >
=======
<v-parallax src="/pic/back.jpg"  >
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
  <div>
    <br>
      <router-link :to="{ path: '/student'}" replace><center>
      <div class="text-xs-center">
        <v-btn round color="black" dark>Welcome</v-btn>
      </div>
    </center>
    </router-link>
  </div>

</v-parallax>

</template>

<script>
export default {
  layout : "default",
  data() {
    return {
      id: 1,
    }
  },
<<<<<<< HEAD
  styleObject: {
    font: '.font-weight-regular.font-italic',
  },
=======
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
}
</script>
