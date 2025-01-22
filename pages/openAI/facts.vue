<script setup>
    const params = {
        model : "text-davinci-003", 
        temperature: 0,
        max_tokens: 60,
        top_p: 1.0,
        frequency_penalty: 0.0,
        presence_penalty: 0.0,
        additional_prompt: "Q: Who is Batman?\nA: Batman is a fictional comic book character.\n\nQ: What is torsalplexity?\nA: Text here.",
    };
</script>

<template>
    <div class="row">
        <div class="col-12 col-md-5 order-3 order-md-1">
            <OpenAIForm :params="params" />
        </div>
        <div class="col-1 d-none d-md-block text-center order-md-2">
            <div class="vr h-100 my-4"></div>
        </div>
        <div class="col-12 d-block d-md-none text-center order-2">
            <hr class="w-100 mx-auto" />
        </div>
        <div class="col-12 col-md-6 order-1 order-md-3">
            <div class="p-3 bg-light border rounded-3 example">
                Q: Who is Batman?<br/>
                A: Batman is a fictional comic book character.
            </div>
        </div>
    </div>  
</template>
<style scoped>.example { overflow:auto; max-height:35rem; }</style>
