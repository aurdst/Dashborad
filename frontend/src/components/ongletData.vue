<template>
    <b-tabs content-class="mt-3 w-10">
        <b-tab title="Data" active>
            <b-table striped hover :items="dataOne">
            </b-table>
        </b-tab>
        <b-tab title="Other data" active>
            <b-table striped hover :items="dataSecond">
            </b-table>
        </b-tab>
    </b-tabs>
</template>

<script>
    export default {
        name: 'OngletData',
        data() {
            return {
                dataOne: [
                    { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
                    { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
                    { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
                    { age: 38, first_name: 'Jami', last_name: 'Carney' },
                ],
                dataSecond: [
                    { age: 34, first_name: 'Larsen', last_name: 'Wilson' },
                    { age: 22, first_name: 'Jami', last_name: 'Carney' },
                    { age: 77, first_name: 'Macdonald', last_name: 'Shaw' },
                ]
            };
        }
    }
</script>