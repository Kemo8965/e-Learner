<template>
<div>
  <v-container>
    <v-row>
      <v-col>
        <v-card width="400" height="400" class=" mt-16  card">
   <v-card-title>
       Login with <v-spacer/><span class="learn">eLearner</span>
     </v-card-title>

     <v-card-text>
         <form class="mt-14">
     <v-text-field
      v-model="email"
      :error-messages="emailErrors"
      label="E-mail"
      required
      prepend-icon="mdi-account-circle"
      @input="$v.email.$touch()"
      @blur="$v.email.$touch()"
    ></v-text-field>

     <v-text-field
      v-model="password"
      :error-messages="passwordErrors"
      
      label="Password"
      :type= "showPassword ? 'text' : 'password' "
       prepend-icon="mdi-lock"
      :append-icon="showPassword? 'mdi-eye' : 'mdi-eye-off'"
      required
      @input="$v.password.$touch()"
      @blur="$v.password.$touch()"
      @click:append="showPassword = !showPassword"
    ></v-text-field>
   
    <v-card-actions>
        <v-btn
      class="mr-4 success"
      @click="submit"
    >
      Register
    </v-btn>

    <v-btn
     class="mr-4 info"
     @click="clear">
      Login
    </v-btn>
    </v-card-actions> 
    
  </form>
 
     </v-card-text>
   </v-card>

      </v-col>

      <v-col class="">
          <v-card width="400" height="400" class=" mt-16  card sign-in-img"></v-card>
      </v-col>
    </v-row>
  </v-container>
</div>
</template>

<<script>
  import { validationMixin } from 'vuelidate'
  import { required, minLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
      email: { required, email },
      password: { required, minLength: minLength(6) },
      
      },
    

    data: () => ({
      showPassword: false,
      email: '',
      password:'',
      
    }),

    computed: {

      checkboxErrors () {
        const errors = []
        if (!this.$v.checkbox.$dirty) return errors
        !this.$v.checkbox.checked && errors.push('You must agree to continue!')
        return errors
      },
      selectErrors () {
        const errors = []
        if (!this.$v.select.$dirty) return errors
        !this.$v.select.required && errors.push('Item is required')
        return errors
      },
      passwordErrors () {
        const errors = []
        if (!this.$v.password.$dirty) return errors
        !this.$v.password.minLength && errors.push('Password must be at least 6 characters long')
        !this.$v.password.required && errors.push('Password is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid e-mail')
        !this.$v.email.required && errors.push('E-mail is required')
        return errors
      },
    },

    methods: {
      submit () {
        this.$v.$touch()
        this.$router.push('/');
      },
      clear () {
        this.$v.$reset() 
        this.email = ''
        this.password = ''
        
      },
    },
  }
</script>

<style lang="scss" scoped>
.learn{
  color:blue;

}

.sign-in-img{
  background-image: url('../../assets/images/pug2.jpg');
  right: 2.5rem;
  width:100%;
  background-size: cover;
  background-repeat: no-repeat;
}
  </style>