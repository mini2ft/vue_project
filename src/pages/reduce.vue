<template>
    <h2>lodash reduce</h2> 

<div>
    list = {{ list }}
    sum ={{sum}}
</div>
<div>
    <a  @click="getSum()">합계 구하기</a>
</div>

</template>

<script>
import 'lodash'
export default {
    data () {
        return {
            list: [1,2,3,4,5],
            sum: 0,
        }
    },
    methods: {
        getSum () {
            this.sum = _.reduce(this.list, function(tot, n) {
                console.log("tot = ", tot, ", n = ", n)
                return tot + n;
            })

        },
    }
}
</script>