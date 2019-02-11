<template>
  <div class="hello">
    <p>You can close the modal dialog by pressing ESC.</p>
    <br>
    <a class="button is-primary" v-on:click="showModal = true">Open Modal Dialog</a>
    <modal v-if="showModal" v-on:close="showModal = false">
      <div class="box">
        <article class="media">
          <div class="media-left">
            <figure class="image is-64x64">
              <img src="@/assets/logo.png" alt="Image">
            </figure>
          </div>
          <div class="media-content">
            <div class="content">
              <p>
                <strong>Vue.js</strong>
                <br>
                Vue.js is an open-source JavaScript framework for building user interfaces and single-page applications.
              </p>
            </div>
          </div>
        </article>
      </div>
    </modal>
  </div>
</template>

<script>

import Modal from './Modal.vue';

export default {
  name: 'HelloWorld',
  components: {Modal},
  data() {
    return {
      showModal: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
