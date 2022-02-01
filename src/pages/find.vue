<template>
    <h2>lodash find</h2> 

<div>
    list = {{ list }}
    sitem ={{sitem}}
</div>
<div>
    <input v-model="search.color" placeholder="색깔"/>
</div>
<div>
    <a  @click="doSearch()">찾기</a>
</div>

</template>

<script>
import 'lodash'
export default {
    data () {
        return {
            search: {color:''},
            list:[
                { 'name': 'apple',  'color': 'red', 'active': true },
                { 'name': 'banana', 'color': 'yellow', 'active': false },
                { 'name': 'grafe', 'color': 'green',  'active': true }
            ],
            sitem: {},
        }
    },
    methods: {
        doSearch () {
            this.sitem = _.find(this.list, {'color': this.search.color});

        },
    }
}
</script>