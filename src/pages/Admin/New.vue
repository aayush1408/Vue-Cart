<template>
  <div>
    <form>
  <div class="form-group">
    <label>Card Name</label>
    <input type="text" class="form-control" v-model="cardName" placeholder="Enter card name">
  </div>
  <div class="form-group">
    <label>Img Url</label>
    <input type="text" class="form-control" v-model="cardUrl" placeholder="Copy image address">
  </div>
   <div class="form-group">
    <label>Price</label>
    <input type="text" class="form-control" v-model="cardPrice" placeholder="Price">
  </div>
    <div class="form-group">
    <label>Card type</label>
    <select class="form-control" v-model="cardType">
      <option>Monster</option>
      <option>Spell</option>
      <option>Trap</option>
    </select>
  </div>
  <button class="btn btn-primary" @click="sendForm()">Submit</button>
</form>
  </div>
</template>
<script>
import {serverBus} from '../../main.js'
export default {
  name:'NewCard',
  data(){
    return{
      cardName:'',
      cardUrl:'',
      cardPrice:'',
      cardType:''
    };
  },
  methods:{
    sendForm(){
      if(this.cardName.length >0 && this.cardUrl.length >0 && this.cardPrice.length >0 && this.cardType.length >0 ){
        const cardName = this.cardName;
        const cardUrl = this.cardUrl;
        const cardPrice = this.cardPrice;
        const cardType = this.cardType;
        serverBus.$emit('create-card',{
          cardName,
          cardUrl,
          cardPrice,
          cardType
        });
      }
      else{
        alert('Fill in all the details');
      }
    },
  }
}
</script>

