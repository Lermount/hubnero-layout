<template>
    <button class="addButton">
        <svg class="addButton-icon" width="20" height="20" viewBox="0 0 20 20" fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <rect width="20" height="20" rx="6" fill="white" fill-opacity="0.2" />
            <path d="M10 6V14" stroke="white" stroke-linecap="round" stroke-linejoin="round" />
            <path d="M14 10H6" stroke="white" stroke-linecap="round" stroke-linejoin="round" />
        </svg>
        <p class="addButton-text">Add new Employee</p>
    </button>
</template>
<script>
export default {

}
</script>
<style scoped>
.addButton {
    display: flex;
    align-items: center;
    justify-content: center;
    width: max-content;
    margin-top: 28px;
    min-width: 184px;
    min-height: 48px;
    padding: 0;
    border: none;
    border-radius: 12px;
    background: #8F20EF;
    cursor: pointer;
}

.addButton-icon {
    margin-right: 12px;
}

.addButton-text {
    font-family: Commissioner-Regular;
    font-size: 14px;
    font-weight: 400;
    line-height: 20px;
    letter-spacing: 0em;
    text-align: left;
    color: #FFFFFF;
}

.addButton:hover .addButton-icon path {
    stroke: #2A355A;
    transition: .2s linear;
}

.addButton:hover .addButton-text {
    color: #2A355A;
    transition: .2s linear;
}
</style>