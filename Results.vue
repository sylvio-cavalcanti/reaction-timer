<template>
    <div class="results" >
        <h1>{{ rank }}</h1>
        <p>Reaction time: {{ score }} ms</p>
    </div>
</template>

<script>
export default {
    props:['score'], 
    data(){
        return {
            rank: null 
        }
    },
    mounted(){
        if (this.score <= 250){
            this.rank = "Awesome! You are a fast one!"
        }
        else if (this.score < 400){
            this.rank = "Not bad, but you could be quicker!"
        }
        else{
            this.rank = "Well that took a while..."
        }
    }
}
</script>
<style>
    .results{
        width: 500px;
        border-radius: 10px;
        background: #0f7caf;
        color: white;
        text-align: center;
        padding: 5px 0;
        margin: 40px auto;
        font-weight: 600;
    }
</style>