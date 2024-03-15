<template>
    <aside id="aside">
        <nav class="aside-top">
            <img src="../../../public/images/svg/logo.svg" alt="logo">
            <ul class="nav-menu">
                <li v-for="link in asideLinks" :key="link.id" class="nav-menu-item">
                    <a class="nav-menu-link" :href="link.url">
                        <img class="nav-menu-icon" :src="link.src" alt="menu-icon">
                    </a>
                </li>
            </ul>
        </nav>
        <div class="aside-bottom">
            <button class="aside-btn">
                <svg class="aside-btn-icon" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect width="20" height="20" rx="6" fill="#F5F7FB" />
                    <path d="M10 6V14" stroke="#8591AE" stroke-linecap="round" stroke-linejoin="round" />
                    <path d="M14 10H6" stroke="#8591AE" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
            </button>
        </div>
    </aside>
</template>
<script>
import { asideLinks } from '@/assets/asideLinks';

export default {
    data: () => ({
        asideLinks
    }),
}
</script>
<style scoped>
#aside {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100vh;
    width: 72px;
    background: #fff;
    border-top-left-radius: 16px;
    border-bottom-left-radius: 16px;
    padding-top: 28px;
}

.aside-top {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.nav-menu {
    margin-top: 28px;
    width: 100%;
}

.nav-menu-item {
    position: relative;
    text-align: center;
    cursor: pointer;
}

.nav-menu-item::after {
    position: absolute;
    display: block;
    content: '';
    top: 0;
    left: 0;
    width: 4px;
    height: 20px;
    background: url('../../../public/images/svg/side-active.svg');
    transition: .2s linear;
}

.nav-menu-item:not(:last-child)::after {
    opacity: 0;
}

.nav-menu-item:hover::after {
    opacity: 1;
    transition: .2s linear;
}

.nav-menu-item:not(:last-child) {
    margin-bottom: 32px;
}

.aside-bottom {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 28px 0px;
    border-top: 1px solid #E5E8EF;
}

.aside-btn {
    border: none;
    background: none;
    cursor: pointer;
    padding: 0;
}

.aside-btn:hover .aside-btn-icon path{
    stroke: #8F20EF;
    transition: .2s linear;
}

@media(max-width: 600px) {
    #aside {
        display: none;
    }
}
</style>