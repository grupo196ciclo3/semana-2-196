<template>    
    <div class="card text-white h-100" v-bind:class="member.codigo % 2 === 0? 'bg-dark': 'bg-danger'" role="alert">
        <div class="d-flex justify-content-center align-center p-2">
            <img v-bind:src="member.image" alt="Foto Miembro" class="img-fluid w-50"/>
        </div>
        <div class="card-body">
            <h5 class="card-title text-center">{{member.nombre}}</h5>
            <h6 class="card-subtitle text-center mb-2">Codigo: {{member.codigo}}</h6>
            <p class="card-text text-center">{{member.descripcion}}</p>
            <p class="card-text text-center">{{member.rol}}</p>
        </div>
    </div>    
</template>

<script>
export default {
    name: "TeamCard",
    props: {
        member: Object,
    },
};
</script>

<style scoped>
</style>
