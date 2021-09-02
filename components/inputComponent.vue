<template>
    <div>
         <!-- v-if="!this.remNumberWrap" -->
        <div>
            <input v-model="bodyNumber" type="number" placeholder="최상단 입력값을 넣어주세요.">
            <button @click="change" class="uk-button uk-button-primary">변환하기</button>
        </div>
        <div >
            <ul>
                <li v-for="(number, i) in numberList" v-bind:key='i' >
                    <span>{{i}}</span>
                    <span>{{number}}</span>
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
            this.remNumberWrap = true;
            let newNumbers = 0
            
            
            for(let i = 8; i < 30; i++){
                newNumbers = i/this.bodyNumber
                this.numberList.push(newNumbers)
                console.log(this.numberValue)
            }
            
        }
    },
    computed: {

    },
    mounted() {
        
    },
    // 변환하기 누르면 입력된 숫자가 1rem 기준으로 바꿈.
    // 사용하려는 값 / 최상단 부모값 = rem 값
};
</script>





