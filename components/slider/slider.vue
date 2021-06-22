<template>
    <div class="slider">
        <div class="slider__bar" ref="bar">
            <div class="slider__handle" :style="handleStyle" ref="handle"/>
                <div class="slider__fill" :style="fillStyle"/>
            
        </div>

    </div>
</template>

<script>
import './slider.scss'
import throttle from 'lodash/throttle'
    export default {
        data: () =>({
            isDragging: false,
            handleWidth:0,
            barWidth:0,
        }),

        props:{
            min:{
                type: Number,
                default: 0
            },
            max:{
                type: Number,
                default: 1
            },

            value: Number,
            disabled: Boolean,
        },

        computed:{
            delta(){
                return this.value/this.max;
            },
             fillStyle(){
                return {
                    transformOrigin: "left center",
                    transform: `scaleX(${this.delta})`
                }
             },
             handleStyle(){
                 const [barWidth, delta, handleWidth] = this;
                return {
                   
                    transform: `translateX(${barWidth * delta - handleWidth * 0.5 }px)`
                }
             
            }
        },

        mounted(){
            this.onWindowResize= throttle(this.onWindowResize, 200);
            this.calcDimensions();

            window.addEventListener('resize', this.onWindowResize);
        },

        methods:{
            calcDimensions(){
                const {bar, handle} = this.$refs;
                console.log({bar,handle})

                this.handleWidth = handle.offsetWidth;
                this.barWidth = bar.offsetWidth;

            },

            onWindowResize(){
               this.calcDimensions(); 
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>