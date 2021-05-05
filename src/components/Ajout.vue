<template>
  <form>
    <div class="form-group row">
      <label for="name" class="col-form-label col-sm-4">Ajouter un appareil: </label>
      <input type="text" class="form-control col-sm-8" name="name" id="name" placeholder="nom de l'appareil" v-model="newAppareil.name">
    </div>
    <div class="form-group row">
      <label for="desc" class="col-sm-4 col-form-label"> Description </label>
      <textarea class="form-control col-sm-8" name="desc" id="desc" rows="3" v-model="newAppareil.description"></textarea>
    </div>
    <div class="form-check">
      <label class="form-check-label">
        <input type="checkbox" class="form-check-input" name="etat" id="etat" checked v-model="newAppareil.etat">
        Etat de l'appareil 
      </label>
    </div>
    <div>
      <button type="button" class="btn btn-success float-right" :disabled = "newAppareil.name == ''" @click="onSubmit()"> Valider </button>
    </div>
  </form> 
</template>

<script>
export default {
  data: () => {
    return {
      newAppareil: {
      etat: true,
      name: '',
      description: ''
    }
    }
  },
  methods:{
    onSubmit(){
      console.log(this.newAppareil);
    }
  }
}
</script>

<style lang = "scss" scoped>

</style>