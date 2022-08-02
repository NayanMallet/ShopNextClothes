<template>
    <header_bloc></header_bloc>
    <menu_bloc></menu_bloc>
    <mid_banner></mid_banner>
</template>
<script>
import header_bloc from '@/components/header_bloc.vue';
import menu_bloc from '@/components/menu_bloc.vue';
import mid_banner from '@/components/mid_banner.vue';
//import item_frame from "@/components/item_frame";

export default {
    name: 'App',
    components: {
        header_bloc,
        menu_bloc,
        mid_banner
        //item_frame
    }
}
</script>

<style>
</style>