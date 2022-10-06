<template>
    <div class="result_main">
        <div class="result_component_optimum" @click="$emit('resultClicked', 0)">
            <div class="result_info">
                <div>
                    {{"Something"}}
                        <v-icon color="white">mdi-ray-start-arrow</v-icon>
                    {{"Something"}}
                </div>
                <div>with Oceanic</div>
            </div>
            <div class="result_info">
                <div>
                    <div class="result_label">
                        Price: 
                    </div>
                    <div class="result_number">
                        {{"$200"}}
                    </div>
                </div>
                <div>
                    <div class="result_label">
                        Time:
                    </div>
                    <div class="result_number">
                        {{"12H"}}
                    </div>
                </div>
            </div>
            <div class="result_optimum_label">OPTIMUM</div>
        </div>

        <div class="result_component" @click="$emit('resultClicked', 1)">
            <div class="result_info">
                <div>
                    {{"Something"}}
                        <v-icon color="black">mdi-ray-start-arrow</v-icon>
                    {{"Something"}}
                </div>
            </div>
            <div class="result_info">
                <div>
                    <div class="result_label">
                        Price: 
                    </div>
                    <div class="result_number">
                        {{"$200"}}
                    </div>
                </div>
                <div>
                    <div class="result_label">
                        Time:
                    </div>
                    <div class="result_number">
                        {{"12H"}}
                    </div>
                </div>
            </div>
        </div>

        <div class="result_component" @click="$emit('resultClicked', 2)">
            <div class="result_info">
                <div>
                    {{"Something"}}
                        <v-icon color="black">mdi-ray-start-arrow</v-icon>
                    {{"Something"}}
                </div>
            </div>
            <div class="result_info">
                <div>
                    <div class="result_label">
                        Price: 
                    </div>
                    <div class="result_number">
                        {{"$200"}}
                    </div>
                </div>
                <div>
                    <div class="result_label">
                        Time:
                    </div>
                    <div class="result_number">
                        {{"12H"}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import { mdiAccount } from "@mdi/js";

    export default {
        name: 'ResultComponent',
        data: () => ({
            icons: {
                mdiAccount
            },       
        }),
    }
</script>

<style scoped>

    .v-icon{
    margin: 0 10px;
    }

    .result_main{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        padding: 20px;
    }

    .result_component_optimum{
        height: 40%;
        width: 100%;
        background-color: #385F82;
        border: 3px solid black;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 25px;
        color: white;
        font-size: 24px;
        position: relative;
        cursor: pointer;
    }

    .result_component{
        height: 25%;
        width: 100%;
        background-color: white;
        border: 3px solid black;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 15px;
        color: black;
        font-size: 18px;
        cursor: pointer;
    }

    .result_info{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 100%;
        padding: 0 10%;
        font-size: 1em;
        font-weight: bold;
    }

    .result_info > div{
        display: flex;
    }

    .result_number {
        font-size: 1.7rem;
        margin-left: 10px;
    }

    .result_optimum_label{
        background-color: #073763;
        position: absolute;
        right: 0;
        top: 0;
        height: 100%;
        writing-mode: vertical-rl;
        text-orientation: mixed;
    }

</style>
 
  