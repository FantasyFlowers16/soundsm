<template>
  <div>
    <div class="b-catalog">
      <div class="b-catalog__item" v-for="item in catalog"></div>
    </div>
    <img src="big1.png">
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component({
  components: {  }
})
export default class Product extends Vue {

  catalog=[
    {
      id:1,
      img:'232',
      bigImg:'../img/big1.png',
      name:'',
      check:true
    },
    {
      id:2,
      img:'23',
      bigImg:'3423423424',
      name:'',
      check:false
    },
    {
      id:3,
      img:'232',
      bigImg:'234324',
      name:'',
      check:false
    },
    {
      id:4,
      img:'232',
      bigImg:'23423',
      name:'',
      check:false
    }
  ]
  get ActiveImg () {
    const activeImg =this.catalog.map((el)=>{
      if(el.check){
        return el
      }
    })
    console.log(activeImg)
    return activeImg[0]?.bigImg //eslint-disable-line
  }

}
</script>

<style lang="stylus">
@import '../css/quasar.variables.styl'
.b-catalog
  margin-top 80px
  display flex
  &__item
    width 50px 
    height 50px
    background white
    box-shadow 0 0 10px rgba(0,0,0,0.5); /* Параметры тени */
</style>
