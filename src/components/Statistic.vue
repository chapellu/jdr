<template>
<div class="statistics">
    <div class="statistic stat" :title="details(stats.values)">
        <p class="title">{{stats.title}}</p>
        <p class="value">{{addition(stats.values)}}</p>
    </div>
    <div class="substats">
        <div class="substat stat" v-for="substat in substats" :key=substat :title="details(substat.values)">
            <p class="title">{{substat.title}}</p>
            <p class="value">{{addition(substat.values)}}</p>
        </div>
    </div>
</div>
</template>


<script>
export default {
    name: 'Statistics',
    props: {
        "stats": {
            type: Object,
            default: () => {}
        },
        "substats": {
            type: Array,
            default: () => []
        }
    },
    methods: {
        addition: (values) => {
            let total = 0;
            for (const value in values) {
                if (values.hasOwnProperty(value)) {
                    total += values[value]
                }
            }
            return total;
        },
        details: (values) => {
            let message = "";
            for (const value in values) {
                if (values.hasOwnProperty(value)) {
                    message += value + ": " + values[value] + " ";
                }
            }
            return message
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p {
    font-size: 300%;
    margin: 0;
    text-align: center;
}

.substats {
    display: flex;
    flex-direction: row;
}

.substat {
    width: 50%;
}

.stat {
    border-style: solid;
    border-width: medium;
}

.title {
    border-bottom-style: solid;
    border-bottom-width: medium;
}
</style>
