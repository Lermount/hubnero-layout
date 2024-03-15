<template>
    <i class="burder-menu">
        <svg class="burder-menu-icon" width="16" height="12" viewBox="0 0 16 12" fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <rect x="0.000999451" y="0.5" width="16" height="1" rx="0.5" fill="#2A355A" />
            <rect x="0.000999451" y="5.5" width="16" height="1" rx="0.5" fill="#2A355A" />
            <rect x="0.000999451" y="10.5" width="16" height="1" rx="0.5" fill="#2A355A" />
        </svg>
    </i>
</template>
<script>
export default {

}
</script>
<style scoped>
.burder-menu {
    cursor: pointer;
    margin-right: 28px;
}

.burder-menu:hover .burder-menu-icon rect {
    fill: #8F20EF;
    transition: .2s linear
}
</style>