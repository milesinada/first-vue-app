<template>
    <li>
        <h2>{{friend.name}}</h2>
        <button @click="toggleDetails">{{ detailsAreVisible ? 'Hide' : 'Show' }} Details</button>        
        <ul v-if="detailsAreVisible">
            <li><strong>Phone:</strong>{{friend.phone}}</li>
            <li><strong>EMail:</strong>{{friend.email}}</li>
        </ul>
    </li>
</template>

<script>
export default{
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