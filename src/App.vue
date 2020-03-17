<template>
  <div class="root">
    <SortableList lockAxis="y"
                  :distance="5"
                  lockOffset="10%"
                  v-model="items">
      <SortableItem v-for="(item, index) in items"
                    :index="index"
                    :key="index"
                    :item="item" />
    </SortableList>
  </div>
</template>

<script>
import SortableList from './components/sortable-list'
import SortableItem from './components/sortable-item'

export default {
  name: 'App',
  components: {
    SortableItem,
    SortableList
  },
  data() {
    return {
      items: ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5', 'Item 6', 'Item 7', 'Item 8', 'Item 9', 'Item 10', 'Item 11', 'Item 12', 'Item 13']
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
ul {
  width: 500px;
  margin: 50px auto;
  list-style: none;
}
</style>
