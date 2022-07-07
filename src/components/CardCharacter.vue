<template>
  <div class="character">
      <img :src="character.image" :alt="character.name"/>
      <div class="character__info">
          {{ character.name }}
          <div class="status">
              <span :class="
                character.status == 'Alive' ? 'alive' : (
                    character.status == 'Death' ? 'dead' : 'default'
                )
              "></span>
              <span>{{character.status}} - {{character.species}}</span>
          </div>
          <div class="origin">
              <span>
                  Origin : {{character.origin.name}}
              </span>
          </div>
          <div class="location">
              <span>
                  Location : {{character.location.name}}
              </span>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    props : ['character']
}
</script>

<style>

</style>