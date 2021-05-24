<template>
    <view>
        <swiper indicator-dots autoplay :interval="3000" :duration="1000" circular>
            <block v-for="(item,index) in resdata" :key="index">
                <swiper-item>
                    <view class="swiper-item" @tap="event(item)">
                        <img :src="item.src"
                        lazy-load
                        style="height: 350upx"
                        >
                    </view>
                </swiper-item>
            </block>
        </swiper>
    </view>
</template>

<script>
    export default {
        name: '',
        props: {
            resdata: Array
        },
        data() {
            return {
                
            }
        },
        methods: {
            event(item) {
                console.log('click', item)
            }
        }
    }
</script>

<style lang="less" scoped>
    
</style>