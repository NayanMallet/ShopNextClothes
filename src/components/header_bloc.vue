<template>
    <div class="header_bloc">
        <div class="nav_menu">
            <svg class="tab_button" @click="openMenu" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h8m-8 6h16" />
            </svg>
            <svg class="search_button" @click="openSearch" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
        </div>
        <h1>Shop Next Clothes</h1>
    </div>
</template>

<script>
export default {
    name: "header_bloc",
    methods: {
        openMenu: function () {
            document.querySelector(".menu_bloc").style.display = "inline-flex";
        },
        openSearch: function () {
            document.querySelector(".search_tab").style.display = "block";
        }
    }
}
</script>

<style scoped>
</style>