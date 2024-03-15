<template>
    <div class="table">
         <Titles />
         <Users />
    </div>
</template>
<script>
import Titles from '@/components/main/table/table-titles.vue';
import Users from '@/components/main/table/table-info.vue';

export default {
    components: {
        Titles,
        Users
    }
}
</script>
<style scoped>
.table {
    flex-grow: 1;
    margin-top: 28px;
    padding: 16px;
    border-radius: 12px;
    background: #fff;
    overflow: scroll;
}

.table::-webkit-scrollbar {
    height: 2px;
    width: 2px;
}

.table::-webkit-scrollbar-track {
    background: transparent;
}

.table::-webkit-scrollbar-thumb {
    background-color: #8F20EF;
    border-radius: 20px;
    border: 4px solid transparent;
}
</style>