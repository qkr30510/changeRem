<template>
    <div class="center">
        <div class="uk-flex" style="margin-bottom:15px">
            <input v-model="bodyNumber" v-on:keyup.enter="change" type="number" placeholder="px"  class="uk-input">
            <button @click="change" class="uk-button uk-button-primary uk-width-1-3">변환하기</button>
        </div>
        <div>
            <ul class="uk-list uk-list-striped">
                <li v-for="(number, i) in numberList" v-bind:key='i' class="numberList" >
                    <div>
                        <span>{{i+8}}px</span>
                        <span> = </span>
                    </div>
                    <div>
                        <span>{{number | dot}}rem</span>
                    </div>
                </li>
            </ul>
        </div>
        <button v-if="moreBtn" @click="more" class="uk-button uk-button-secondary uk-width-1-3" style="display:block; margin:auto;">more</button>
    </div>
</template>

<script>
export default {
    name: 'inputComponent',
    data() {
        return {
            bodyNumber:14,
            pxNumber:'',
            numberList:[],
            moreBtn:false,
        };
    },
    methods: {
        change(){
            this.moreBtn = true;
            this.numberList = []
            let newNumbers = 0
           
            for(let i = 8; i < 30; i++){
                newNumbers = i/this.bodyNumber
                this.numberList.push(newNumbers)
                console.log('e',this.numberValue)
            }
        },
        more(){
            this.moreBtn = false
            let newNumbers = 0
           
            for(let i = 30; i < 71; i++){
                newNumbers = i/this.bodyNumber
                this.numberList.push(newNumbers)
                console.log('e',this.numberValue)
            }            
        }
    },
    filters: { 
        dot(value){
            return value.toFixed(2)
        }
    },
    computed: {

    },
    mounted() {
        this.change()
    },
};
</script>

<style>
.center{
    max-width:1100px;
    width:100%;
    margin:auto;
}
.numberList{
    display: flex;
    justify-content: flex-start;
}

.numberList div:last-child{
    margin-left: 5px;
}
</style>




