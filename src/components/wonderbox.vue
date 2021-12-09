<template>
    
     <div class="wonderbox">
         
        <div v-for="wonder in wonders" :key="wonder.id" >
                
                <wonder :wonder="wonder"/>
        </div>

     </div>

</template>

<script>

import wonder from "./wonder.vue"
export default{

    name: 'wonderbox',
    components: {
        wonder
    },
    props: {
        wonders: JSON
    }

}

</script>


<style>

.wonderbox{

    background-color: rgb(63, 11, 14);
    padding: 1em;
    color: gray;
}
</style>