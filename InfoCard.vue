<template>
    <div>
        <h2>{{ name }}</h2>
        <h6>Phone: {{ phoneNumber }}</h6>
        <h6>email: {{ emailAddress }}</h6>
        <h6>favarite: {{ isFavorite }}</h6>
    </div>
</template>

<script>
export default {
    props: [
        'name',
        'phoneNumber',
        'emailAddress',
        'isFavorite'
    ]
}
</script>
