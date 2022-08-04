<template>
    <div class="search_tab">
        <div class="sc_header">
            <div class="sc_box">
                <input class="search_input" type="text">
                <svg class="search_button" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                </svg>
            </div>
            <hr>
        </div>
        <div class="sc_body">
        </div>
        <svg class="close_button" @click="closeMenu" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
        </svg>
    </div>
</template>

<script>
export default {
    name: "search_tab",
    methods: {
        closeMenu: function () {
                document.querySelector(".search_tab").style.display="none";
        }
    }
}
</script>

<style scoped>

</style>