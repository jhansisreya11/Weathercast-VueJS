<template>
    <div class="box">
        <h1 class="h1-style"> {{appName}} </h1>
        <h3 class="h2-style"> {{dateOfReport}} </h3>
        <h4 class="h3-style"> {{myName}} </h4>
    </div>
</template>

<script>
    export default{
    name: 'MyHeader',
    props:{
    appName: String,
    dateOfReport: String,
    myName: String
    }
}

</script>

<style scoped>
.box{
    margin: 20px 0;
    text-align: center;
    font-family: 'Montserrat', sans-serif;
    margin-bottom: 10px;
}
.h1-style{
    margin: 10px;
}
.h2-style{
    margin: 10px;
}
.h3-style{
    margin: 10px;
}
</style>