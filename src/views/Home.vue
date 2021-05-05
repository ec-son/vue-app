<template>
  <div class="home">
    <div class="card" v-for="(item,index) in appareils" v-bind:key="item.id">
      <div class="card-body">
        <h5 class="card-title"> {{ item.name }} </h5>
        <div class="etat">
          <div>
            <span class="titre">Etat: </span>
            <span :class=" item.etat == 'Eteint'?'etatRed':'etatGreen'" > {{ item.etat }} </span>
          </div>
          <div>
            <button class="btn btn-danger float-right" @click="onChangeEtat(index,false)" :disabled="item.etat == 'Eteint'" > Eteindre </button>
            <button class="btn btn-success float-right" @click="onChangeEtat(index,true)" :disabled="item.etat == 'Allumé'" > Allumer </button>
          </div>
        </div>
        <div class="card-text">
          <span class="titre"> Description: </span> <span> {{ item.description }} </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      appareils:[
        {
          name: 'Machine à laver',
          etat: 'Allumé',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
          
        },
        {
          name: 'Fer à repasser',
          etat: 'Allumé',
          description: 'Architecto aspernatur earum ducimus deleniti, ipsum voluptatum'
        }
      ]
    }
  },
  methods:{
    onChangeEtat(id,etat){
      this.appareils[id].etat = etat == true? 'Allumé':'Eteint'
    }
  }
}
</script>

<style lang = "scss" scoped>
  .home {
    margin-top: 2rem;
  }
  .titre {
    font-weight: bold;
  }
  button{
    margin-left: 1rem;
  }
  .etat {
    display: flex;
  }
  .card {
    margin-bottom: 1rem;
  }
  .etatGreen {
    color: green;
  }
  .etatRed {
    color: red
  }
</style>