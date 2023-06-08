<template>
<div @click="click1">
    <slot name="dealPart1"></slot>
</div>
</template>

<script>
export default{
    name: "Deal"
}
</script>