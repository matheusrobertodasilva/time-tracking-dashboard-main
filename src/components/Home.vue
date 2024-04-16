<script >
    import Card from './Card.vue'

    export default{
        components:{
            Card
        },
        data(){
            return{
                cards:[
                    {titulo:"Work",tempoOne:"32",tempoTwo:"36",corFundo:"bg-Light-red-(work)",imagemFundo:"bg-[url('src/assets/images/icon-work.svg')]"},
                    {titulo:"Play",tempoOne:"10",tempoTwo:"8",corFundo:'bg-Soft-blue-(play)',imagemFundo:"bg-[url('src/assets/images/icon-play.svg')]"},
                    {titulo:"Study",tempoOne:"4",tempoTwo:"7",corFundo:'bg-Light-red-(study)',imagemFundo:"bg-[url('src/assets/images/icon-study.svg')]"},
                    {titulo:"Exercise",tempoOne:"4",tempoTwo:"5",corFundo:'bg-Lime-green-(exercise)',imagemFundo:"bg-[url('src/assets/images/icon-exercise.svg')]"},
                    {titulo:"Social",tempoOne:"5",tempoTwo:"10",corFundo:'bg-Violet-(social)',imagemFundo:"bg-[url('src/assets/images/icon-social.svg')]"},
                    {titulo:"Self Care",tempoOne:"2",tempoTwo:"2",corFundo:'bg-Soft-orange-(self-care)',imagemFundo:"bg-[url('src/assets/images/icon-self-care.svg')]"}
                ]
            }
        }
    }
</script>

<template>
    <section class="px-5 my-[10vh] lg:h-screen lg:flex lg:justify-center lg:items-center ">
        <div class="lg:grid lg:grid-cols-4 lg:grid-rows-2 lg:gap-5">
            <div class="bg-Dark-blue rounded-xl lg:row-span-2 ">
                <div class="bg-Blue flex items-center rounded-xl p-7 lg:flex-col lg:items-start lg:justify-around lg:space-y-10">
                    <img src="/src/assets/images/image-jeremy.png" alt="imagem de perfil" class="w-[15vw] border-[3px] rounded-full lg:w-[5vw]">
                    <div class="ml-4 lg:ml-0">
                        <p class="text-Pale-Blue font-light lg:text-sm">Report for</p>
                        <h4 class="text-2xl lg:text-3xl font-light lg:mb-12 lg:w-[10vw]">Jeremy Robson</h4>
                    </div>
                </div>
                <div class="flex justify-around items-center p-5 text-Desaturated-blue lg:flex-col lg:items-start lg:space-y-4">
                    <a href="#" class="lg:hover:text-white ">Daily</a>
                    <a href="#" class="text-white ">Weekly</a>
                    <a href="#" class="lg:hover:text-white ">Monthly</a>
                </div>
            </div>
            <Card v-for="card in cards"
                :titulo="card.titulo" 
                :tempo-one="card.tempoOne" 
                :tempo-two="card.tempoTwo" 
                :corFundo="card.corFundo" 
                :imagemFundo="card.imagemFundo"
            />
        </div>
    </section>
</template>