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
    <div class="container h" style="width: max-content;">
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
</template>

<style scoped>
.h{
  border-left: 1px solid #ddd;
  padding-top: 10px;
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
</style>