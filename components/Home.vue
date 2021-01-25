<template>
  <div class="h-screen bg-cover login flex justify-center">
    <div class="flex bg-gray mt-10 py-10 mb-40 px-1 rounded-xl" v-show="showSelect">
     <div class="container mr-3 py-1 max-w-md mx-auto">
       <Center> <label class="font-semibold justify-center  text-green-800 pb-5 block">Movie Application</label>
        </Center> 
        <br>
        
       <v-select
          id="movie"
          v-model="Name"
          :options="movieNameOption"
          :clearable="false"
          placeholder=
          "List Movie"
          class="text"
                   
        />
        <Center> <button @click="search" type="button" class="  text-blue-800 rounded px-1 py-5  mr-2 text-black">
         ค้นหาข้อมูลที่เลือก
          </button>
          </Center> 
     

          <br>
          <br>
        <label class="font-semibold  text-green-800  pb-1 block">English Name  </label>
        <input
          v-model="En"
          disabled
          type="text"
          class="border rounded-lg px-5 py-2 mt-1 mb-5 text-sm w-full"
          placeholder=""
        />
        <label class="font-semibold text-sm text-green-800 "> Thai Name </label>
        <input
          v-model="Th"
          disabled
          type="text"
          class="border rounded-lg px-3 py-2 mt-1 mb-5 text-sm w-full"
          placeholder=""
        />
        <label class="font-semibold text-sm text-green-800  pb-1 block">ปีที่เข้าฉาย</label>
        <input
          v-model="Year"
          disabled
          type="text"
          class="border rounded-lg px-3 py-2 mt-1 mb-5 text-sm w-full"
          placeholder=""
        />
        <div class="container mr-3 py-1 max-w-md mx-auto">
         
          
          
        </div>
      </div>
    </div>     
     </div>
  
  
</template>

<script>
import Vue from 'vue'
import vSelect from 'vue-select'
import 'vue-select/dist/vue-select.css'
Vue.component('v-select', vSelect)
export default {
  data() {
    return {
      Name: '',
      En: '',
      Th: '',
      Year: '',
      showSelect: true,
      showMovie: false,
         
      movieNameOption: [
        {
          En: 'Star Wars: The Last Jedi	',
          Th: 'สตาร์ วอร์ส: ปัจฉิมบทแห่งเจได',
          year: '2017',
          label: 'Star Wars: The Last Jedi'
        },
        {
          En: 'Jurassic World: Fallen Kingdom',
          Th: 'จูราสสิค เวิลด์ อาณาจักรล่มสลาย',
          year: '2015',
          label: 'Jurassic World: Fallen Kingdom'
        },
         {
          En: 'Frozen	',
          Th: 'ผจญภัยแดนคำสาปราชินีหิมะ',
          year: '2019',
          label: 'Frozen'
        },
        {
          En: 'Beauty and the Beast',
          Th: 'โฉมงามกับเจ้าชายอสูร',
          year: '2017',
          label: 'Beauty and the Beast'
        },
         {
          En: 'Incredibles 2	',
          Th: 'รวมเหล่ายอดคนพิทักษ์โลก 2',
          year: '2018',
          label: 'Incredibles 2'
        },
        {
          En: 'The Fast and Furious 8',
          Th: 'เร็ว...แรงทะลุนรก 8',
          year: '2017',
          label: 'The Fast and Furious 8'
        },
         
        {
          En: 'Minions',
          Th: 'มินเนี่ยน',
          year: '2015',
          label: 'Minions'
        },
         {
          En: 'Captain America: Civil War	',
          Th: 'กัปตันอเมริกา: ศึกฮีโร่ระห่ำโลก',
          year: '2016',
          label: 'Captain America: Civil War'
        },
        {
          En: 'Aquaman',
          Th: 'อควาแมน เจ้าสมุทร',
          year: '2018',
          label: 'Aquaman '
        }
        
      ]
    }
  },
  methods: {
    search() {
      this.En = this.Name.En
      this.Th = this.Name.Th
      this.Year = this.Name.year
      if (this.Name !== '') {
        this.showEditbutton = true
      }
    },
      
         
      
  }
}
</script>



   

