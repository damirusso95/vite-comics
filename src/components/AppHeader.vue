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
        <nav class="navbar navbar-light bg-dark">
            <div class="container-fluid">
                <a class="navbar-brand" href="#">
                    <!-- IMMAGINE LOGO -->
                    <img src="../assets/img/dc-logo.png" alt="" width="30" height="24" class="d-inline-block align-text-top">
                </a>
                <!-- LINKS NAVBAR CON V-FOR -->
                <a href="" v-for="link in links">{{ link }}</a>
            </div>
        </nav>

    </header>
</template>

<style></style>
