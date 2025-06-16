<template>
    <div class="detail-container"
    >
        <!-- {{ objectDetail[id].title }}
        {{ objectDetail[id].description }} -->

        {{ getTitle() }} 
    </div>
</template>

<script>

export default {
    data() {
        return {
            id: this.$route.params.id,
            objectDetail: [
                {
                    id: 1,
                    title: "Antalya 17.01.2024",
                    description: "Antalya, Türkiye'nin en popüler turistik bölgesi ve birçok ziyaretçiye hoş geldiniz."
                },
                {
                    id: 2,
                    title: "Bursa 06.08.2024",
                    description: "Bursa, Türkiye'nin en popüler turistik bölgesi ve birçok ziyaretçiye hoş geldiniz."
                },
                {
                    id: 3,
                    title: "Amsterdam 14.10.2024",
                    description: "Amsterdam, Hollanda'nın başkenti ve birçok ziyaretçiye hoş geldiniz."
                },
                {
                    id: 4,
                    title: "Konya 02.01.2025",
                    description: "Konya, Türkiye'nin en popüler turistik bölgesi ve birçok ziyaretçiye hoş geldiniz."
                }
            ]
        }
    },
    created() {
        console.log('detail', this.objectDetail[this.id]);
    },
    methods: {
        getTitle() {
            return this.objectDetail.find(item => item.id === this.id).title;
        }
    }
}
</script>

<style>
.detail-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
</style>