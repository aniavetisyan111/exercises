<template>
   <v-col cols="12">
        <v-col cols="12">
            <v-text-field
            v-model="title"
            :rules="rules"
            filled
            label="first name"
          ></v-text-field>
          <v-text-field
            v-model="title"
            :rules="rules"
            filled
            label="last name"
          ></v-text-field>
          <v-text-field
            v-model="title"
            :rules="rules"
            filled
            label="email"
          ></v-text-field>
          <v-text-field
          v-model="password"
          :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
          :rules="[rules.required, rules.min, rules.number]"
          :type="show1 ? 'text' : 'password'"
          name="input-10-1"
          label="Password"
          hint="At least 8 characters"
          counter
          error-count="3"
          filled
          @click:append="show1 = !show1"
          ></v-text-field>
        </v-col>
        <v-col>
        <v-btn color="primary">Sign up</v-btn>
      </v-col>
      </v-col>
</template>
<script>
export default {
  name: 'ExerciseFour',

  data () {
    return {
      show1: false,
      password: 'Password',
      rules: {
        required: value => !!value || 'Required.',
        min: v => v.length >= 8 || 'Min 8 characters',
        number: v => /(?=.*\d)/.test(v) || 'Must have one number'
      }
    }
  }
}
</script>
