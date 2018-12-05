<template>
    <section>
    </br>
        <v-container>
        
        <button class="button field is-danger" @click="checkedRows = []"
            :disabled="!checkedRows.length">
            <b-icon icon="close"></b-icon>
            <span>Clear checked</span>
        </button>


        

        <b-tabs>
            <b-tab-item label="Youtube links download">
                <b-table
                    :data="data"
                    :columns="columns"
                    :checked-rows.sync="checkedRows"
                    :is-row-checkable="(row) => row.id !== 3"
                    checkable>

                    <template slot="bottom-left">
                        <b>Total checked</b>: {{ checkedRows.length }}
                    </template>
                </b-table>
            </b-tab-item>

            <b-tab-item label="Checked rows">
                <pre>{{ checkedRows }}</pre>
            </b-tab-item>
        </b-tabs>
        <downloadVideo/>
    </v-container>
    </section>
</template>

<script>
    import downloadVideo from "@/components/downloadVideo";

    export default {
        components:{
            downloadVideo
        },
        data() {
            const data = [
                { 'id': "cdwMOoAMAbg", 'name': 'Pan-Pot @ Zurich Street Parade 2018 (BE-AT.TV)', 'channel': 'BE.AT.TV', 'date': '2016-12-06 14:38:38', 'minutes': "4:30m" },
                { 'id': "JKHDSFBASDF", 'name': 'Pan-Pot @ Zurich Street Parade 2018 (BE-AT.TV)', 'channel': 'BE.AT.TV', 'date': '2016-12-06 14:38:38', 'minutes': "4:30m" },
                { 'id': "klajdsflaie", 'name': 'Pan-Pot @ Zurich Street Parade 2018 (BE-AT.TV)', 'channel': 'BE.AT.TV', 'date': '2016-12-06 14:38:38', 'minutes': "4:30m" },
                { 'id': "qekjalksjds", 'name': 'Pan-Pot @ Zurich Street Parade 2018 (BE-AT.TV)', 'channel': 'BE.AT.TV', 'date': '2016-12-06 14:38:38', 'minutes': "4:30m" },
            ]

            return {
                data,
                checkedRows: [data[1], data[3]],
                columns: [
                    {
                        field: 'id',
                        label: 'ID',
                        width: '40',
                        numeric: true
                    },
                    {
                        field: 'name',
                        label: 'Name',
                    },
                    {
                        field: 'channel',
                        label: 'Channel',
                    },
                    {
                        field: 'date',
                        label: 'Date',
                        centered: true
                    },
                    {
                        field: 'minutes',
                        label: 'Minutes',
                    }
                ]
            }
        }
    }
</script>