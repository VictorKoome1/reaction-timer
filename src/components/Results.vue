<!-- eslint-disable -->
<template>
    <p> your reaction time is - {{ score }} ms</p>
    <p>{{ rank }}</p>
</template>

<script>

export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted () {
        if(this.score < 250) {
            this.rank = "Superb Ninja"
        } else if(this.score < 400) {
            this.rank = "Good reflexes"
        } else {
            this.rank = "snail pace..."
        }
    }
}
</script>

<style>

</style>