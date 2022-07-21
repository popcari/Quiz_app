<template>
   <div class="result">
        <div class="title">{{results[resultIndex].title}}</div>
        <div class="desc">
            {{results[resultIndex].desc}}
        </div>
    </div>
</template>

<script>
export default {
name: 'ResultCom',
props:["results","totalCorrect"],
data(){

},
methods:{

},
computed:{
    resultIndex(){
        let index = 0;
// e: element, i: item
this.result.forEach((e, i) => {
    if(e.min <= this.totalCorrect && e.max >= this.totalCorrect ){
        index = i;

    }
});

        return index;
    }
}
}
</script>

<style>

</style>