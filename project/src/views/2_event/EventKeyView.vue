<template>
  <div>
    <!-- <input type="search" @keyup="checkEnter($event)" v-model="searchText" />
    <button @click="doSearch">조회</button> -->

    <input type="search" @keyup.enter="doSearch" v-model="searchText" />
    <button @click="doSearch">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      searchText: '',
      sampleData: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(event) {
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>
