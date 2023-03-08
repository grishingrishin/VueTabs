<template>
    <transition name="fade" mode="out-in">
        <component :is="tag" class="ce-tabs__items">
            <slot />
        </component>
    </transition>
</template>

<script>
export default {
    name: 'CETabItems',
    props: {
        value: {
            type: [String, Number],
            default: '',
        },
        tag: {
            type: String,
            default: 'div',
        },
    },
};
</script>
