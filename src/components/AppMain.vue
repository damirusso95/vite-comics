<!-- componente main -->
<script>
export default {
    data() {
        return {

            cards: [
                {
                    image: "dc-logo.png",
                    text: "prova"
                },
                {

                    text: "prova"
                },
                {

                    text: "prova"
                },
                {

                    text: "prova"
                },
                {

                    text: "prova"
                },
                {

                    text: "prova"
                }

            ]

        }

    },
    methods: {
        getImg(path) {
            let risultato = new URL("../assets/img/" + path, import.meta.url);
            return risultato.href;
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
                    <div>{{ card.text }} 
                        <img :src="getImg(image)" alt="">
                    

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

.blu {
    background-color: blue;
    padding: 4rem 0;
}
</style>