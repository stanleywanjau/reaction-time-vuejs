<template>
  <div class="block w-40 rounded-xl bg-blue-500 text-white text-center p-28 mx-auto m-10" v-if="showBlock" @click="stopTimer">click me</div>
</template>

<script>
export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false,
            timer: null,
            reactionTime:0
        }
    },
    mounted() {
        setTimeout(() => {
            this.showBlock = true
            this.startTimer()
        },this.delay)
    },
    methods:{
        startTimer(){
            this.timer = setInterval(()=>{this.reactionTime +=10},10)
        },
        stopTimer(){
            clearInterval(this.timer)
            this.$emit('end',this.reactionTime)
        }
    }
}
</script>

<style>

</style>