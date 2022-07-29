<template>
<div id="articles_banner">
    <h1>NEW ARRIVALS</h1>
</div>
</template>

<script>
export default {
    name: "articles_banner"
}
</script>

<style scoped>
#articles_banner {
    width: 100%;
    height: 42px;


    text-align: center;

    background: #F9F6F6;
    box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.25);
}

#articles_banner h1 {
    display: -webkit-inline-box;
    margin: 13.5px 0;

    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;

    width: fit-content;

    color: #000000;
}
</style>