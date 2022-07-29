<template>
    <div class="sticky">
        <header_bloc></header_bloc>
        <articles_banner></articles_banner>
    </div>
    <div id="items_scroll">
        <ul class="scrolling">
            <item_frame class="item" :item='{
            name: "Hoodie Zip Violet",
            size: "M",
            price: "20,00 €",
            brand: "CARHARTT",
            link: "https://www.vinted.fr/hommes/vetements/sweats-and-pulls/pulls-a-capuche-avec-zip/1743748226-sweat-zip-carahartt",
            imageUrl: "https://images1.vinted.net/t/03_0256f_8WeQmpNc3Ar5ATnLMcnRTtg7/f800/1649507870.jpeg?s=b1616fd9df9a9eef397c8458c71981e886927448"
        }'></item_frame>
            <item_frame class="item" :item='{
            name: "Hoodie Zip Violet",
            size: "M",
            price: "20,00 €",
            brand: "CARHARTT",
            link: "https://www.vinted.fr/hommes/vetements/sweats-and-pulls/pulls-a-capuche-avec-zip/1743748226-sweat-zip-carahartt",
            imageUrl: "https://images1.vinted.net/t/03_0256f_8WeQmpNc3Ar5ATnLMcnRTtg7/f800/1649507870.jpeg?s=b1616fd9df9a9eef397c8458c71981e886927448"
        }'></item_frame>
            <item_frame class="item" :item='{
            name: "Hoodie Zip Violet",
            size: "M",
            price: "20,00 €",
            brand: "CARHARTT",
            link: "https://www.vinted.fr/hommes/vetements/sweats-and-pulls/pulls-a-capuche-avec-zip/1743748226-sweat-zip-carahartt",
            imageUrl: "https://images1.vinted.net/t/03_0256f_8WeQmpNc3Ar5ATnLMcnRTtg7/f800/1649507870.jpeg?s=b1616fd9df9a9eef397c8458c71981e886927448"
        }'></item_frame>
            <item_frame class="item" :item='{
            name: "Hoodie Zip Violet",
            size: "M",
            price: "20,00 €",
            brand: "CARHARTT",
            link: "https://www.vinted.fr/hommes/vetements/sweats-and-pulls/pulls-a-capuche-avec-zip/1743748226-sweat-zip-carahartt",
            imageUrl: "https://images1.vinted.net/t/03_0256f_8WeQmpNc3Ar5ATnLMcnRTtg7/f800/1649507870.jpeg?s=b1616fd9df9a9eef397c8458c71981e886927448"
        }'></item_frame>
        </ul>
    </div>

</template>

<script>
import header_bloc from '@/components/header_bloc.vue'
import articles_banner from '@/components/articles_banner.vue'
import item_frame from "@/components/item_frame";

export default {
    name: 'App',
    components: {
        header_bloc,
        articles_banner,
        item_frame
    }
}
</script>

<style>

#app, html {
    margin:0;
    padding:0;
    width: 100%;
    height: 100%;
    font-family: 'Montserrat',sans-serif;
}

#items_scroll {
    display: grid;
    grid-gap: 15px;
    align-content: start;
}

#items_scroll > .scrolling {
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

















</style>
