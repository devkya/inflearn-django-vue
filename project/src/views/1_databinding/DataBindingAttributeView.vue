<template>
  <div>
    <img :src="imgSrc" alt="" style="width: 200px; height: auto" />
    <br />
    <input type="text" v-bind:value="userId" readonly />
    <input type="text" :value="userId" readonly />
    <br />
    <input type="search" name="" id="" v-model="txt1" />
    <button :disabled="txt1 == ''">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'devkya',
      imgSrc:
        'https://live-production.wcms.abc-cdn.net.au/ff1221fbfdb2fe163fdda15df5f77676?impolicy=wcms_crop_resize&cropH=394&cropW=700&xPos=0&yPos=37&width=862&height=485',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
