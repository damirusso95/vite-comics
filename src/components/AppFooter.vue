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
        <div class="container-fluid">
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
    </footer>
</template>

<style scoped>
footer {
    color: aliceblue;
}

.container-fluid {
    background-image: url(../assets/img/footer-bg.jpg);
    height: 350px;
}

ul {
    list-style: none;
    padding: 0;
}
</style>