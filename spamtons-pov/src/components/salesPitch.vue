<template>
    <div @click="showNext1">
    <slot name="salesPitch1" @click="showNext1"></slot>
    </div>
    <div @click="showNext2">
    <slot name="salesPitch2" @click="showNext2"></slot>
    </div>
    <div @click="showNext3">
    <slot name="salesPitch3" @click="showNext3"></slot>
    </div>
</template>

<script>
export default {
    name: "salesPitch",
    methods: {
        showNext1(){
            this.$emit('showNext1')
        },
        showNext2(){
            this.$emit('showNext2')
        },
        showNext3(){
            this.$emit('showNext3')
        },
    }
}
</script>