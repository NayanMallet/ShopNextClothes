<template>
    <header_bloc></header_bloc>
    <menu_bloc></menu_bloc>
</template>
<script>
import header_bloc from '@/components/header_bloc.vue';
import menu_bloc from '@/components/menu_bloc.vue';
//import articles_banner from '@/components/articles_banner.vue';
//import item_frame from "@/components/item_frame";

export default {
    name: 'App',
    components: {
        header_bloc,
        menu_bloc
        //articles_banner,
        //item_frame
    }
}
</script>

<style>

#app, html, body {
    margin:0;
    padding:0;
    width: 100%;
    height: 100%;
    font-family: 'Montserrat',sans-serif;
}

.items_scroll {
    display: grid;
    grid-gap: 15px;
    align-content: start;
}

.items_scroll > .scrolling {
    grid-column: 2 / -2;
}

.scrolling {
    display: grid;
    grid-gap: 15px;
    grid-template-columns: 10px;
    grid-template-rows: minmax(150px, 1fr);
    grid-auto-flow: column;
    grid-auto-columns: calc(50% - var(--gutter) * 2);

    overflow-x: scroll;
    scroll-snap-type: x proximity;
    margin: 15px 0;
    padding: 0;

    list-style: none;
}

.scrolling::-webkit-scrollbar {
    display: none;
}

.scrolling:before, .scrolling:after {
    content: '';
    width: 10px;
}

.scrolling > .item, .item {
    scroll-snap-align: center;
    padding: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.sticky {
    position: sticky;
    top: 0;
    width: 100%
}

* {
    box-sizing: border-box !important;
}

</style>