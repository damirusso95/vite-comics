<!-- componente main -->
<script>
export default {
    data() {
        return {


            cards: [
                {
                    imageName: "buy-comics-digital-comics.png",
                    text: "Digital comics"
                },
                {
                    imageName: "buy-comics-merchandise.png",
                    text: "DC merchandaise"
                },
                {
                    imageName: "buy-comics-subscriptions.png",
                    text: "Subscrition"
                },
                {
                    imageName: "buy-comics-shop-locator.png",
                    text: "Comic shop locator"
                },
                {
                    imageName: "buy-dc-power-visa.svg",
                    text: "DC power visa"
                }

            ],


            fumetti: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                },
            ]

        }

    },

    methods: {
        getImage(nomefile) {
            return new URL(`../assets/img/${nomefile}`, import.meta.url);
        },
    }
}
</script>

<template>
    <main>
        <div class="container-fluid">

            <!-- PRIMA RIGA -->
            <div class="row">
                <div class="col-12 container-jumbo">
                    <!-- <img class="img-jumbo" src="../assets/img/jumbotron.jpg" alt=""> -->
                </div>
            </div>

            <!-- RIGA CARDS -->
            <div class="row">
                <div v-for="carte in fumetti" class="contenitore-gen">
                    <div>
                        <img class="cards-image" :src="carte.thumb" alt="">
                        <span>{{ carte.series }}</span>
                    </div>


                </div>
            </div>
            <!-- RIGA IMMAGINE + TESTO -->
            <div class="row blu">
                <div v-for="card in cards" class="col-2">
                    <div>
                        <img :src="getImage(card.imageName)" alt="Card Image" />
                        <span>{{ card.text }} </span>
                    </div>






                </div>
            </div>

        </div>
    </main>

</template>

<style scoped>
main {
    background-color: black;
    color: white;
}

img {
    width: 20%;
}
.cards-image{
    width: 100%;
    object-fit: cover;
}

.container-jumbo {
    height: 21rem;
    background-image: url('../assets/img/jumbotron.jpg');

}
.cards-container{
    width: 200px;
    height: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    
}
.contenitore-gen{
    width: 15%;
}

span {
    padding-left: 1rem;
}

.blu {
    justify-content: center;
    align-items: baseline;
    background-color: blue;
    padding: 4rem 0;
}
</style>