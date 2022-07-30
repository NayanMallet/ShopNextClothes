<template>
    <div class="item_frame variant2">
        <div class="frame3">
            <h1>Redirection sur Vinted</h1>
            <div class="lds-spinner">
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
            </div>
        </div>
    </div>
    <div class="item_frame" @click="variantChange(item.link)" :style="'background: linear-gradient(180deg, rgba(0, 0, 0, 0) 42.91%, #000000 118.2%), url(' + item.imageUrl + ') center'">
        <div class="texts">
            <div class="upper_part">
                <h1 class="clothing_name">{{ item.name }}</h1>
                <div class="frame1">
                    <p class="clothing_size">{{ item.size }}</p>
                    <svg width="5" height="10" viewBox="0 0 5 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M3.28125 7.8125C3.19492 7.8125 3.125 7.74957 3.125 7.67188V7.39062C3.125 7.31293 3.19492 7.25 3.28125 7.25H5V6.125H3.28125C3.19492 6.125 3.125 6.06207 3.125 5.98438V5.70312C3.125 5.62543 3.19492 5.5625 3.28125 5.5625H5V4.4375H3.28125C3.19492 4.4375 3.125 4.37457 3.125 4.29688V4.01562C3.125 3.93793 3.19492 3.875 3.28125 3.875H5V2.75H3.28125C3.19492 2.75 3.125 2.68707 3.125 2.60938V2.32812C3.125 2.25043 3.19492 2.1875 3.28125 2.1875H5V1.0625C5 0.751895 4.72012 0.5 4.375 0.5H0.625C0.279883 0.5 0 0.751895 0 1.0625V8.9375C0 9.24811 0.279883 9.5 0.625 9.5H4.375C4.72012 9.5 5 9.24811 5 8.9375V7.8125H3.28125Z"
                            fill="white"/>
                    </svg>
                </div>
            </div>
            <div class="frame2">
                <p class="clothing_brand">{{ item.brand }}</p>
                <p class="clothing_price">{{ item.price }}</p>
            </div>
        </div>
    </div>
</template>

/*
<div class="items_scroll">
<ul class="scrolling">
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
*/


<script>
export default {
    name: "item_frame",
    props: ['item'],
    methods: {
        goToUrl: async function (url) {
            window.open(url, '_blank');
            document.querySelector('.item_frame:not(#variant2)').style.display = 'block';
            document.querySelector('#variant2').style.display = 'none';
        },
        variantChange: async function (url) {
            document.querySelector('.item_frame:not(#variant2)').style.display = 'none';
            document.querySelector('#variant2').style.display = 'block';
            setTimeout(() => {
                this.goToUrl(url);
            }, 1000);

        }
    }
}
</script>

<style scoped>
.item_frame {
    width: 260px;
    height: 420px;
    border-radius: 30px;
}

.item_frame:not(#variant2){
    background-size: cover !important;
    display: block;
}

.texts {
    padding: 300px 20px 40px 20px;
    width: 220px;
    height: 80px;
    margin: 0;
}

.upper_part{
    display: flex;
    flex-direction: row;
    padding-bottom: 5px;
}

.clothing_name {
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 29px;
    color: #FFFFFF;

    width: 160px;
    height: 60px;
    padding: 0;
    margin: 0;
}

.frame1 {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;

    width: 22px;
    height: 16px;
    padding: 0;
    gap: 5px;
    margin: auto 0 0 auto;

}

.clothing_size {
    width: 12px;
    height: 16px;

    font-style: normal;
    font-weight: 400;
    font-size: 13px;
    line-height: 16px;

    text-align: right;
    text-transform: capitalize;

    color: #FFFFFF;

    flex: none;
    order: 0;
    flex-grow: 0;
    margin: 0;
}

.frame1 svg {
    width: 5px;
    height: 9px;

    flex: none;
    order: 1;
    flex-grow: 0;
    padding-bottom: 2px;
}

.frame2 {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
    padding: 0;
    gap: 13px;

    width: 220px;
    height: 17px;

}

.clothing_brand {
    margin: 0;
    width: fit-content;
    height: 17px;
    text-align: left;

    font-style: normal;
    font-weight: 300;
    font-size: 13px;
    line-height: 16px;

    color: #FFFFFF;

    flex: none;
    order: 0;
    flex-grow: 0;
}

.clothing_price {
    margin: 0 0 0 auto;
    height: 17px;

    font-style: normal;
    font-weight: 700;
    font-size: 14px;
    line-height: 17px;

    text-align: right;


    color: #FFFFFF;


    flex: none;
    order: 1;
    flex-grow: 0;
}



.variant2 {
    background: #80C5F8;
    display: none;
}

.frame3 {
    display: flex;
    flex-direction: column;
    align-items: center;

    width: 210px;
    height: 140px;
    padding: 140px 25px;
    gap: 30px;
}

.frame3 h1 {
    width: 210px;
    height: 60px;
    padding: 0;
    margin: 0;

    font-family: 'Montserrat', sans-serif;
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 29px;
    text-align: center;

    color: #FFFFFF;

    flex: none;
    order: 0;
    flex-grow: 0
}

.frame3 svg {
    width: 48px;
    height: 48px;

    flex: none;
    order: 1;
    flex-grow: 0;

    padding: 0;

}

.lds-spinner {
    color: #FFFFFF;
    display: inline-block;
    position: relative;
    width: 30px;
    height: 30px;
}
.lds-spinner div {
    transform-origin: 15px 15px;
    animation: lds-spinner 1.2s linear infinite;
}
.lds-spinner div:after {
    content: " ";
    display: block;
    position: absolute;
    top: 2px;
    left: 19px;
    width: 3px;
    height: 9px;
    border-radius: 10%;
    background: #fff;
}
.lds-spinner div:nth-child(1) {
    transform: rotate(0deg);
    animation-delay: -1.1s;
}
.lds-spinner div:nth-child(2) {
    transform: rotate(30deg);
    animation-delay: -1s;
}
.lds-spinner div:nth-child(3) {
    transform: rotate(60deg);
    animation-delay: -0.9s;
}
.lds-spinner div:nth-child(4) {
    transform: rotate(90deg);
    animation-delay: -0.8s;
}
.lds-spinner div:nth-child(5) {
    transform: rotate(120deg);
    animation-delay: -0.7s;
}
.lds-spinner div:nth-child(6) {
    transform: rotate(150deg);
    animation-delay: -0.6s;
}
.lds-spinner div:nth-child(7) {
    transform: rotate(180deg);
    animation-delay: -0.5s;
}
.lds-spinner div:nth-child(8) {
    transform: rotate(210deg);
    animation-delay: -0.4s;
}
.lds-spinner div:nth-child(9) {
    transform: rotate(240deg);
    animation-delay: -0.3s;
}
.lds-spinner div:nth-child(10) {
    transform: rotate(270deg);
    animation-delay: -0.2s;
}
.lds-spinner div:nth-child(11) {
    transform: rotate(300deg);
    animation-delay: -0.1s;
}
.lds-spinner div:nth-child(12) {
    transform: rotate(330deg);
    animation-delay: 0s;
}
@keyframes lds-spinner {
    0% {
        opacity: 1;
    }
    100% {
        opacity: 0;
    }
}

</style>