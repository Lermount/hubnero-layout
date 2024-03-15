<template>
    <ul class="table-titles">
        <li v-for="title in tibleTitles" :key="title.id" class="table-header">
            <img v-if="title.search" class="title-icon" :src="title.search" alt="search">
            <img v-if="title.cross" class="title-icon" :src="title.cross" alt="cross">
            <p class="title-name">{{ title.name }}</p>
            <span v-if="title.arrowTop || title.arrowBottom" class="arrows">
                <img class="arrow arrow-top" :src="title.arrowTop" alt="top">
                <img class="arrow arrow-bottom" :src="title.arrowBottom" alt="bottom">
            </span>
            <img v-if="title.dropdown" class="title-dropdown" :src="title.dropdown" alt="dropdown">
        </li>
    </ul>
</template>
<script>
import { tibleTitles } from '@/assets/tableTitles';

export default {
    data: () => ({
        tibleTitles
    }),
}
</script>

<style scoped>
.table-titles {
    display: grid;
    grid-template-rows: repeat(1, 1fr);
    grid-template-columns: repeat(8, 1fr);
    max-width: 1760px;
    min-width: 1420px;
    padding: 0px 16px;
    border-radius: 12px;
    background: #F5F7FB;
}

.table-header {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    min-height: 64px;
    padding-right: 16px;
}

.table-header:not(:first-child) {
    padding-left: 16px;
}

.table-header:not(:last-child) {
    border-right: 1px solid #E5E8EF;
}

.title-icon {
    width: 20px;
    height: 20px;
    margin-right: 4px;
    cursor: pointer;
}

.title-name {
    margin-right: 4px;
    font-family: Commissioner-Medium;
    font-size: 12px;
    font-weight: 500;
    line-height: 16px;
    letter-spacing: 0em;
    text-align: left;
    color: #2A355A;
}

.arrows {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    width: 20px;
    height: 20px;
}

.arrow {
    cursor: pointer;
}

.title-dropdown {
    margin-left: auto;
    width: 20px;
    height: 20px;
    border-radius: 6px;
    cursor: pointer;
}
</style>