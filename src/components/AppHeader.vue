<!-- COMPONENTE HEADER -->
<script>
export default {
    data() {
        return {
            // ARRAY LINKS NAVBAR
            links: [
                "CHARACTERS",
                "CHOMICS",
                "MOVIES",
                "CHARACTERS",
                "CHARACTERS",
                "CHARACTERS",
                "CHARACTERS",
                "CHARACTERS",
                "CHARACTERS",
                "CHARACTERS"
            ],

        }

    }
}

</script>

<template>
    <!-- CONTENITORE HEADER -->
    <header>
        <!-- NAVBAR HEADER -->
        <nav class="col">
            <div class="row boxed">
                <div class="col-2">
                    <!-- IMMAGINE LOGO -->
                    <img class="logo" src="../assets/img/dc-logo.png">
                </div>
                <div class="col-1 container-links">
                    <a href="" v-for="link in links">{{ link }}</a>
                </div>
            </div>


        </nav>

    </header>
</template>

<style>
nav{
    display: flex;
    justify-content: center;
}

.logo{
    width: 70px;
    padding: 1rem 0;
}

.container-links{
    display: flex;
    flex-direction: row;
    align-items: center;
    text-align: center;
}

a {
    padding: 1rem;
    font-size: 10px;
    text-decoration: none;
}
</style>
