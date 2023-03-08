<template>
    <component :is="tag" class="ce-tabs__tabs">
        <slot />
    </component>
</template>

<script>
export default {
    name: 'CETabNav',
    props: {
        tag: {
            type: String,
            default: 'ul',
        },
    },
};
</script>

<style>
.ce-tabs__tabs {
    display: flex;
    margin-bottom: 16px;
    padding: 4px;
    font-weight: 700;
    background-color: #eceff0;
    border-radius: 12px;
    list-style: none;
}
</style>
