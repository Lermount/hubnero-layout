<template>
    <div class="header-user">
        <img class="header-user-avatar" src="../../../public/images/svg/headerUser.svg" alt="avatar">
        <p class="header-user-name">Ernest Eberly</p>
        <i class="header-user-dropdown">
            <svg class="dropdown-icon" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="20" height="20" rx="6" fill="#F5F7FB" />
                <path d="M6.66663 8.33333L9.99996 11.6667L13.3333 8.33333" stroke="#8591AE" stroke-linecap="round"
                    stroke-linejoin="round" />
            </svg>

        </i>
    </div>
</template>
<script>
export default {

}
</script>
<style scoped>
.header-user {
    display: flex;
    align-items: center;
    padding-left: 28px;
    border-left: 1px solid #E5E8EF;
}

.header-user-avatar {
    height: 32px;
    width: 32px;
    border-radius: 8px;
}

.header-user-name {
    margin-left: 12px;
    font-family: Commissioner-Medium;
    font-size: 14px;
    font-weight: 500;
    line-height: 20px;
    letter-spacing: 0px;
    text-align: left;
    color: #2A355A;
}

.header-user-dropdown {
    margin-left: 12px;
    cursor: pointer;
}

.header-user-dropdown:hover .dropdown-icon path {
    stroke: #8F20EF;
    transition: .2s linear
}

@media(max-width: 600px) {
    .header-user {
        display: none;
    }
}
</style>