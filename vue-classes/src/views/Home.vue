<template>
  <div class="home">
    <div class="search-bar">
        <form class="pure-form">
            <i class="fas fa-search"></i><input v-model="searchText" />
        </form>
    </div>
    <ClassData />
  </div>
</template>

<script>
// @ is an alias to /src
import ClassData from '@/components/ClassList.vue'

export default {
  name: 'Home',
  components: {
    ClassData
  },
  data() {
    return {
      searchText: '',
    }
  },
  computed: {
  }
}
</script>
<style scoped>
  .search-bar {
    margin-bottom: 30px;
  }
</style>
