<template>
  <div>
    <p>漢字2文字を入れてください</p>
    <div class="level-item">
      <input class="input is-small" type="text" :value="msg" @change="onChangeInput">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: ''
    }
  },
  methods: {
    onChangeInput(event) {
      this.commitChange(event.target.value)
    },
    commitChange(newValue) {
      this.$emit('input', newValue)
    }
  }
}

</script>
