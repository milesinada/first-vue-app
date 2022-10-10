<template>
    <li>
        <h2>{{ name }}</h2>
        <button @click="toggleDetails">{{ detailsAreVisible ? 'Hide' : 'Show' }} Details</button>        
        <ul v-if="detailsAreVisible">
            <li><strong>Phone:</strong>{{phoneNumber}}</li>
            <li><strong>EMail:</strong>{{ emailAddress }}</li>
        </ul>
    </li>
</template>

<script>
export default{
    props:[
        'name',
        'phoneNumber',
        'emailAddress'
    ],
    data(){
        return{
            detailsAreVisible: false,
            friend: {
                id: 'miles',
                name: 'Miles Inada',
                phone: '8083469737',
                email: 'milesinada219@gmail.com'
            },
        };
    },
    methods: {
        toggleDetails(){
            this.detailsAreVisible = !this.detailsAreVisible;
            
        },
    }
};
</script>