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
                <div class="col">
                    <h2 class="text-center py-5">qui andrà il contenuto</h2>
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
img{
    width: 20%;
}
span{
    padding-left: 1rem;
}

.blu {
    justify-content: center;
    align-items: baseline;
    background-color: blue;
    padding: 4rem 0;
}
</style>