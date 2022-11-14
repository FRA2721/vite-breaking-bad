<!-- apploadingsection-script-section -->
<script>
export default{
    // name
    name: "AppLoadingSection"
}
</script>
<!-- /apploadingsection-script-section -->

<!-- apploadingsection-template-section -->
<template>

    <!-- loader-container -->
    <div class="loader-container">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/77/Breaking_Bad_logo.svg/1280px-Breaking_Bad_logo.svg.png" alt="breaking bad logo">
        <h2>Wait a minute...</h2>
        <div class="loader"></div>
    </div>
    <!-- /loader-container-section -->

</template>
<!-- /apploadingsection-template-section -->

<!-- apploadingsection-style-section -->
<style lang="scss">

// loader-container-formatting-section
.loader-container{
    width: 100%;
    height: 10vh;
    display: flex;
    align-items: center;
    justify-content: center;

    .loader {
        border: 10px solid #f3f3f3;
        border-top: 10px solid green;
        border-radius: 50%;
        width: 100px;
        height: 100px;
        animation: spin .5s linear infinite;
        margin-top: 300px;
        margin-left: -200px;
        }

        @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
        }

    // img-formatting-section
    img{
        width: 100px;
        display: flex;
        padding: 1.5em 1.5em;
        align-items: center;
    }

    // h1-tipography
    h2{
        color: hsl(120, 100%, 25%);
    }
}
</style>
<!-- /apploadingsection-style-section -->