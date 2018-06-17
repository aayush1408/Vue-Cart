<template>
<div>
<div class="container">
  <div class="row">
        <div v-for="card in cards" :key="card.name" class="col-md-3">
          <img :src=card.url />
          <h4>{{card.name}}</h4>          
          <h5>{{card.price}}</h5>
          <h5>{{card.type}}</h5>
          <button class="btn btn-sm btn-success">Add to cart</button>
        </div>
    </div>
</div>
</div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      cards : [
        {
        name:'Dark Magician',
        url:'https://vignette.wikia.nocookie.net/myyugiohdeck/images/d/da/Dark_Magician.jpg/revision/latest/scale-to-width-down/325?cb=20110610035254',
        price:'2000',
        type:'Monster'
      },
      {
        name:'Red Eyes Black Dragon ',
        url:'https://6d4be195623157e28848-7697ece4918e0a73861de0eb37d08968.ssl.cf1.rackcdn.com/22341_200w.jpg',
        price:'2000',
        type:'Monster'
      },
        {
        name:'Blue Eye White Dragon ',
        url:'https://vignette.wikia.nocookie.net/yugioh/images/7/77/BlueEyesWhiteDragon-LCKC-EN-UR-1E.png/revision/latest?cb=20180415030139',
        price:'4000',
        type:'Monster'
      },
        {
        name:'Sword Slasher',
        url:'http://qtoptens.com/wp-content/uploads/2017/06/SwordSlasher.png',
        price:'1500',
        type:'Monster'
      }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img{
  height: 300px;
  width: 200px;
}
</style>
