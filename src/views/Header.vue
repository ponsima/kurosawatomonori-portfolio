<template>
    <header class="Info">
        <figure>
            <img v-bind:src="myPicture" class="img_down" alt="myPicture">
            <img v-bind:src="myPicture" class="img_up" alt="myPicture">
        </figure>
        <img v-bind:src="myPicture" class="faceImg" alt="myPicture">
        <h1 class="name">TOMONORI KUROSAWA</h1>
        <p class="job">Web Developer</p>
    </header>

</template>

<script lang="ts">
    export default {
        name: "Header",
        data() {
            return {
                myPicture: "https://firebasestorage.googleapis.com/v0/b/portfolio-161c4.appspot.com/o/flamelink%2Fmedia%2Fmy_img2.JPG?alt=media&token=f12a1cd4-3cfa-4380-bb03-b2eee11cba9d",
            };
        },
    };
</script>

<style scoped lang="scss">
    .Info {

        /*position: relative;*/
        $blurPx: 15px;

        figure {
            height: 150px;
            width: 100%;
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            filter: blur($blurPx); /*ぼかし度*/

            .img_down {
                width: 100%;
                height: 100%;
                object-fit: cover;
                opacity: 0.9;

            }

            .img_up {
                position: absolute;
                top: 0;
                left: 0;
                margin: 0 20%;
                width: 60%;
                height: 100%;
                object-fit: cover;
                filter: blur($blurPx); /*ぼかし度*/
            }

        }

        .faceImg {
            position: relative;
            display: block;
            margin: 75px auto 0;
            width: 180px;
            border: 15px solid #fff;
            border-radius: 120px;
        }
    }

    .name {
        font-size: 24px;
        text-align: center;
        margin-bottom: 10px;
        font-weight: 700;
    }

    .job {
        text-align: center;
        margin-bottom: 15px;

        color: #999;
        font-size: 18px;
    }
</style>
