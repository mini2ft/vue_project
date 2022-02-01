<template>
    <h2>lodash filter</h2> 

    <div>
        <table style="border: 1px solid">
            <thead>
                <tr>
                    <th>이름</th>
                    <th>나이</th>
                    <th>작업</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in list" :key="item.name">
                    <th>{{ item.name }}</th>
                    <th>{{ item.age }}</th>
                    <th><button @click="deleteItem(item.name)">삭제</button></th>
                </tr>
            </tbody>
        </table>
    </div>

</template>

<script>
import 'lodash'
export default {
    data () {
        return {
            search: {color:''},
            list:[
                { name: '호랑이', age: 9},
                { name: '원숭이', age: 3},
                { name: '돌고래', age: 5}
            ],
            sitem: {},
        }
    },
    methods: {
        deleteItem (nm) {
            console.log(nm)
            // this.list = _.filter(this.list, 'name', nm)
            // this.list = _.filter(this.list, 'name', '호랑이')
            this.list = this.list.filter(item => {
                console.log("item.name = ", item.name)
                console.log("결과:", item.name != nm)
                return item.name != nm
            })

        },
    }
}
</script>