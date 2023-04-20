<template>
    <div>
        <p>Reaction time: {{ this.score }} ms</p>
        <p>{{ this.rank }}</p>
    </div>
</template>
<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null,
        }
    },
    mounted() {
        if(this.score <= 250) {
            this.rank = 'Fast'
        } else if (this.score <= 400) {
            this.rank = 'Slower'
        } else {
            this.rank = 'So Sloooow'
        }
    }
}
</script>
<style>
    
</style>