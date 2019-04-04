<template>
  <div id="app">
    <section>
      <div class="columns is-centered">
        <div class="column is-three-fifths is-offset-one-fifth">
          <SynthesizedImage :msg="msg"/>
          <Form @input="onInput" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import SynthesizedImage from './components/SynthesizedImage'
import Form from  './components/Form'
import 'bulma/css/bulma.css'

export default {
  name: 'App',
  components: {
    SynthesizedImage,
    Form
  },
  data() {
    return {
      msg: '',
    }
  },
  methods: {
    onInput(newMessage) {
      this.msg = newMessage
    }
  }

}
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
