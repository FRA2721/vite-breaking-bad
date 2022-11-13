<!-- appheader-script-section -->
<script>
export default{
    // name
    name: "AppHeader",
}
</script>
<!-- /appheader-script-section -->

<!-- appheader-template-section -->
<template>

    <!-- header-section -->
    <header>
        <!-- logo-&-header -->
        <div class="logo">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/77/Breaking_Bad_logo.svg/1280px-Breaking_Bad_logo.svg.png" alt="Logo Breaking bad">
            <h1>Breaking Bad Api</h1>
        </div>
        <!-- logo-&-header -->
    </header>
    <!-- /header-section -->

</template>
<!-- /appheader-template-section -->

<!-- appheader-style-section -->
<style lang="scss">
@use "../styles/partials/variables" as *;

// logo-formatting-section
.logo {
    display: flex;
    padding: 1.5em 1.5em;
    align-items: center;

    // img
    img {
        width: 100px;
    }

    // h1-tipography
    h1{
        margin-left: 1em;
        font-size: 2rem;
        transition-duration: 1s;

        &:hover{
            color: hsl(120, 100%, 25%);
        }
    }
}
</style>
<!-- /appheader-style-section -->