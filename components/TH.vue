<template>
    <div class="thai">
        <head>
            <script src="https://twemoji.maxcdn.com/v/latest/twemoji.min.js" crossorigin="anonymous"></script>
        </head>

        <p v-if="$route.query.name === 'โฟกัด'" class="cont">
            <span class="heading">
                ถึงไอหมาของเค้า
            </span>
            <span id="gomburr-text">
                &nbsp;&nbsp;&nbsp;&nbsp;
            </span>
        </p>
        <p v-else-if="$route.query.name === 'กอมมี่'" class="cont">

        </p>
        <p v-else class="cont">
            <span class="heading">
                ถึงคุณ {{ $route.query.name }}
            </span>
            <br>
            <span id="wText">
                &nbsp;&nbsp;&nbsp;&nbsp;คนที่ได้อ่านข้อความนี้ ถึงแม้ว่าจะช้าไปหน่อยที่ผมจะมา Merry Christmas ทุกคน แต่ก็สุขสันต์วันปีใหม่นะครับ ขอให้มีความสุขในปี {{ fullYear }} ที่กำลังจะมาถึงนี้นะครับ ขอให้เวลาทำอะไรๆ ก็ดีไปหมดทุกอย่างเลยยย แล้วก็ขอให้รอดจากไอประเทศเส็งเคร็งนี่นะครับ สวัสดีครับ <i class="em em-wink"></i> <i class="em em-smiley"></i>
            </span>
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            fullYear: 2022,
        }
    },
    mounted() {
        const nD = new Date()
        var fY = nD.getFullYear()
        this.fullYear = fY + 1
    }
}
</script>