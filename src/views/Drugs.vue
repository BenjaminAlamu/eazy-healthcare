<template>
    <div class="pt-32">
        <p class="text-center title-text m-2">Drug Listing</p>
        <div class="flex flex-wrap">
            <div class="w-full md:w-1/4" v-for="i in 16" :key="i">
                <DrugCard class="m-2" />
            </div>
        </div>
    </div>
</template>

<script>
import DrugCard from "@/components/DrugCard.vue";
    export default {
        components:{
            DrugCard
        }
    }
</script>

<style scoped>
.title-text{
    font-size: 36px;
line-height: 59px;
text-align: center;
}

</style>