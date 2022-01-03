<template>
    <h2>Array 관련 함수</h2> 

    list = {{ list }}
    list_clone ={{list_clone}}
<div>
    <input v-model="item.name" placeholder="이름"/>
    <input v-model="item.age" placeholder="나이"/>
    <a  @click="doAddItem()">추가</a>
</div>

</template>

<script>
import 'lodash'
export default {
    data () {
        return {
            list: [],
            list_clone: [],
            item: {
                name: '',
                age: 0
            },
        }
    },
    methods: {
        doAddItem () {
            console.log(this.item)
            this.list.push(this.item);
            this.list_clone.push(_.cloneDeep(this.item))

        },
    }
}
</script>