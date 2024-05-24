<script>
export default {
    data() {
        return {
            // ARRAY LINKS NAVBAR
            linksFooter: [
                "Characters",
                "Comics",
                "Movies",
                "Tv",
                "Games",
                "Videos",
                "News"
            ],

        }

    }
}
</script>

<template>
    <footer>
        <div class="container-fluid bg-footer">
            <div class="container">
                <div class="row">

                    <div class="col-2">
                        <h2>DC comics</h2>
                        <ul v-for="linkFooter in linksFooter">
                            <li>
                                {{ linkFooter }}
                            </li>
                        </ul>

                    </div>
                    <div class="col-2">
                        <h2>DC</h2>
                        <ul v-for="linkFooter in linksFooter">
                            <li>
                                {{ linkFooter }}
                            </li>
                        </ul>
                    </div>
                    <div class="col-2">
                        <h2>Sites</h2>
                        <ul v-for="linkFooter in linksFooter">
                            <li>
                                {{ linkFooter }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <div class="container-fluid last">
            <div class="container">
                <div class="row">
                    <div class="col-3">
                        <button>SING-UP NOW!</button>
                    </div>
                    <div class="col-3">
                        <h2>FOLLOW US</h2>
                    </div>
                    <div class="col-3">
                        immagini
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped>
footer {
    color: aliceblue;
}

.bg-footer {
    background-image: url(../assets/img/footer-bg.jpg);
    height: 350px;
}

ul {
    list-style: none;
    padding: 0;
}

.last {
    background-color: darkgray;
    color: aliceblue;
}
</style>