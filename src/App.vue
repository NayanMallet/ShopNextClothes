<template>
    <header_bloc></header_bloc>
    <menu_bloc></menu_bloc>
    <mid_banner></mid_banner>
    <item_frame class="item" :item='{
            name: "Hoodie Zip Violet",
            size: "M",
            price: "20,00 €",
            brand: "CARHARTT",
            link: "https://www.vinted.fr/hommes/vetements/sweats-and-pulls/pulls-a-capuche-avec-zip/1743748226-sweat-zip-carahartt",
            imageUrl: "https://images1.vinted.net/t/03_0256f_8WeQmpNc3Ar5ATnLMcnRTtg7/f800/1649507870.jpeg?s=b1616fd9df9a9eef397c8458c71981e886927448"
        }'></item_frame>
</template>
<script>
import header_bloc from '@/components/header_bloc.vue';
import menu_bloc from '@/components/menu_bloc.vue';
import mid_banner from '@/components/mid_banner.vue';
import item_frame from "@/components/item_frame";

export default {
    name: 'App',
    components: {
        header_bloc,
        menu_bloc,
        mid_banner,
        item_frame
    }
}
</script>

<style>
</style>