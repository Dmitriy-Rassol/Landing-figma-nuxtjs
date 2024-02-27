<template>
    <div class="selector">
        <div :class="{ item: true, active: selected == 0 }" data-id="0" @click="select">Figma for design +
            prototyping</div>
        <div :class="{ item: true, active: selected == 1 }" data-id="1" @click="select">FigJam for whiteboarding</div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            selected: 0,
        };
    },
    methods: {
        select(event) {
            this.selected = event.target.dataset['id'];
            this.$emit('setType', this.selected);
        }
    }
}
</script>
<style>
.selector {
    border-radius: 8px;
    background: rgb(229, 229, 229);
    display: inline-flex;
    padding: 4px;
}

.item {
    padding: 12px 14px;
}

.item.active {
    background: rgb(255, 255, 255);
    border-radius: 5px;
}
</style>