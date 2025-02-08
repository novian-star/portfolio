<script setup lang="ts">
import {
  Briefcase,
  Building,
  Cake,
  Facebook,
  Github,
  Mail,
  Mars,
  Phone,
  School,
  University,
  User,
} from 'lucide-vue-next';
import PapgerPage from '../PapgerPage.vue';

const age = new Date().getFullYear() - new Date('2002-04-15').getFullYear();

const contacts = [
  {
    icon: Phone,
    label: '064-098-8485',
    value: '064-098-8485',
    href: 'tel:0640988485',
  },
  {
    icon: Mail,
    label: 'humanityisyour@gmail.com',
    value: 'humanityisyour@gmail.com',
    href: 'mailto:humanityisyour@gmail.com',
  },
  {
    icon: Facebook,
    label: 'Natchapak Pontawin',
    value: 'Natchapak Pontawin',
    href: 'https://www.facebook.com/natchapak.pontawin',
  },
  {
    icon: Github,
    label: 'novian-star',
    value: 'novian-star',
    href: 'https://github.com/novian-star',
  },
];

const educationRecords = [
  {
    title: 'โรงเรียนพระนารายณ์',
    level: 'มัธยมศึกษาตอนปลาย',
    branch: 'อังกฤษ-คณิต',
    location: 'ลพบุรี',
    period: 'พ.ศ. 2560-2562',
    gpa: '3.89',
    icon: School,
  },
  {
    title: 'มหาวิทยาลัยราชภัฏเทพสตรี',
    level: 'ปริญญาตรี (เกียรตินิยมอันดับ 1)',
    branch: 'วิศวกรรมสารสนเทศและการสื่อสาร',
    location: 'ลพบุรี',
    period: 'พ.ศ. 2563-2567',
    gpa: '3.91',
    icon: University,
  },
];

const experienceRecords = [
  {
    title: 'นักศึกษาฝึกงาน',
    company: 'การไฟฟ้าส่วนภูมิภาค เขต 3 (ภาคเหนือ) จังหวัดลพบุรี',
    department: 'กองดิจิทัลและการสื่อสาร',
    period: 'พฤศจิกายน 2566 - มกราคาม 2567',
    description: 'ทดลองพัฒนาระบบจองรถ ระบบการแจ้งซ่อม',
    icon: Building,
  },
  {
    title: 'ลูกจ้างชั่วคราว',
    company: 'การไฟฟ้าส่วนภูมิภาค เขต 3 (ภาคเหนือ) จังหวัดลพบุรี',
    department: 'กองดิจิทัลและการสื่อสาร',
    period: 'มิถุนายน 2567 - ปัจจุบัน',
    description: 'พัฒนาแอพพลิเคชันเพื่อทุ่นแรงในการทำงาน',
    icon: Briefcase,
  },
];

const toolsUsed = [
  {
    icon: 'https://api.iconify.design/logos:visual-studio-code.svg',
    href: 'https://code.visualstudio.com/',
  },
  {
    icon: 'https://api.iconify.design/logos:html-5.svg',
    href: 'https://developer.mozilla.org/en-US/docs/Web/HTML',
  },
  {
    icon: 'https://api.iconify.design/logos:css-3.svg',
    href: 'https://developer.mozilla.org/en-US/docs/Web/CSS',
  },
  {
    icon: 'https://api.iconify.design/logos:javascript.svg',
    href: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript',
  },
  {
    icon: 'https://api.iconify.design/logos:typescript-icon.svg',
    href: 'https://www.typescriptlang.org/',
  },
  {
    icon: 'https://api.iconify.design/logos:github-icon.svg',
    href: 'https://github.com',
  },
  {
    icon: 'https://api.iconify.design/logos:nodejs-icon-alt.svg',
    href: 'https://nodejs.org/',
  },
  {
    icon: 'https://api.iconify.design/logos:bun.svg',
    href: 'https://bun.sh/',
  },
  {
    icon: 'https://api.iconify.design/logos:vue.svg',
    href: 'https://vuejg.org/',
  },
  {
    icon: 'https://api.iconify.design/logos:nuxt-icon.svg',
    href: 'https://nuxt.com/',
  },
  {
    icon: 'https://api.iconify.design/logos:tailwindcss-icon.svg',
    href: 'https://tailwindcss.com/',
  },
  {
    icon: 'https://api.iconify.design/logos:prisma.svg',
    href: 'https://prisma.io/',
  },
  {
    icon: 'https://api.iconify.design/logos:postgresql.svg',
    href: 'https://www.postgresql.org/',
  },
  {
    icon: 'https://api.iconify.design/logos:vercel-icon.svg',
    href: 'https://vercel.com/',
  },
  {
    icon: 'https://api.iconify.design/logos:neon-icon.svg',
    href: 'https://neon.tech/',
  },
  {
    icon: 'https://api.iconify.design/logos:firebase.svg',
    href: 'https://www.nginx.com/',
  },
];
</script>

<template>
  <PapgerPage>
    <div class="w-full h-full bg-neutral-200">
      <!-- Header -->
      <div class="flex p-8 gap-8 bg-white shadow">
        <div class="flex items-center justify-center w-3xs">
          <img
            class="w-48 h-48 rounded-2xl"
            src="/natchapuk-phonthawil-portrait.jpg"
            alt="Profile Picture"
          />
        </div>

        <div class="flex flex-col flex-1 gap-2">
          <h1 class="font-semibold text-4xl text-highlighted">ณัชภัค ผลถวิล</h1>

          <hr class="border-neutral-200" />

          <div class="flex flex-1 items-center justify-center">
            <p class="text-center text-sm text-muted">
              “ผมชอบการเรียนรู้นวัตกรรมใหม่ ๆ การสร้างสรรค์ ให้ทันต่อโลกปัจจุบัน
              และในอนาคต พร้อมนำความรู้
              ความสามารถมาพัฒนาผลงานและชิ้นงานให้ตรงตามเป้าหมายที่วางไว้”
            </p>
          </div>

          <div class="flex items-center justify-around gap-2 text-xs">
            <!-- Gender -->
            <div class="flex items-center gap-1 text-muted">
              <Mars class="w-4 h-4" />

              <span>เพศชาย</span>
            </div>

            <!-- Birthday -->
            <div class="flex items-center gap-1 text-muted">
              <Cake class="w-4 h-4" />

              <span>15 เมษายน 2545</span>
            </div>

            <!-- Age -->
            <div class="flex items-center gap-1 text-muted">
              <User class="w-4 h-4" />

              <span>อายุ {{ age }} ปี</span>
            </div>
          </div>
        </div>
      </div>

      <div class="p-8 space-y-8">
        <div class="flex gap-8">
          <!-- Contact -->
          <div class="min-w-3xs bg-white rounded shadow overflow-auto">
            <div class="p-4 border-b bg-emerald-700">
              <h2 class="font-semibold text-white">ข้อมูลติดต่อ</h2>
            </div>

            <div class="p-4">
              <ul class="space-y-4">
                <template v-for="contact in contacts" :key="contact.value">
                  <li class="flex items-center gap-2 text-xs">
                    <component :is="contact.icon" class="w-4 h-4" />

                    <a
                      class="text-neutral-700"
                      :href="contact.href"
                      target="_blank"
                    >
                      {{ contact.value }}
                    </a>
                  </li>
                </template>
              </ul>
            </div>
          </div>

          <!-- Education record -->
          <div class="flex-1 bg-white rounded shadow overflow-auto">
            <div class="p-4 border-b bg-emerald-700">
              <h2 class="font-semibold text-white">ประวัติการศึกษา</h2>
            </div>

            <div class="p-4">
              <ul class="space-y-4">
                <template
                  v-for="record in educationRecords"
                  :key="record.value"
                >
                  <li class="text-xs">
                    <div class="space-y-2">
                      <h3
                        class="flex items-center gap-2 font-semibold text-neutral-700"
                      >
                        <component :is="record.icon" class="w-5 h-5" />

                        {{ record.level }}
                      </h3>

                      <p class="text-neutral-500">
                        {{ record.title }} - {{ record.branch }} -
                        {{ record.location }}
                      </p>

                      <p class="text-neutral-500">
                        เกรดเฉลี่ย {{ record.gpa }} ระยะเวลาการศึกษา
                        {{ record.period }}
                      </p>
                    </div>
                  </li>
                </template>
              </ul>
            </div>
          </div>
        </div>

        <!-- Experience record -->
        <div class="bg-white rounded shadow overflow-auto">
          <div>
            <h2 class="p-4 bg-emerald-700 border-b font-semibold text-white">
              ประสบการณ์การทำงาน
            </h2>
          </div>

          <div class="p-4">
            <ul class="space-y-4">
              <template v-for="record in experienceRecords" :key="record.value">
                <li class="text-xs">
                  <div class="space-y-2">
                    <h3
                      class="flex items-center gap-2 font-semibold text-neutral-700"
                    >
                      <component :is="record.icon" class="w-5 h-5" />

                      {{ record.title }}
                    </h3>

                    <p class="text-neutral-500">
                      {{ record.company }} - {{ record.department }}
                    </p>

                    <p class="text-neutral-500">
                      {{ record.description }}
                    </p>

                    <p class="text-neutral-500">ระยะเวลา {{ record.period }}</p>
                  </div>
                </li>
              </template>
            </ul>
          </div>
        </div>

        <!-- Tools -->
        <div class="grid grid-cols-8 py-8 gap-8">
          <template v-for="tool in toolsUsed" :key="tool.icon">
            <a :href="tool.href" target="_blank">
              <img class="w-12 h-12 text-neutral-700" :src="tool.icon" />
            </a>
          </template>
        </div>
      </div>
    </div>
  </PapgerPage>
</template>
