<!-- appcardsactorslist-script-section -->
<script>
import AppCardsActors from './AppCardsActors.vue';
import { store } from '../store';
export default{
    // name
    name: "AppCardsActorsList",
    components:{
        AppCardsActors,
    },
    data(){
        return {
            // store-code
            store,
        }
    }
}
</script>
<!-- /appcardsactorslist-script-section -->

<!-- appcardsactorslist-tempalte-section -->
<template>

    <!-- choice-container -->
    <div class="container">

        <!-- choice -->
        <select class="choice">
            <option value>Select your category</option>
            <option value="1">category-1</option>
            <option value="2">category-2</option>
            <option value="3">category-3</option>
            <option value="4">category-4</option>
            <option value="5">category-5</option>
        </select>
        <!-- /choice -->

        <!-- actors-container -->
        <div class="actors-container">
            <div class="actors-founded">Founded {{ store.actors.length }} actors</div>
            <div class="actors-card row row-cols-xl-5 g-4" >
                <div class="col" v-for="actor in store.actors" :key="actor.actors_id">
                    <AppCardsActors :actors="actor" />
                </div>
            </div>
        </div>
        <!-- /actors-container -->

    </div>
    <!-- /choice-container -->
</template>
<!-- /appcardsactorslist-template-section -->

<!-- appcardsactorslist-style-section -->
<style lang="scss">
@use "../styles/partials/variables" as *;

// container-formatting-section
.container{
    margin: 3em 0;

    // form-formatting-section
    .choice{
        color: green;
        max-width: 333px;
        border-radius: 50px;
        border: 3px solid green;
    }

    select{
        transition-duration: 1s;
        cursor: pointer;
    
        &:hover{
            color: white;
            background-color: green;
        }   
    }

    // actors-container-formatting-section
    .actors-container{
        padding: 3em;
        margin: 3em 0;
        background-color: $background-2;

        // actor-founded
        .actors-founded{
            padding: 1em;
            background-color: $background-banner-section;
        }

        // actors-cards
        .actors-card{
            margin: 1em 0;
        }
    }
}
</style>
<!-- /appcardsactorslist-style-section -->