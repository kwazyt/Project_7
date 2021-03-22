<template>
  <div>
    <b-container class="m-5">
      <b-input-group>
      <b-input-group-prepend class="mx-2">
          <b-avatar></b-avatar>
      </b-input-group-prepend>
    <b-form-input v-model="text" placeholder="Write something...">
    </b-form-input>
      <b-input-group-append>
        <input
        style= "display:none"
        type="file"
        @change="onFileSelected"
        ref="fileInput">
        <b-button
        @click="$refs.fileInput.click()"
        variant="outline-secondary">
            <b-icon icon="image"></b-icon>
            Photo
        </b-button>
          <b-button
          @click="onUpload"
          variant="primary">
          Add new post
          </b-button>
          </b-input-group-append>
          </b-input-group>
    </b-container>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  methods: {
    onFileSelected (event) {
      this.selectedFile = event.target.files[0]
    },
    onUpload () {
      const fd = new FormData()
      fd.append('image', this.selectedFile, this.selectedFile.name)
      axios.post('#', fd)
        .then(res => {
          console.log(res)
        })
    }
  }
}
</script>
