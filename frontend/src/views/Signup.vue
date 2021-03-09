<template>
    <div>
        <h1>Sign Up</h1><br>
        <b-form @submit="onSubmit"  v-if="show">
            <b-form-group
        id="input-group-1"
        label="Email address:"
        label-for="input-1"
        description="We'll never share your email with anyone else.">
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          placeholder="Enter email"
          required>
        </b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-2"
        label="First Name:"
        label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          placeholder="Enter your first name"
          required>
        </b-form-input>
      </b-form-group>

      <b-form-group
      id="input-group-3"
      label="Surname:"
      label-for="input-3">
        <b-form-input
          id="input-3"
          v-model="form.name"
          placeholder="Enter Surname"
          required>
        </b-form-input>
      </b-form-group>

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
        email: '',
        name: ''
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
