<script setup>

</script>

<template>
   <div class="container px-0">
        <div class="chat-bar">
            <h5 class="mb-0">Chat</h5>
            <nav>
                <ul class="breadcrumb ">
                    
                        <i class="mt-2 px-1 bi bi-house-door"></i>

                        <h6 class="mt-2 px-1">/</h6>
                    <li class="breadcrumb-item active">Chat</li>
                </ul>
            </nav>
        </div>
    </div>
</template>

<style scoped>
.chat-bar {
            background: white;
            padding: 10px 20px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }
.breadcrumb {
            margin-bottom: 0;
        }
.breadcrumb-item.active {
            background: rgba(124, 106, 255, 0.2);
            padding: 5px 10px;
            border-radius: 8px;
            color: #7C6AFF;
        }
</style>