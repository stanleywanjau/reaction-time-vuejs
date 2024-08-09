<template>
  <p>Reaction time {{ score }}</p>
  <p class="text-xl text-green-200">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {            
            rank:null
        }
    },
    mounted() {
        if (this.score < 250) {
        this.rank = 'ninja fingers'
        } else if (this.score < 400) {
        this.rank = "Rapid Reflexes"
        } else {
        this.rank = "snail pace..."
    }
    
 }
}
</script>

<style>

</style>