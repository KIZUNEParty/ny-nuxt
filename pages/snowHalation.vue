<template>
    <div class="hover">
        <div class="black centerize">
            <div class="box">
                <div v-if="$route.query.lang === 'th'">
                    <TH />
                </div>
                <div v-if="$route.query.lang === 'en'">
                    <h1>
                        Dear {{ $route.query.name }}
                    </h1>
                </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<style>
@import url(./style/main.css);
@import url(./style/snowHalation.css);
</style>

<script>
export default {
    created() {
        console.log(this.$route.query.name);
        console.log(this.$route.query.lang);
    },
}
</script>