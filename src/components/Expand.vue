<template>
    <section id="expand">
        <div id="expand-title" :class="{open:open}" @click="toggleExpand">
            <slot name="title"></slot>
            <p id="arrow">></p>
        </div>
        <transition name="translateY">
            <div id="expand-content" v-show="open">
                <slot></slot>
            </div>
        </transition>
    </section>
</template>

<script>
export default {
    data() {
        return {
            open: false
        }
    },
    methods: {
        toggleExpand() {
            this.open = !this.open
        }
    }
}
</script>

<style>
#expand {
    width: 100%;
    margin-top: 30px;
    background-color: var(--background-color-secondary);
    display: flex;
    flex-direction: column;
    border-radius: 1ch;
}

#expand-title {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 0px 30px;
    cursor: pointer;
}

.open #arrow{
    transform: rotate(-90deg);
}

#expand-title p {
    margin: 0px;
    font-size: 1em;
    height: fit-content;
}

#arrow {
    font-size: 3em !important;
    font-family: 'VT323', monospace;
    transform: rotate(90deg);
}

#expand-content p {
    font-size: 1em;
    margin: 0px 0px 0px 30px;
}
</style>