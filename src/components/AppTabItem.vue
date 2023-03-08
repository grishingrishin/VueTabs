<template>
    <component
        :is="tag"
        v-show="isActive"
        class="ce-tabs__item"
        :class="{
            'ce-tabs__item--active': isActive,
        }"
    >
        <slot />
    </component>
</template>

<script>
export default {
    name: 'CETabItem',
    props: {
        tabId: {
            type: [String, Number],
            default: '',
        },
        tag: {
            type: String,
            default: 'div',
        },
    },
    inject: {
        getActiveTabId: {
            default: () => {},
        },
    },
    computed: {
        isActive() {
            return this.tabId === this.getActiveTabId();
        },
    },
};
</script>
