<script setup>
import dashboard from './components/dashboard.vue'
import toph from './components/toph.vue'
import chatbar from './components/chatbar.vue';
import chatlist from './components/chatlist.vue';
import ChatBox from './components/ChatBox.vue'
</script>

<template>
        <div class="raw d-flex ">
            <div class="col-2">
                <dashboard/>
            </div>
            <div class="col-10 bg rounded">
                <toph/>
                <chatbar class="py-4"/>
                <div class="raw d-flex ms-1 mt-5 ">
                    <div class="tbg d-flex ms-5 rounded">
                    <div class="col-3">
                        <chatlist/>
                    </div>
                    <div class="col-9 chat-box ms-3">
                        <ChatBox/>
                    </div>
                </div>
                </div>
            </div>
        </div>
</template>

<style scoped>
.bg{
    background-color: rgb(244, 247, 251);
    height: 140vh   ;
    max-width:90%;
}
.tbg{
    background-color: rgb(255, 255, 255);
    max-height: 90vh ;
}
.chat-box {
  background: transparent;
  border-radius: 0 10px 10px 0;
  width: 850px;
  height: 100vh; 
}

</style>
