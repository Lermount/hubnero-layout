<template>
    <div class="pagination">
        <i class="prew">
            <svg class="prew-icon" width="20" height="20" viewBox="0 0 20 20" fill="none"
                xmlns="http://www.w3.org/2000/svg">
                <rect width="20" height="20" rx="6" fill="#F5F7FB" />
                <path d="M11.6667 6.66663L8.33333 9.99996L11.6667 13.3333" stroke="#8591AE" stroke-linecap="round"
                    stroke-linejoin="round" />
            </svg>
        </i>
        <ul class="pages">
            <li class="page">1</li>
            <li class="page curent-page">2</li>
            <li class="page">3</li>
            <li class="page separator">...</li>
            <li class="page">12</li>
        </ul>
        <i class="next">
            <svg class="next-icon" width="20" height="20" viewBox="0 0 20 20" fill="none"
                xmlns="http://www.w3.org/2000/svg">
                <rect width="20" height="20" rx="6" fill="#F5F7FB" />
                <path d="M8.33334 13.3334L11.6667 10L8.33334 6.66671" stroke="#8591AE" stroke-linecap="round"
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
.pagination {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    margin-top: 28px;
    padding: 16px;
    border-radius: 12px;
    background: #FFFFFF;
}

.prew,
.next {
    cursor: pointer;
}

.prew:hover .prew-icon path,
.next:hover .next-icon path {
    stroke: #8F20EF;
    transition: .2s linear;
}

.pages {
    display: flex;
    align-items: center;
    margin: 0px 8px;
}

.page {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 36px;
    height: 36px;
    font-family: Commissioner-Regular;
    font-size: 14px;
    font-weight: 400;
    line-height: 20px;
    letter-spacing: 0em;
    text-align: left;
    color: #8591AE;
    cursor: pointer;
}

.page:hover:not(:nth-child(4n)) {
    color: #8F20EF;
    transition: .2s linear;
}

.curent-page {
    border-radius: 12px;
    background: #F5F7FB;
    color: #2A355A;
}

.separator {
    cursor: unset;
}


@media(max-width: 600px) {
   .pagination {
    justify-content: center;
   }
}
</style>