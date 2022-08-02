<template>
    <div class="menu_bloc">
        <div class="menu_top">
            <h1>Shop Next Clothes</h1>
            <svg class="close_button" @click="closeMenu" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
        </div>
        <div class="menu_nav">
            <a class="home_link" href="#">HOME</a>
            <a class="contact_link" href="#">CONTACT</a>
        </div>
    </div>
</template>

<script>
export default {
    name: "menu_bloc",
    methods: {
        closeMenu: function () {
            if (document.querySelector(".menu_bloc").style.display === "inline-flex") {
                document.querySelector(".menu_bloc").style.display="none";
            } else {
                document.querySelector(".menu_bloc").style.display="inline-flex";
            }
        }
    }
}
</script>

<style scoped>
</style>