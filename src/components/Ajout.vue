<template>
  <form>
    <div class="form-group">
      <label for="name">Ajouter un appareil: </label>
      <input type="text" class="form-control" name="name" id="name" aria-describedby="helpId" placeholder="nom de l'appareil" v-model="newAppareil.name">
      <small id="helpId" class="form-text text-muted">Precisez bien le nom.</small>
    </div>
    <div class="form-check">
      <label class="form-check-label">
        <input type="checkbox" class="form-check-input" name="etat" id="etat" checked v-model="newAppareil.etat">
        Etat de l'appareil 
      </label>
    </div>
    <div>
      <button class="btn btn-success float-right" :disabled = "newAppareil.name == ''"> Valider </button>
    </div>
</form> 
</template>

<script>
import { Options, Vue } from 'vue-class-component';
export default {
    data: () => {
      return {
        newAppareil: {
        etat: true,
        name: ''
      }
      }
    }
}
</script>

<style lang = "scss" scoped>
    form {
        /* width: 50%; */
        /* margin: auto; */
        margin-top: 2rem;
    }
</style>