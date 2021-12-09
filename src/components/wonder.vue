<template>


    <div>
    
    <h2>{{wonder.wonder}}</h2>
    <h3>{{wonder.Location}}</h3>
    <h4>{{wonder.by}}</h4>
    <h5> {{wonder.description}}</h5>


    </div>
</template>

<script>

export default{
    name: 'wonder',
    props:{
        wonder : JSON
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    background-color: #a1d4fd;
    color: black;
    padding: 1em;
}

.red{
background-color: orangered !important;

}


</style>