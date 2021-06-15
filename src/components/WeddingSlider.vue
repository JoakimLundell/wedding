<template>
    <div class="center">
        <a href="#" class="prev" @click.prevent="prev"> &#10094; </a>
        <div class="slider" :style="{width: width, height: height}">
              <!--transition-group name='fade'-->
                  <span v-for="i in [currentIndex]" :key="i">
                <img :src="currentImg" :style="{width: width, height: height}"/>
                  </span>
              <!--/transition-group-->
            
        </div>
        <a href="#" class="next" @click.prevent="next"> &#10095; </a>
    </div>
    
</template>

<script>
export default {
    data() {
        return {
            /*iimages: [
                '/src/assets/slider/1.jpg',
                '/src/assets/slider/2.jpg',
                '/src/assets/slider/3.jpg',
                '/src/assets/slider/4.jpg',
                '/src/assets/slider/5.jpg',
                '/src/assets/slider/6.jpg'
            ],*/
            currentIndex: 0,
        }
    },

    props: {
        width: 0,
        height: 0,
        images: {
            required: true,
            type: Array
        }
    },
    
    methods: {
        next: function() {
            this.currentIndex += 1
        },
        prev: function() {
            this.currentIndex -= 1
        }
    },

    computed: {
        currentImg: function() {
            return this.images[Math.abs(this.currentIndex) % this.images.length];
        },

        getWidthHeight: function() {
            return '{width:' + this.width + '; height:' +  this.height + '}'
        }
    }
}
</script>

<style scoped>
    div.center {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 6px;
    }
    div.slider {
        display: flex;
        justify-content: center;
        overflow: hidden;
    }

    .prev, .next {
        cursor: pointer;
        width: auto;
        padding: 16px;
        font-weight: bold;
        font-size: 18px;
        transition: 0.7s ease;
        border-radius: 0 4px 4px 0;
        text-decoration: none;
        user-select: none;
    }

    /*.prev:hover,
    .next:hover {
        color: var(--link-color-hover)
    }*/

    

    img {
        animation: show 2s;
    }
    
    @keyframes show {
        0% {
            opacity: 0;
        }
    }
</style>