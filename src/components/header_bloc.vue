<template>
<div id="header_bloc">
    <div id="menu">
      <svg id="tab_button" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h8m-8 6h16" />
      </svg>
      <svg id="search_button" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
      </svg>
    </div>
      <h1 id="header_text">Shop Next Clothes</h1>
</div>
</template>

<script>
export default {
    name: "header_bloc"
}
</script>

<style scoped>
#header_bloc {
    margin:0;
    padding:0;
    width: 100%;
    height: 230px;

    display: flex;
    flex-direction: column;

    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.5) 100%), url('../assets/header_bloc_background.png');
    background-size: cover;
    background-position: center;
    mix-blend-mode: normal;

}

#menu {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin: 25px 0 15px 0;

    width: 100%;
}

#tab_button, #search_button {
    width: 35px;
    height: 35px;

    flex: none;
    order: 0;
    flex-grow: 0;

    color: #FFFFFF;
}

#tab_button {
    margin-left: 30px;
}

#search_button {
    margin-right: 30px;
}

#header_text{
    margin: 0 auto;
    width: 100px;

    font-style: normal;
    font-weight: 600;
    font-size: 40px;
    line-height: 30px;

    color: #FFFFFF;
}



</style>