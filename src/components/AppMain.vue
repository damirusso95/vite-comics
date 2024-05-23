<!-- componente main -->
<script>
export default {
    data() {
        return {
            
            cards: [
                {
                    image: ,
                    text: "prova"
                },
                {
                    image: ,
                    text: "prova"
                },
                {
                    image: ,
                    text: "prova"
                },
                {
                    image: ,
                    text: "prova"
                },
                {
                    image: ,
                    text: "prova"
                },
                {
                    image: ,
                    text: "prova"
                }
                
            ]

        }

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
            <div class="row">
                <div v-for="card in cards" class="col-2">
                    <div>{{card.text}}</div>
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
</style>