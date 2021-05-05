<template>
  <div class="home">
    <div class="card" v-for="item in appareils" v-bind:key="item.id">
      <div class="card-body">
        <h5 class="card-title"> {{ item.name }} </h5>
        <div class="etat">
          <span>Etat: {{ item.etat }} </span> 
          <div >
            <button class="btn btn-danger float-right" > Eteindre </button>
            <button class="btn btn-success float-right" > Allumer </button>
          </div>
        </div>
        <div class="card-text">
          <span class="titre"> Description: </span> <span> {{ item.description }} </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  components: {
  },
  data: () => {
    return {
      appareils:[
        {
          name: 'Machine à lavé',
          etat: 'allumé',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
          
        },
        {
          name: 'Fer à repasser',
          etat: 'allumé',
          description: 'Architecto aspernatur earum ducimus deleniti, ipsum voluptatum'
        }
      ]
    }
  }
})

export default class Home extends Vue {

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
</style>