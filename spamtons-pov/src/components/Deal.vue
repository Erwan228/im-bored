<template>
    <div @click="click1">
        <slot name="dealPart1"></slot>
    </div>
    <div @click="click2">
    <slot name="dealPart2"></slot>
    </div>
    <div @click="click3">
    <slot name="dealPart3"></slot>
    </div>
</template>

<script>
export default{
    name: "Deal",
    methods: {
        click1() {
            this.$emit('clickDeal1')
        },
        click2(){
            this.$emit('clickDeal2')
        },
        click3(){
            this.$emit('clickDeal3')
        }
    }
}
</script>

<style>

</style>