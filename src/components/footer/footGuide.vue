<template>
    <section id='foot_guide'>
        <section @click = "gotoAddress()" class="guide_item">
            <span>外卖</span>
        </section>
        <section @click = "gotoAddress()" class="guide_item">
            <span>搜索</span>
        </section>
        <section @click = "gotoAddress()" class="guide_item">
            <span>订单</span>
        </section>
        <section @click = "gotoAddress()" class="guide_item">
            <span>我的</span>
        </section>
    </section>
</template>

<script>
    export default {
    	data(){
            return{
                
            }
        },
        created(){
           
        },
        mounted(){
            
        },
        computed: {
        },
        methods: {
        	gotoAddress(){

            },
        },

    }

</script>

<style lang="scss" scoped>

    #foot_guide{
        background-color: #fff;
        position: fixed;
        z-index: 100;
        left: 0;
        right: 0;
        bottom: 0;
        @include wh(100%, 1.95rem);
        display: flex;
        box-shadow: 0 -0.026667rem 0.053333rem rgba(0,0,0,.1);
    }
    .guide_item{
    	flex: 1;
    	display: flex;
    	text-align: center;
    	flex-direction: column;
    	align-items: center;
		.icon_style{
			@include wh(.8rem, .8rem);
			margin-top: .3rem;
			fill: #ccc;
		}
		span{
			@include sc(.45rem, #666);
		}
    }
   
</style>
