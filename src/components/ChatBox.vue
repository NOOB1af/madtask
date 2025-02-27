<script setup>
import u1 from '@/assets/u1.png'
import u3 from '@/assets/u3.png'
import ch1 from '@/assets/ch1.png'
import m1 from '@/assets/m1.png'
import m2 from '@/assets/m2.png'
import m3 from '@/assets/m3.png'
import m5 from '@/assets/m5.png'
import m6 from '@/assets/m6.png'
import m7 from '@/assets/m7.png'
import m8 from '@/assets/m8.png'
import m9 from '@/assets/m9.png'
</script>

<script>
export default {
  data() {
    return {
      showmedia: false,
      showBlockModal: false,
      showUnlockModal: false,
      showDeleteModal: false,
    };
  },
  methods: {
    togglemedia() {
      this.showmedia = !this.showmedia;
    }
  }
};
</script>


<template>
    <div class="row d-flex box">
        <div class="col-12 chat-container ">
            <header class="d-flex justify-content-between align-items-center bg-white p-3 header1">
                <div class="profile1 d-flex align-items-center me-auto">
                    <img :src="u1" class="rounded-circle" height="40" width="40">
                    <span class="away">Away</span>
                </div>
                <div class="d-flex align-items-center icons">
                  <div>
                    <i class="bi bi-ban ms-5 i1 cursor-pointer" @click="showBlockModal = true"></i>
                    <div v-if="showBlockModal" class="modal-backdrop fade show" @click="showBlockModal = false"></div>
                    <div v-if="showBlockModal" class="modal fade show d-block" tabindex="-1">
                      <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content text-center p-4">
                          <div class="modal-body">
                            <i class="bi bi-ban i1 d-block mx-auto mb-3"></i>
                            <h5 class="fw-bold">Block User</h5>
                            <p class="text-muted">You Are Going To Block This User, Are You Sure?</p>
                          </div>
                          <div class="modal-footer d-flex justify-content-center border-0">
                            <button class="btn btn-cancel px-4" @click="showBlockModal = false">Cancel</button>
                            <button class="btn btn-yes px-4">Yes</button>
                          </div>
                        </div>
                      </div>
                    </div>
                    <i class="bi bi-unlock ms-4 cursor-pointer" @click="showUnlockModal = true"></i>
                    <div v-if="showUnlockModal" class="modal-backdrop fade show" @click="showUnlockModal = false"></div>
                    <div v-if="showUnlockModal" class="modal fade show d-block" tabindex="-1">
                      <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content text-center p-4">
                          <div class="modal-body">
                            <i class="bi bi-unlock i1 d-block mx-auto mb-3"></i>
                            <h5 class="fw-bold">Unlock User</h5>
                            <p class="text-muted">You Are Going To Unblock This User, Are You Sure?</p>
                          </div>
                          <div class="modal-footer d-flex justify-content-center border-0">
                            <button class="btn btn-cancel px-4" @click="showUnlockModal = false">Cancel</button>
                            <button class="btn btn-yes px-4">Yes</button>
                          </div>
                        </div>
                      </div>
                    </div>
                    <i class="bi bi-trash3 ms-4 i2 cursor-pointer" @click="showDeleteModal = true"></i>
                    <div v-if="showDeleteModal" class="modal-backdrop fade show" @click="showDeleteModal = false"></div>
                    <div v-if="showDeleteModal" class="modal fade show d-block" tabindex="-1">
                      <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content text-center p-4">
                          <div class="modal-body">
                            <i class="bi bi-trash3 i1 d-block mx-auto mb-3"></i>
                            <h5 class="fw-bold">Delete Conversation</h5>
                            <p class="text-muted">Once You Sure To Delete This Conversation, You Will Not Be Able To Undo This Action</p>
                          </div>
                          <div class="modal-footer d-flex justify-content-center border-0">
                            <button class="btn btn-cancel px-4" @click="showDeleteModal = false">Cancel</button>
                            <button class="btn btn-yes px-4">Yes</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                    <i class="bi bi-telephone ms-4 p"></i>
                    <i class="bi bi-camera-video ms-3 p"></i>
                    <i class="bi bi-list ms-3 me-3 i3 p"></i>
                    
                </div>
            </header>
        <div class="row">
            <div class="col-8 view-chat">
                <div class="container chat">
                    <div class="d-flex align-items-center">
                    <img :src="u3" class="u rounded-circle" height="45" width="45">
                    <div class="ms-3">
                      <p class="p1">Andrew, 2hours ago</p>
                    </div>
                    </div>
                      <p class="ms-5 ps-2 p2">If I don't like something, I'll stay away from it.</p>
                </div>
                <div class="d-flex justify-content-end">
                    <div class="ms-3 ">
                    <p class="p3">2hours ago</p>
                    </div>
                </div>
                      <p class="ps-2 pe-3 p4 ">If I don't like something, I'll stay away from it.</p>
                <div class="container chat">
                    <div class="d-flex align-items-center">
                      <img :src="u3" class="u rounded-circle" height="45" width="45">
                    <div class="ms-3">
                      <p class="p1">Andrew, 2hours ago</p>
                    </div>
                    </div>
                      <p class="ms-5 ps-2 p2">I want more detailed information.</p>
                </div>
                <div class="d-flex justify-content-end">
                    <div class="ms-3 ">
                    <p class="p3">2hours ago</p>
                    </div>
                </div>
                    <p class="ps-2 pe-3 p4 ">If I don't like something, I'll stay away from it.</p>
                    <p class="ps-2 pe-3 p5">They got there early, and they got really good seats.</p>
                <div class="container chat">
                    <div class="d-flex align-items-center">
                      <img :src="u3" class="u rounded-circle" height="45" width="45">
                    <div class="ms-3">
                      <p class="p1">Andrew, 2hours ago</p>
                    </div>
                    </div>
                      <img :src="ch1" class="image1 mt-1" height="80" width="104">
                </div>
                <div>
                  <div class="d-flex justify-content-between align-items-center bg-white mt-2  massage">
                    <div class="profile1 d-flex align-items-center me-auto mt-1">
                      <i class="bi bi-emoji-smile ms-0 p"></i>
                      <p class="massage1">Type a massage</p>
                    </div>
                    <div class="d-flex align-items-center icons">
                      <i class="ic1 bi bi-image p"></i>
                      <i class="ic1 bi bi-paperclip p"></i>
                      <i class="ic1 bi bi-mic p"></i>
                    </div>
                  </div>
                </div>
            </div>
            <div class="col-4 m-sidebar">
                <div class="container">
                  <h6>Media <span class="number">(36)</span></h6>
                  <div class="image2">
                    <img :src="ch1" class="mt-1" height="64" width="68">
                    <img :src="m1" class="mt-1" height="64" width="68">
                    <img :src="m2" class="mt-1" height="64" width="68">
                  </div>
                  <div class="image3">
                    <img :src="m3" class="mt-1" height="64" width="68">
                    <img :src="ch1" class="mt-1" height="64" width="68">
                    <img :src="m1" class="mt-1" height="64" width="68">
                  </div>
                  <h6 class="mt-3">Files <span class="number">(36)</span></h6>
                  <div class="image4">
                    <div class="files-info">
                      <img :src="m5" class="mt-1 ms-0" height="53" width="53">
                      <div class="info mt-1">
                        <h6>service-task.pdf</h6>
                        <p>2MB 2 Dec 2022</p>
                      </div>
                    </div>
                    <div class="files-info">
                      <img :src="m6" class="mt-1 ms-1" height="48" width="48">
                      <div class="info mt-1">
                        <h6>homepage-design.fig</h6>
                        <p>2MB 2 Dec 2022</p>
                      </div>
                    </div>
                    <div class="files-info">
                      <img :src="m7" class="mt-1 ms-1" height="48" width="48">
                      <div class="info mt-1">
                        <h6>about-us.html</h6>
                        <p>2MB 2 Dec 2022</p>
                      </div>
                    </div>
                    <div class="files-info">
                      <img :src="m8" class="mt-1 ms-1" height="50" width="46">
                      <div class="info mt-1">
                        <h6>work-project.zip</h6>
                        <p>2MB 2 Dec 2022</p>
                      </div>
                    </div>
                    <div class="files-info">
                      <img :src="m9" class="mt-1 ms-1" height="48" width="48">
                      <div class="info mt-1">
                        <h6>custom.js</h6>
                        <p>2MB 2 Dec 2022</p>
                      </div>
                    </div>
                  </div>
                </div>
            </div>
        </div>
        </div>
    </div>
</template>

<style>
.profile1 {
  display: flex;
  align-items: center;
  gap: 10px;
}
.header1{
  border-bottom: 1px solid #ddd;
  width: 861.5px;
}
.away {
  color: rgb(152, 164, 174); 
  font-size: 14px; 
}
.i1{
  color: rgb(99, 91, 255);
}
.i2{
  color:rgb(255, 0, 0)
}
.i3 {
  font-size: 25px;
  color: black ;
}

.view-chat {
  background: rgba(255, 255, 255, 0); 
  padding: 15px;
  height: auto;
  overflow-y: auto; 
}
.m-sidebar {
  background: rgba(255, 255, 255, 0); 
  padding: 15px;
  height: auto; 
  border-left: 1px solid #ddd; 
  overflow-y: auto;
}
.p1 {
  color: rgb(152, 164, 174); 
  font-size: 14px;
  margin: 0;
}
.p2 {
  display: inline-block;
  border: 1px solid rgb(239, 244, 250);
  padding: 4px;
  border-radius: 6px;
  background-color: rgb(239, 244, 250);
}
.p3{
  color: rgb(152, 164, 174); 
  font-size: 14px;
  margin: 0;
}
.p4{
  text-align: right; 
  margin-left: auto;
  margin-right: 0;
  margin-left: 210px;
  border: 1px solid rgb(236, 253, 253);
  padding: 4px;
  border-radius: 6px;
  background-color: rgb(236, 253, 253);
}
.p5{
  text-align: right; 
  margin-left: auto;
  margin-right: 0;
  margin-left: 160px;
  border: 1px solid rgb(236, 253, 253);
  padding: 4px;
  border-radius: 6px;
  background-color: rgb(236, 253, 253);
}
.image1{
  margin-left: 61px;
}
.massage{
  border-top: 1px solid #ddd;
}
.massage1{
  color: rgb(152, 164, 174); 
  font-size: 14px;
  border-radius: none;
  margin: 0;
  padding: 0;
}
.ic1{
  margin-left: 15px;
  padding: 0;
}
.number{
  color:rgb(152, 164, 174)
}
.image2, .image3 {
  display: flex;
  gap: 10px;
}
.image2 img, .image3 img {
  border-radius: 15px;
  object-fit: cover;   
}
.image4{
  display: flex;
  flex-direction: column;
  gap: 5px;
}
.image4 img{
  object-fit: cover;
}
.files-info{
  display: flex;
  align-items: center; 
  gap: 5px;
  font-size: 1pc;
}
.info {
  display: flex;
  flex-direction: column; 
  justify-content: center;
  margin: 0;
  padding: 0;
  height: 45px;
  line-height: 1.2; 
}
.info h6{
  font-size: 16px;
  margin: 0;
}
.info p{
  font-size: 12px;
  color: gray;
  margin: 3px;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(83, 83, 83, 0.323) !important;
  z-index: 1040;
}
.cursor-pointer {
  cursor: pointer;
}
.btn-yes {
  background-color: rgb(87, 92, 212) !important; 
  color: rgb(255, 255, 255) !important;
  border: none;
}
.btn-cancel {
  background-color: rgb(149, 149, 149) !important; 
  color: white !important;
  border: none;
}
.btn-yes:hover {
  filter: brightness(1.2);
}
.btn-cancel:hover {
  filter: brightness(1.2);
}
.p{
  cursor: pointer;
}
</style>
