<template>
    <div class="eng">
        <div class="cont">
                <span class="heading">
                Dear {{ $route.query.name }}
            </span>
            <br>
            <span id="wText">
                &nbsp;&nbsp;&nbsp;&nbsp;To the person who is reading this message. I think that it’s too late to say “Merry Christmas” to you but “Happy New Year {{ fullYear }}!!” I’m hoping that this year is the great year for you, hoping that you can do everything that you ever want and hoping that you will survive from this fucking country. So.. Happy New Year!! <i class="em em-wink"></i> <i class="em em-smiley"></i>
            </span>
        </div>
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