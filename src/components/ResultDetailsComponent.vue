<template>
    <div class="details_main">
        <div class="details_container" :class="{ optimum: optimum }">
            <div class="details_info">
                <div>
                    {{"Something"}}
                        <v-icon v-if="optimum" color="white">mdi-ray-start-arrow</v-icon>
                        <v-icon v-if="!optimum" color="black">mdi-ray-start-arrow</v-icon>
                    {{"Something"}}
                </div>
                <div v-if="optimum">with Oceanic</div>
            </div>

            <div class="details_route">
                <div class="base_controls_label">
                    Shipping route:
                </div>
                <div class="details_route_row" v-for="route in routes" :key="route">
                    {{route.from}}
                    <div v-if="optimum == true">
                        <v-icon color="white" v-if="route.by == 0">mdi-airplane</v-icon>
                        <v-icon color="white" v-if="route.by == 1">mdi-truck</v-icon>
                        <v-icon color="white" v-if="route.by == 2">mdi-ferry</v-icon>
                    </div>
                    <div v-if="optimum == false">
                        <v-icon color="black" v-if="route.by == 0">mdi-airplane</v-icon>
                        <v-icon color="black" v-if="route.by == 1">mdi-truck</v-icon>
                        <v-icon color="black" v-if="route.by == 2">mdi-ferry</v-icon>
                    </div>
                        
                    {{route.to}}
                </div>
            </div>

            <div class="details_info">
                <div>
                    <div class="details_label">
                        Price: 
                    </div>
                    <div class="details_number">
                        {{"$222"}}
                    </div>
                </div>
                <div>
                    <div class="details_label">
                        Time:
                    </div>
                    <div class="details_number">
                        {{"12H"}}
                    </div>
                </div>
                <div class="details_controls">
                    <div class="base_controls_label">
                        Type fee:
                    </div>
                    <select class="base_controls_dropdown">
                        <option v-for="fee in fees" :key="fee">{{fee}}</option>
                    </select>
                    <button
                        type="button"
                        class="base_controls_button"
                    >
                        Book
                    </button>
                </div>
            </div>
            <div class="details_optimum_label">OPTIMUM</div>
        </div>
    </div>
</template>

<script>
    import { mdiAccount } from "@mdi/js";

    export default {
        name: 'ResultDetailsComponent',
        props: ['optimum'],
        data: () => ({
            icons: {
                mdiAccount
            },
            fees: ['Weapons: 100%', 'Funny stuff: 10%'],
            routes: [
                        {from: 'Tunis', to: 'Kabalo', by: 0}, 
                        {from: 'Kabalo', to: 'Kabalo', by: 1},
                        {from: 'Tunis', to: 'Tunis', by: 2}
                    ]       
        })
    }
</script>

<style scoped>

    .v-icon{
    margin: 0 10px;
    }



    .details_main{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        padding: 25px;
    }

    .details_container{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        background-color:white;
        border: 3px solid black;
        color: black;
        position: relative;
        font-size: 20px;
        padding: 20px;
    }

    .details_info{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 100%;
        padding: 0 10%;
        font-size: 1em;
        font-weight: bold;
    }

    .details_info > div{
        display: flex;
        align-items: center;
    }

    .details_number {
        font-size: 1.7rem;
        margin-left: 10px;
    }

    .details_optimum_label{
        background-color: #073763;
        position: absolute;
        right: 0;
        top: 0;
        height: 100%;
        writing-mode: vertical-rl;
        text-orientation: mixed;
        text-align: left;
        font-size: 26px;
        padding-top: 10px;
        display: none;
    }

    .optimum{
        background-color: #385F82;
        color: white;
    }

    .optimum .details_optimum_label{
        display: block;
    }

    .details_controls{
        display: flex;
        flex-direction: column;
        width: 40%;
        align-items: center;
    }

    .details_route{
        display: flex;
        flex-direction: column;
        width: 60%;
    }

    .details_route_row{
        display: flex;
        justify-content: center;
    }

</style>
 
  