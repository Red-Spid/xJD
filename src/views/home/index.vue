<template>
    <div>
        <bod/>
        <div class="">
        111111
        </div>
        <div class="recommend_box" ref='wrapper'>
            <ul class="my_list">
                <li v-for="(item,key) in arr" :key="key">
                    第{{key}}条数据
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
import bod from '@/components/body/jd_home.vue'
// import tit from '@/components/tit/return.vue'
import Bscroll from 'better-scroll'
export default{
    components:{bod},
    data(){
        return{
            arr:["1","2","3","4","5","6","7","8","9","10","1","2","3","4","5","6","7","8","9","10"]
        }
    },
    mounted(){
        this.$nextTick(() => {
             this.scroll = new Bscroll(this.$refs.wrapper);
        });
    },
    created(){
        this.forE()
    },
    methods:{
        forE(){
            // this.arr.forEach((i,n)=>{
                // console.log(i,n)
            // })
            // console.log(this.arr);
        }
    }
}
</script>
<style lang="less">
.recommend_box{
    overflow: hidden;
    height:10rem;
    position: absolute;
    top:7rem;
    left:0;
    right:0;
    bottom: 0;
}
.my_list{
    padding: 5rem;
}
</style>