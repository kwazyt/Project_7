<template>
    <div>
        <h1>Login</h1><br>
        <b-form @submit="onSubmit"  v-if="show">
      <b-form-group
      id="input-group-4"
      label="Username:"
      label-for="input-4">
        <b-form-input
          id="input-4"
          v-model="form.username"
          placeholder="Enter Username"
          required>
        </b-form-input>
      </b-form-group>

      <b-form-group
      id="input-group-5"
      label="Password:"
      label-for="input-5"
      description="Your password must consist of a combination of uppercase and lowercase letters, numbers and special symbols, such as punctuation. It should be at least 8 characters long ">
        <b-form-input
          id="input-5"
          v-model="form.password"
          placeholder="Enter Password"
          required>
        </b-form-input>
      </b-form-group><br>

      <b-button pill size="lg" type="submit" variant="primary">Continue</b-button>
        </b-form>
    </div>
</template>

<script>
export default {
  data () {
    return {
      form: {
        username: '',
        password: ''
      },
      show: true
    }
  },
  methods: {
    onSubmit (event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    }
  }
}
</script>
