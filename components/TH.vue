<template>
    <div class="thai">
        <head>
            <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
            <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
            <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
        </head>

        <h1>
            ถึงคุณ {{ $route.query.name }}
        </h1>
        <p v-if="$route.query.name === 'โฟกัด'" class="cont">
            ถึงไอหมาของเค้า
        </p>
        <p v-else class="cont">
            คนที่ได้อ่านข้อความนี้ ถึงแม้ว่าจะช้าไปหน่อยที่ผมจะมา Merry Christmas ทุกคน แต่ก็สุขสันต์วันปีใหม่นะครับ ขอให้มีความสุขในปี {{ fullYear }} ที่กำลังจะมาถึงนี้นะครับ ขอให้เวลาทำอะไรๆ ก็ดีไปหมดทุกอย่างเลยยย แล้วก็ขอให้รอดจากไอประเทศเส็งเคร็งนี่นะครับ สวัสดีครับ 😁😁
        </p>
        <br><br><br>
        <div class="myEP">
            <span>อ๋อ แล้วก็ขอฝากเพลงไว้ในอ้อมอกอ้อมใจด้วยนะครับ 🥺</span>
            <br>
            <br>
            <Cards />
        </div>
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