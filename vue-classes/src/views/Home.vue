<template>
  <div class="home">
    <div class="search-bar">
        <form class="pure-form">
            <i class="fas fa-search"></i><input v-model="searchText" />
        </form>
    </div>
    <ClassData :classes="filteredData" @course-add="courseAdded"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ClassData from '@/components/ClassList.vue'
import data from '../assets/class-data';

export default {
  name: 'Home',
  components: {
    ClassData
  },
  data() {
    return {
      searchText: '',
      data
    }
  },
  methods: {
    courseAdded(id){
      console.log('hey!', id);
    }
  },
  computed: {
    filteredData(){
      return this.data.filter(item => item.name.includes(this.searchText));
    }
  }
}
</script>
<style scoped>
  .search-bar {
    margin-bottom: 30px;
  }
</style>
