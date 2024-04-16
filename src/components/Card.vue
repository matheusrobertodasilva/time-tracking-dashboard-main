<script>
    export default {
        props:[
            "corFundo",
            "titulo",
            "tempoOne",
            "tempoTwo",
            "imagemFundo"
        ]
    }
</script>

<template>
    <div 
    class="rounded-tl-xl rounded-tr-xl rounded-bl-2xl rounded-br-2xl bg-no-repeat bg-[right_15px_top_-10px] my-5 pt-8 lg:my-0 lg:flex lg:flex-col lg:justify-end lg:w-[18vw]"
    :class="[corFundo],imagemFundo"
    >
        <div class="bg-Dark-blue rounded-xl p-6 lg:hover:bg-[#34397b] ">
            <div class="space-y-2 lg:space-y-4">
                <div class="flex justify-between items-center">
                    <p>{{ titulo }}</p>
                    <a href="#">
                        <svg width="21" height="5" xmlns="http://www.w3.org/2000/svg"><path d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z" fill="#BBC0FF" fill-rule="evenodd" /></svg>
                    </a>
                </div>
                <div class="flex justify-between items-center lg:flex-col lg:items-start">
                    <h4 class="text-3xl lg:text-6xl font-light">{{ tempoOne }}hrs</h4>
                    <p class="text-Desaturated-blue ">Last Week - {{ tempoTwo }}hrs</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style>

</style>