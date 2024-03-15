<template>
    <ul class="info">
        <li class="info-left">
            <img class="info-img" src="../../../public/images/svg/info-img.svg" alt="icon">
            <h3 class="info-title">Team</h3>
            <i class="info-icon">
                <svg class="info-icon-svg" width="14" height="15" viewBox="0 0 14 15" fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <rect y="0.5" width="14" height="14" rx="7" fill="#F5F7FB" />
                    <path d="M7.00053 7.00003V11" stroke="#8591AE" stroke-linecap="round" stroke-linejoin="round" />
                    <circle cx="7.00101" cy="4.25003" r="0.75" fill="#8591AE" />
                </svg>
            </i>
        </li>
        <li class="info-right">
            <ul class="info-right-list">
                <li v-for="item in infoItems" :key="item.id" class="info-right-item" :class="item.name">
                    <span class="number">{{ item.number }}</span>
                    <p class="description">{{ item.description }}</p>
                </li>
            </ul>
        </li>
    </ul>
</template>
<script>
import { infoItems } from '@/assets/infoItems';

export default {
    data: () => ({
        infoItems
    }),
}
</script>
<style scoped>
.info {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1403px;
    padding: 16px 28px;
    border-radius: 12px;
    background: #fff;
}

.info-left {
    display: flex;
    align-items: center;
}

.info-img {
    height: 32px;
    width: 32px;
    margin-right: 16px;
    border-radius: 8px;
}

.info-title {
    font-family: Commissioner-Medium;
    font-size: 14px;
    font-weight: 500;
    line-height: 20px;
    letter-spacing: 0px;
    text-align: left;
    color: #2A355A;
}

.info-icon {
    margin-left: 4px;
    cursor: pointer;
}

.info-icon:hover .info-icon-svg path {
    stroke: #8F20EF;
    transition: .2s linear
}

.info-right {
    overflow-x: scroll;
}

.info-right::-webkit-scrollbar {
    height: 2px;
}

.info-right::-webkit-scrollbar-track {
    background: transparent;
}

.info-right::-webkit-scrollbar-thumb {
    background-color: #8F20EF;
    border-radius: 20px;
    border: 4px solid transparent;
}

.info-right-list {
    display: flex;
    align-items: center;
    width: 100%;
}

.info-right-item {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 0px 36px;
    border-left: 1px solid #E5E8EF;
}

.info-right-item.members,
.info-right-item.women {
    padding-left: 0;
    border-left: none;
}

.info-right-item.online {
    position: relative;
}

.info-right-item.online::after {
    position: absolute;
    display: block;
    content: '';
    top: 5px;
    right: 30px;
    height: 6px;
    width: 6px;
    border-radius: 50%;
    background: #24C182;
}

.number {
    font-family: Commissioner-Medium;
    font-size: 22px;
    font-weight: 500;
    line-height: 29px;
    letter-spacing: 0em;
    text-align: left;
    color: #2A355A;
}

.description {
    width: max-content;
    font-family: Commissioner-Regular;
    font-size: 12px;
    font-weight: 400;
    line-height: 18px;
    letter-spacing: 0px;
    text-align: left;
    color: #8591AE;
}

@media(max-width: 1440px) {
    .info-left {
        margin-right: 30px;
    }
}
</style>