
<script setup>
import u0 from '@/assets/u0.png'
</script>
<script>

import u1 from '@/assets/u1.png'
import u2 from '@/assets/u2.png'
import u3 from '@/assets/u3.png'
import u4 from '@/assets/u4.png'
import u5 from '@/assets/u5.png'
export default {
  data() {
    return {
      search: "",
      chats: [
        {
          name: "Michell Flintoff",
          message: "You: Yesterday w...",
          time: "15 minutes",
          avatar: u1,
          status: "online",
        },
        {
          name: "Bianca Anderson",
          message: "Nice looking dre...",
          time: "30 minutes",
          avatar: u2,
          status: "offline",
        },
        {
          name: "Andrew Johnson",
          message: "Sent a photo",
          time: "2 hours",
          avatar: u3,
          status: "away",
        },
        {
          name: "Mark Johnson",
          message: "Lorem ipsum text ...",
          time: "3 hours",
          avatar: u2,
          status: "away",
        },
        {
          name: "Mark Strokes",
          message: "Lorem ipsum text ...",
          time: "5 days",
          avatar: u4,
          status: "online",
        },
        {
          name: "Mark, Stoinus & Rish...",
          message: "Lorem ipsum text ...",
          time: "5 days",
          avatar: u5,
          status: "online",
        },
      ],
      statusColors: {
        online: "bg-green-500",
        offline: "bg-red-500",
        away: "bg-yellow-500",
      },
    };
  },
  computed: {
    filteredChats() {
      return this.chats.filter(chat =>
        chat.name.toLowerCase().includes(this.search.toLowerCase())
      );
    },
  },
};
</script>

<template>
  <div class=" sidebar chat-sidebar">
    <div class="d-md-block bg-white profile ms-1 mt-3">
      <div class="profile-info">
          <img :src="u0" class="u " height="45" width="45">
          <div class="user">
            <h3>Mathew Anderson</h3>
            <p>Marketing Director</p>
          </div>
          <i class="bi bi-three-dots-vertical ms-5 p"></i>
          </div>
        <div class="mt-4">
      <input
        v-model="search"
        type="text"
        placeholder="Search contacts"
        class="px-3 py-1 fs-6 ser rounded border"
      />
        </div>

    <div class="mt-4 ">
      <div class="dropdown-center">
        <button class="btn rounded dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            Recent chats
          </button>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Recent chats</a></li>
            <li><a class="dropdown-item" href="#">oldest chats</a></li>
            <li><a class="dropdown-item" href="#">Action three</a></li>
          </ul>
        </div>
      <div class="chat-list">
      <div 
        v-for="(chat, index) in filteredChats" 
        :key="index" 
        class="chat-item p"
      >
        <div class="avatar-wrapper">
          <img
            :src="chat.avatar"
            :alt="chat.name"
            class=" avatar"
          />
          <span
            style="width: 8px; height: 8px;"
            class="ms-1 mt-5 rounded"
            :class="statusColors[chat.status]"
          ></span>
        </div>
        <div class="chat-info">
        <div class="chat-header">
           <h4>{{ chat.name }}</h4>
           <span class="time">{{ chat.time }}</span>
          </div>
          <p class="message">{{ chat.message }}</p>
          </div>
      </div>
    </div>
  </div>
  </div>
</div>
</template>

<style scoped>
.p{
  cursor: pointer;
}
.ser{
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  margin-top: 15px;
  width: auto;
  position: relative;
}
.ser input {
  width: 90%;
  padding: 9px;
  border: 1px solid #ddd;
  border-radius: 5px;
  outline: none;
  font-size: 14px;
  padding: 10px 40px;
}
.ser i {
  position: absolute;
  left: 12px;
  top: 50%;
  transform: translateY(-50%);
  color: #888;
  font-size: 16px;
}
.ser input::placeholder {
  color: gray;
}

.bg-green-500 {
  background-color: #10b981;
}
.bg-red-500 {
  background-color: #ef4444;
}
.bg-yellow-500 {
  background-color: #facc15;
}
.profile {
  display: flex;
  align-items: center;
  gap: 10px;
  border-right: 1px solid #ddd;
  height: 636px;
}
.profile-info {
  display: flex;
  align-items: center; 
  gap: 10px; 
}
.u {
  width: 45px;
  height: 45x;
  border-radius: 50%;
  border: 2px solid #e0e0e0;
}
.user {
  display: flex;
  flex-direction: column; 
  justify-content: center;
  margin: 0;
  padding: 0;
  height: 45px;
  line-height: 1.2; 
}
.user h3 {
  font-size: 16px;
  margin: 0;
}
.user p {
  font-size: 12px;
  color: gray;
  margin: 3px;
}
.chat-list {
  width: auto;
  border:none;
  overflow: hidden;
  background: #fff;
} 
.chat-item {
  display: flex;
  align-items: center;
  padding: 10px;
}
.chat-item:hover {
  background-color: rgb(246, 247, 249);
}
.chat-item.active {
  background-color: #e0f7fa;
}
.avatar-wrapper {
  position: relative;
  margin-right: 12px;
}
.chat-item:last-child {
  border-bottom: none;
}
.avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
}
.chat-info {
  flex: 1;
}
.chat-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.chat-header h4 {
  margin: 0;
  font-size: 16px;
}
.time {
  font-size: 12px;
  color: #999;
}
.message {
  margin: 5px 0 0;
  color: rgb(152, 164, 174);
  font-size: 12px;
}
.chat-sidebar {
  width: max-content;
  height: auto;
  background: #ffffff;
  padding: 20px;
  border-radius: 10px 0 0 10px;
  font-family: Arial, sans-serif; 
}
</style>