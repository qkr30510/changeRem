<template>
    <div>
        <div class="uk-flex" style="margin-bottom:15px">
            <input v-model="bodyNumber" type="number" placeholder="최상단 입력값을 넣어주세요."  class="uk-input">
            <button @click="change" class="uk-button uk-button-primary uk-width-1-3">변환하기</button>
        </div>
        <div >
            <ul class="uk-list uk-list-striped">
                <li v-for="(number, i) in numberList" v-bind:key='i' >
                    <span>{{i+8}}px</span>
                    <span> = </span>
                    <span>{{number | dot}}rem</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'inputComponent',
    data() {
        return {
            bodyNumber:'',
            pxNumber:'',
            remNumberWrap:false,
            numberList:[],

        };
    },
    methods: {
        change(){
            this.numberList = []
            this.remNumberWrap = true;
            let newNumbers = 0
           
            for(let i = 8; i < 30; i++){
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
        
    },
};
</script>





