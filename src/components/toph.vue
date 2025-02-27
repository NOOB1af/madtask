<script setup>

</script>

<template>
    <header class="d-flex justify-content-between align-items-center ll py-5">
        
            <div class="d-flex align-items-center mt-3">
                <i class="bi bi-search nav-item fs-5"></i>
                <i class="bi bi-grid nav-item fs-5"></i>
            </div>
            
            <div class=" d-flex align-items-center">
                <i class="bi bi-moon nav-item fs-5"></i>
                <i class="bi bi-bell nav-item fs-5"></i>
                <img src="https://flagcdn.com/w40/gb.png" alt="UK Flag" class="nav-item" width="30">
                <img src="https://randomuser.me/api/portraits/men/1.jpg" alt="User" class="profile-img nav-item">
                <i class="bi bi-caret-down-fill nav-item"></i>
        
        </div>
</header>
</template>

<style scoped>
 .ll {
            background-color: white;
            padding: 10px 20px;
            height: 60px;
        
        }
        .nav-item {
            margin: 0 10px;
            cursor: pointer;
        }
        .profile-img {
            width: 35px;
            height: 35px;
            border-radius: 50%;
        }
</style>