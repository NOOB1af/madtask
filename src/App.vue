<script setup>
import dashboard from './components/dashboard.vue'
import toph from './components/toph.vue'
import chatbar from './components/chatbar.vue';
import chatlist from './components/chatlist.vue';
import ChatBox from './components/ChatBox.vue'


</script>

<template>
    <div class="container-fluid tbg ">
        <div class="raw d-flex ">
            <div class="col-2" style="min-width: 212px;">
                <dashboard/>
            </div>
            <div class="col-10 d rounded bg  br">
                <toph/>
                <chatbar class="py-4 ms-5"style="max-width: 90%;" />
                <div class="container ms-5 mt-5 rounded d w">
                    <div class="raw d-flex  ">
                        <div class=" c ">
                            <chatlist/>
                        </div>
                        <div class=" ">
                            <ChatBox/>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.w{
min-width: auto;
}
.c{
    border-right: 1px solid #ddd;
    max-width: max-content;
}
.d{
    background-color: #fff;
    max-width: max-content;
}
.bg{
    
    height: 140vh   ;
    max-width:100%;
    background-color: rgb(244, 247, 251);
    min-width: 950px;
}
.tbg{
    background-color: rgb(255, 255, 255);
    max-height: 100px ;
    width:100%;
}


</style>
