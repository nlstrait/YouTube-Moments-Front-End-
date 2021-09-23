<template>
  <div class="search-bar">
    <input v-model="query" @keyup.enter="handleEnter">
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  data() {
    return {
      query: '',
    }
  },
  methods: {
    handleEnter: function () {
      this.$emit('search', this.query);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
.search-bar {
  margin: auto;
  align-self: center;
  border: 1px solid lightgrey;
  border-radius: 25px;
  min-width: 200px;
  max-width: 584px;
  min-height: 25px;
}
.search-bar:hover {
  box-shadow: lightgrey 0 1px 5px;
}
.search-bar:focus-within{
  box-shadow: lightgrey 0 1px 5px;
}
input {
  margin: auto;
  padding: 0;
  word-wrap: break-word;
  display: flex;
  flex: 100%;
  height: 46px;
  width: calc(100% - 40px);
  border: none;
  background: transparent;
  font-size: 16px;
}
input:focus {
  outline: none;
}
</style>
