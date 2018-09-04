<template>
<v-app>
<<<<<<< HEAD
   <v-form v-model="valid"> 
=======
   <v-form v-model="valid">
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
    <v-text-field
      v-model="name"
      :rules="nameRules"
      :counter="10"
      label="Name"
<<<<<<< HEAD
      required  
=======
      required
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
    ></v-text-field>
    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
    ></v-text-field>
  </v-form>
    <div class="text-xs-center">
<<<<<<< HEAD
    <v-btn color="back" dark @click="Dologin"><v-icon>vpn_key</v-icon> </v-btn> 
    <nuxt-link to="/"><v-btn color="back" dark @click="Dosave"><v-icon>power_settings_new</v-icon> </v-btn></nuxt-link>
  </div>
  
=======
    <nuxt-link to="/table"><v-btn color="back" dark><v-icon>vpn_key</v-icon> </v-btn></nuxt-link>
    <nuxt-link to="/"><v-btn color="back" dark><v-icon>power_settings_new</v-icon> </v-btn></nuxt-link>
  </div>
  <v-footer class="grey darken-4">
    <v-spacer></v-spacer>
    <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
  </v-app>
</template>

<script>
  export default {
    layout : "publics",
<<<<<<< HEAD
    data: () => ({ //แหล่งเก็บชื่อตัวแปร
=======
    data: () => ({
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
      valid: false,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
<<<<<<< HEAD
        v => v.length <= 20 || 'Name must be less than 10 characters'
=======
        v => v.length <= 10 || 'Name must be less than 10 characters'
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
      ]
<<<<<<< HEAD
    }),
    methods:{
      async Dologin(){
        console.log (this.email)
        console.log (this.password)
        let res = await this.$http.post('http://127.0.0.1/php-thada/login.php', {
          user : this.name,
          pass : this.email
        })
        if (res.data.ok){
          this.$router.push('/table')
        }
      },
      Dosave(){
        this.name='',
        this.email=''
      }
    }
=======
    })
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
  }
</script>