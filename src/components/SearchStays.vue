<template>
    <div class="search-container">
        <img src="../assets/logo.png" class="logo-img" v-if="!startSearch" />

        <div class="search-bar" :class="startSearch ? 'search-bar-full' : ''">
            <div class="field">
                <p class="label-txt" v-if="startSearch">LOCATION</p>
                <p class="main-txt">Add location</p>
            </div>
            <div class="v-line"></div>
            <div class="field">
                <p class="label-txt" v-if="startSearch">GUESTS</p>
                <p class="placeholder-txt">Add guests</p>
            </div>
            <div class="v-line"></div>
            <div class="search-btn">
                <span class="material-icons search-icon">search</span>
                <p v-if="startSearch">Search</p>
            </div>
        </div>
    </div>
</template>

<script setup>

// regulise da li je pretraga ili se samo prikazuju odabrani parametri pretrage
const startSearch = false;
</script>

<style scoped>
.search-container {
    display: flex;
}

.search-bar {
    display: flex;
    justify-content: space-evenly;
    width: 30%;
    margin-left: auto;
    box-shadow: 0px 1px 6px 0px #0000001A;
    border-radius: 16px;
}

.search-bar-full {
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1px 1fr 1px 1fr;
}

.field {
    width: 100%;
    border: 1px solid white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 16px;
}

.field:hover {
    border: 1px solid black;
    border-radius: 16px;
    transition: border 2s;
}

.placeholder-txt {
    color: #BDBDBD;
}

.main-txt {
    color: #333333;
}

.label-txt {
    font-size: 9px;
    font-weight: 800;
    line-height: 11px;
    letter-spacing: 0em;
}

.search-btn {
    display: flex;
    justify-content: center;
    align-content: center;
    padding: 16px;
    border-radius: 16px;
}

.search-icon {
    color: #EB5757;
}

.search-btn:hover {
    color: red;
    transition: color 2s;
}

.v-line {
    border-left: 1px solid #F2F2F2;
}

img {
    object-fit: contain;
}

@media only screen and (width: 600px) {
    .search-container {
        display: flex;
        flex-direction: column;
    }

    .search-bar {
        width: 100%;
    }
}
</style>