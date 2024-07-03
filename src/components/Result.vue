<template>
  <!-- <slot>Default value</slot> -->
  <p>Reaction time {{score}} ms</p>
  <p class="rank" > {{rank}}</p>
</template>

<script>

export default {
    props: ['score'],
    data(){
        return{
            rank : null
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = 'Ninja fingers'
        } else if(this.score < 400) {
            this.rank = 'Rapid flexes'
        } else{
            this.rank = 'Two slow'
        }
    }

}
</script>

<style >
.rank{
    font-size:1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>