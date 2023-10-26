<template>
    <div>
        <h1 class="mt-5 text-center">#Advice {{ id }}</h1>
        <p class="text-center mt-5 mx-5">"{{ advice }}"</p>
    </div>
</template>
<script>

export default {
    data() {
        return {
            advice: '',
            id:''
        };
    },
    async mounted() {
        this.advice = await getAdvice();
        this.id= await getAdviceid()

    },
};
async function getAdvice() {
    const response = await fetch('https://api.adviceslip.com/advice');
    const data = await response.json();
    

    const randomAdvice = data.slip.advice
    return randomAdvice;
}
async function getAdviceid() {
    const response = await fetch('https://api.adviceslip.com/advice');
    const data = await response.json();
    
    const idAdvice = data.slip.id
    return idAdvice;
}
</script>