<!-- appcardsactors-script-section -->
<script>
export default{
    name: "AppCardsActors",
    props: {
        actors: Object
    }
}
</script>
<!-- /appcardsactors-script-section -->

<!-- appcardsactors-template-section -->
<template>

    <!-- actors-section -->
    <div class="actors">
        <img :src="actors.img" :alt="actors.name">
        <div class="actors-description">
            <h2><strong>{{ actors.name }}</strong></h2>
            <h3>{{ actors.category }}</h3>
            <h4>{{ actors.status }}</h4>
        </div>
    </div>
    <!-- /actors-section -->

</template>
<!-- /appcardsactors-tempalte-section -->

<!-- appcardsactors-style-section -->
<style lang="scss">
@use "../styles/partials/variables" as *;

// actors-formatting-section
.actors{
    width: 100%;
    height: 100%;
    padding: 1em;
    background-color: $background-1;
    transition-duration: 1s;

    &:hover img{
        opacity: 1;
        width: 100%;
        border-radius: 300px;
        transform: scale(.9);
    }

    // img-formatting-section
    img{
        width: 100%;
        object-fit: cover;
        object-position: top;
        max-height: 333px;
        opacity: .5;
        border-radius: 0px;
        transition-duration: 1.5s;
    }

    // actors-description
    .actors-description{
        margin: 1em 0;
        text-align: center;

        // h2-tipography
        h2{
            font-size: 1.5rem;
            margin-bottom: 1em;
        }

        // h3-tipography
        h3{
            font-size: 1.3rem;
            color: $text-2;
        }

        // h4-tipography
        h4{
            font-size: 1rem;
            color: $text-2;
        }
    }
}
</style>
<!-- /appcardsactors-style-section -->