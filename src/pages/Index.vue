<template>
  <q-page class="q-page">
    <product></product>
  </q-page>
</template>

<script lang="ts">
import { Todo, Meta } from 'components/models'
import { Vue, Component } from 'vue-property-decorator'
import Product from '../components/product'
@Component({
  components: { Product }
})
export default class PageIndex extends Vue {
  todos: Todo[] = [
    {
      id: 1,
      content: 'ct1'
    },
    {
      id: 2,
      content: 'ct2'
    },
    {
      id: 3,
      content: 'ct3'
    },
    {
      id: 4,
      content: 'ct4'
    },
    {
      id: 5,
      content: 'ct5'
    }
  ];

  meta: Meta = {
    totalCount: 1200
  };
}
</script>

<style lang="stylus">
@import '../css/quasar.variables.styl'

</style>
