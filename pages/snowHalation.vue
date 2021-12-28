<template>
    <div class="hover">
        <head>
            <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
            <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
            <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
        </head>
        <div class="black centerize">
            <div class="box">
                <div v-if="$route.query.lang === 'th'">
                    <TH />
                    <br><br><br>
                    <div class="myEP">
                        <span>อ๋อ แล้วก็ขอฝากเพลงไว้ในอ้อมอกอ้อมใจด้วยนะครับ <i class="em em-pleading_face"></i></span>
                        <br>
                        <br>
                        <Cards />
                    </div>
                </div>
                <div v-else-if="$route.query.lang === 'en'">
                    <h1>
                        Dear {{ $route.query.name }}
                    </h1>
                    <br><br><br>
                    <div class="myEP">
                        <span>อ๋อ แล้วก็ขอฝากเพลงไว้ในอ้อมอกอ้อมใจด้วยนะครับ <i class="em em-pleading_face"></i></span>
                        <br>
                        <br>
                        <Cards />
                    </div>
                </div>
                <div v-else>
                    <h1 style="text-align: center !important;">
                        Just a Landing!
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