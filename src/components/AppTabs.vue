<template>
    <component :is="tag" class="ce-tabs">
        <slot />
    </component>
</template>

<script>
export default {
    name: 'CETabs',
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
    provide() {
        return {
            getActiveTabId: () => this.activeTabId,
            changeActiveTabId: this.changeActiveTabId,
        };
    },
    data() {
        return {
            activeTabId: null,
        };
    },
    created() {
        this.activeTabId = this.value;
    },
    methods: {
        changeActiveTabId(tabId) {
            this.activeTabId = tabId;
        },
    },
};
</script>
