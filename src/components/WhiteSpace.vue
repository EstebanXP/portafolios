<template>
    <div class="whiteSpace">
        <h3>{{ inText }}</h3>
    </div>
</template>

<script>
export default {
  name: 'WhiteSpace',
  props: {
    inText: {
      type: String,
      required: true
    },
    inImage: {
      type: String,
      required: false
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.whiteSpace{
    width: 80%;
    height: 100px;
    /*border: 1px solid #000;*/
    margin: auto;
    text-align: auto;
}
</style>
