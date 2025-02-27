<script setup>
import logo from '@/assets/logo.png';
</script>

<template>
    <div class="container-fluid mw"> 
            <nav class=" d-md-block bg-white hv-100">
                <div class="raw d-flex px-4">
                <img :src="logo" class=" object-fit-scale logo" alt="...">
                <h6 class="mt-5">Hi TEAM</h6>


            </div>
                <ul class="nav flex-column px-4 mt-4 ">
                    <li class="nav-item ic p-2"><i class=" bi bi-house"></i>  Dashboard</li>
                    <li class="nav-item ic p-2"><i class=" bi bi-box"></i>  Orders</li>
                    <li class="nav-item ic p-2"><i class=" bi bi-people"></i>  Passengers</li>
                    <li class="nav-item ic p-2"><i class=" bi bi-car-front"></i>  Captains</li>
                    <li class="nav-item ic p-2"><i class=" bi bi-clipboard"></i>  Categories</li>
                    <hr></hr>
                    <li class="nav-item ic p-2"><i class=" bi bi-card-text"></i>  Settlement</li>
                    <hr></hr>
                    <li class="nav-item ic p-2"><i class=" bi bi-chat-left-text"></i>  Contact</li>
                    <li class="nav-item ic p-2"><i class=" bi bi-stars"></i>  Reviews</li>
                    <hr></hr>
                    <li class="nav-item ic p-2"><i class="bi bi-shield"></i>  Permissions</li>
                    <li class="nav-item ic p-2"><i class="bi bi-translate"></i>  Translation</li>
                    <li class="nav-item ic p-2"><i class="bi bi-film"></i>  Education Video</li>
                    <li class="nav-item ic p-2"><i class="bi bi-gear"></i>  Settings</li>
                    <li class="nav-item ic p-2"><i class="bi bi-grid-3x2-gap-fill"></i>  Content</li>
                </ul>
            </nav>
            
    </div>
</template>

<style scoped>
.bg{
    background-color: white;
}
.logo{
max-width:100px;
max-height: 100px;
}
.nav-item:hover {
    background-color: rgba(30, 42, 255, 0.789);
    box-shadow: 0 0 10px rgba(99, 91, 255, 0.897);
    border-radius: 5px;
    color: rgb(255, 255, 255);
}
.mw{
    max-width: 300px;
}
.ic:hover i{
    color: rgb(255, 255, 255);
}
.ic i{
    color: rgb(152, 164, 174);
}
</style>