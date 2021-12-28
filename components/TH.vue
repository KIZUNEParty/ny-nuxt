<template>
    <div class="thai">
        <head>
            <script src="https://twemoji.maxcdn.com/v/latest/twemoji.min.js" crossorigin="anonymous"></script>
        </head>

        <p v-if="$route.query.name === 'โฟกัด'" class="cont">
            <span class="heading">
                ถึงไอหมาของเค้า
            </span>
            <br>
            <span id="fgus-text">
                &nbsp;&nbsp;&nbsp;&nbsp;ขอบคุณที่ยังอยู่ด้วยกันนะคะ ถึงแม้ว่าเค้าจะงี่เง่าไปบ้าง (จริงๆ ก็ไม่บ้าง) แต่ก็ยังทนอยู่ด้วยกัน รักนะคะ อยู่กับเค้าไปนานๆ นะ ไอหมาของเค้า โฮ่งๆ
            </span>
        </p>
        <p v-else-if="$route.query.name === 'กอมมี่'" class="cont">
            <span class="heading">
                ถึงคุณกอมมี่บร๋อแบร์น่ารักที่สุดในโลก
            </span>
            <br>
            <span class="gomburr-text">
                &nbsp;&nbsp;&nbsp;&nbsp;
                <span v-if="$route.query.toSkoy === 'yes'">
                    ฆอบคุ๊ลธิ๊ฆ์เป็นรฮญญิ๊ฒหั๊ล์ยกั๊ซ์ผใครหล๊ยๆ ฃ๊ลน๊ครั๊ผ ถึงเเม๊ว๊พ์จ่มริ๊เฬอื่บ์ลงฌ์เเญ่ๆ นั๊บ์ยชิ๊วิฏฆฮงคุ๊บ์ลกอฒเองก่ฏ๊ฒ ฆอหั๊ล์ยห๊ษ์ายป่วญเร็วๆ เร่รฬฬก่ฆอหั๊ล์ยฏิฎนั๊บ์ยบ์ฒห๊ษ์าลัญธิ๊ฆ์หวังน๊ครั๊ผ
                </span>
                <span v-else>
                    ขอบคุณที่เป็นรอยยิ้มให้กับใครหลายๆ คนนะครับ ถึงแม้ว่าจะมีเรื่องแย่ๆ ในชีวิตของคุณกอมเองก็ตาม ขอให้หายป่วยเร็วๆ แล้วก็ขอให้ติดในมหาลัยที่หวังนะครับ
                </span> 
                <i class="em em-wink"></i>
            </span>
            <img src="https://scontent.fbkk23-1.fna.fbcdn.net/v/t39.30808-6/185524019_164188712437203_2090336010499463669_n.jpg?_nc_cat=100&ccb=1-5&_nc_sid=0debeb&_nc_eui2=AeFefEwO3g1rEjVCEc1R4x1cZCiLM94t2LFkKIsz3i3YsQd9OCDeTbxB7dh7iQZiJCkCfngwT12Zzn2h3My1Y9jE&_nc_ohc=bQc2tNeVvGsAX_jGnNq&_nc_ht=scontent.fbkk23-1.fna&oh=00_AT97wnDtus320WakQ4qQyQXlRmpMcpf2RK-l2useZfg_4A&oe=61CFB5FC" alt="gomburr" class="gomburr">
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
            skoyOut: null
        }
    },
    mounted() {
        const nD = new Date()
        var fY = nD.getFullYear()
        this.fullYear = fY + 1
    }
}
</script>