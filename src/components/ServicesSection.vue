<template >
    <section class="text-white mt-20" id="services">
        <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-white mb-4">My Services</h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3">
            <div v-for="service in services" :key="service.id" data-aos="fade-up"
            class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
            >
                <div class="mx-auto h-24 w-24 text-center xl:h-28 xl:w-28">
                    <div>
                        <img :src="service.icon" alt="service icon">
                    </div>
                </div>
                <div class="text-center">
                    <h3 class="pt-8 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                        {{ service.name }}
                    </h3>
                    <p class="text-grey pt-4 text-sm group-hover:text-white md:text-base">
                        {{ service.description }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import {ref} from 'vue';
const services =ref([
    {
        id:1,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/google-code.png',
        name:'WEB DEVELOPMENT',
        description:'Podemos desenvolver Back-ends eficientes para sua empresa com consumos de WEB APIs.'
    },
    {
        id:2,
        icon:'https://img.icons8.com/external-vectorslab-glyph-vectorslab/100/fffeee/external-Technical-Writing-mobile-app-development-vectorslab-glyph-vectorslab.png',
        name:'Settings',
        description:'Podemos criar configurações específicas para seu negócio. '
    },
    {
        id:3,
        icon:'https://img.icons8.com/external-solid-design-circle/100/ffffff/external-Mobile-Development-digital-marketing-solid-design-circle.png',
        name:'Mobile Development',
        description:'Muitos négocios como restaurantes optam pelas tecnologias de cardápio digital para facilitar os pedidos.'
    },
    {
        id:4,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/email-open.png',
        name:'WEB SITES - LANDING PAGE',
        description:'Um novo visual para atrair clientes na palma da sua mão com websites nos navegaroes para poderem achar sua empresa no mundo digital.'
    },
    {
        id:5,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png',
        name:'Graphic Design',
        description:'Podemos criar sua logotipo para sua empresa!'
    },
    {
        id:6,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/web-design.png',
        name:'SYSTEM',
        description:'Criação de sistemas como sistemas de administraçaõ para empresas e para gerência de RH.'
    },
    ])
</script>

