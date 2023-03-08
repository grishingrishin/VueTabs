<template>
    <component :is="tag" class="ce-tabs__tab">
        <button
            type="button"
            class="ce-tabs__btn"
            :class="{
                'ce-tabs__btn--active': isActive,
            }"
            @click="changeActiveTabId(tabId)"
        >
            <slot />
        </button>
    </component>
</template>

<script>
export default {
    name: 'CETab',
    props: {
        tabId: {
            type: [String, Number],
            default: '',
        },
        tag: {
            type: String,
            default: 'li',
        },
    },
    inject: {
        getActiveTabId: {
            default: () => {},
        },
        changeActiveTabId: {
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

<style>
.ce-tabs__tab {
    flex: 1;
}

.ce-tabs__btn {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-height: 40px;
    color: #677b87;
    border: none;
    background: transparent;
    border-radius: 8px;
}

.ce-tabs__btn:hover {
    background-color: #f7fcfe;
}

.ce-tabs__btn--active {
    color: #41ACE8;
    background-color: #fff;
}
</style>
