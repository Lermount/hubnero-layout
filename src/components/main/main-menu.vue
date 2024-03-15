<template>
    <main id="main">
        <InfoPanel />
        <AddButton />
        <Table />
        <Pagination />
    </main>
</template>
<script>
import InfoPanel from '@/components/main/info-panel.vue';
import AddButton from '@/components/main/add-button.vue';
import Table from '@/components/main/table/users-table.vue';
import Pagination from '@/components/main/pagination-panel.vue';

export default {
    components: {
        InfoPanel,
        AddButton,
        Table,
        Pagination
    }
}
</script>
<style scoped>
#main {
    display: flex;
    flex-direction: column;
    padding: 28px;
    height: calc(100vh - 105px);
    background: #F5F7FB;
    border-bottom-right-radius: 16px;
}

@media(max-width: 600px) {
    #main {
        border-top-left-radius: 16px;
    }
}
</style>