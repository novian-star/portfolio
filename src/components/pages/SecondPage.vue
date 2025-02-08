<script setup lang="ts">
import LogosNuxtIcon from './../icons/LogosNuxtIcon.vue';
import LogosGoogleSheets from './../icons/LogosGoogleSheets.vue';
import PapgerPage from './../PapgerPage.vue';
import LogosNeonIcon from './../icons/LogosNeonIcon.vue';
import LogosHtml5 from './../icons/LogosHtml5.vue';
import LogosCss3 from './../icons/LogosCss3.vue';
import LogosJavascript from './../icons/LogosJavascript.vue';

const projects = [
  {
    title: 'ระบบบันทึกข้อมูลการแจ้งซ่อม',

    location: 'ผปด.กดส.ฝสบ.น3 - การไฟฟ้าส่วนภูมิภาค เขต 3 (ภาคเหนือ)',

    role: 'พัฒนาเว็บแอปพลิเคชัน',

    period: 'มกราคม 2568 - ปัจจุบัน',

    description:
      'ระบบบันทึกข้อมูลการแจ้งซ่อม สำหรับการบันทึกข้อมูลการแจ้งซ่อมของพนักงานที่รับผิดชอบในการรับซ่อม คอมพิวเตอร์และอุปกรณ์ต่อพ่วง เพื่อนำข้อมูลไปเสนอขขออนนมุติการจัดซื้ออะไหล่',

    tools: [
      {
        label: 'Nuxt (แอปพลิเคชัน)',
        icon: LogosNuxtIcon,
        href: 'https://nuxt.com',
      },
      {
        label: 'Google Sheets (ฐานข้อมูล)',
        icon: LogosGoogleSheets,
        href: 'https://workspace.google.com/products/sheets/',
      },
    ],

    example: {
      href: 'https://pea-repair.vercel.app',

      qrcode: '/pea-repair-qrcode.png',
    },
  },
  {
    title: 'ระบบจัดการข้อมูลการบำรุงรักษา',

    location: 'ผปด.กดส.ฝสบ.น3 - การไฟฟ้าส่วนภูมิภาค เขต 3 (ภาคเหนือ)',

    role: 'พัฒนาเว็บแอปพลิเคชัน',

    period: 'มกราคม 2568 - ปัจจุบัน',

    description:
      'ระบบจัดการข้อมูลการบำรุงรักษา สำหรับบันทึกข้อมูลการบำรุงรักษาทรัพย์สิน คอมพิวเตอร์และอุปกรณ์ต่อพ่วง เพื่อตรวจสอบข้อมูลของทรัพย์สินที่ถูกต้อง และตรงตามเงื่อนไขการบำรุงรักษา',

    tools: [
      {
        label: 'Nuxt (แอปพลิเคชัน)',
        icon: LogosNuxtIcon,
        href: 'https://nuxt.com',
      },
      {
        label: 'Neon Serverless Postgres (ฐานข้อมูล)',
        icon: LogosNeonIcon,
        href: 'https://neon.tech/',
      },
    ],

    example: {
      href: 'https://pea-n3-property.vercel.app',

      qrcode: '/pea-n3-property-qrcode.png',
    },
  },
];

const secondProjectTools = [
  {
    label: 'HTML',
    icon: LogosHtml5,
    href: 'https://developer.mozilla.org/en-US/docs/Web/HTML',
  },
  {
    label: 'CSS',
    icon: LogosCss3,
    href: 'https://developer.mozilla.org/en-US/docs/Web/CSS',
  },
  {
    label: 'JavaScript',
    icon: LogosJavascript,
    href: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript',
  },
];
</script>

<template>
  <PapgerPage>
    <div class="relative grid grid-rows-2 w-full h-full p-8 gap-8 bg-gray-200">
      <!-- Project -->
      <div class="bg-white rounded shadow overflow-hidden">
        <div class="p-4 bg-emerald-700 border-b">
          <h2 class="font-semibold text-white">
            ผลงาน/ชิ้นงาน/โครงการที่โดดเด่นในอดีตหรือปัจจุบัน
            ที่เกี่ยวข้องกับตำแหน่งที่สมัคร
          </h2>
        </div>

        <div class="p-4">
          <div class="grid grid-cols-2 gap-4">
            <template v-for="project in projects">
              <div class="space-y-2 divide-y">
                <div class="pb-2 space-y-1 text-sm">
                  <h3 class="font-semibold">{{ project.title }}</h3>

                  <p class="text-xs text-muted">
                    {{ project.location }}
                  </p>
                </div>

                <div class="space-y-2 text-xs">
                  <div class="space-y-1 leading-5">
                    <p>
                      <span class="font-semibold">บทบาทหน้าที่:</span>

                      {{ project.role }}
                    </p>

                    <p>
                      <span class="font-semibold"> ระยะเวลาที่ทำงาน: </span>
                      {{ project.period }}
                    </p>

                    <p>
                      <span class="font-semibold"> รายละเอียด: </span>

                      {{ project.description }}
                    </p>

                    <div>
                      <span class="font-semibold"> เทคโนโลยีที่ใช้: </span>

                      <ul class="space-y-1">
                        <template v-for="tool in project.tools">
                          <li>
                            <a
                              class="flex items-center gap-1"
                              :href="tool.href"
                              target="_blank"
                            >
                              <component :is="tool.icon" class="w-6 h-6" />

                              <span class="text-xs">{{ tool.label }}</span>
                            </a>
                          </li>
                        </template>
                      </ul>
                    </div>

                    <div class="space-y-2">
                      <p>
                        <span class="font-semibold"> ตัวอย่าง: </span>
                        <a
                          class="text-primary underline"
                          :href="project.example.href"
                          target="_blank"
                        >
                          {{ project.example.href }}
                        </a>
                      </p>

                      <img
                        class="w-24 h-24"
                        :src="project.example.qrcode"
                        alt="QR Code"
                      />
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>

      <!-- Project -->
      <div class="bg-white rounded shadow overflow-hidden">
        <div class="p-4 bg-emerald-700 border-b">
          <h2 class="font-semibold text-white">ผลงานโครงการที่โดดเด่น</h2>
        </div>

        <div class="p-4 space-y-2 divide-y text-sm leading-5">
          <div class="pb-2 space-y-1">
            <h3 class="font-semibold">เว็บแอปพลิเคชันออกแบบลวดลายพัดสาน</h3>

            <p class="text-xs text-muted leading-5">
              แอปพลิเคชันสำหรับการออกแบบลวดลายพัดสาน
              ที่พัฒนาขึ้นเพื่อเพิ่มความง่ายในการสานพัดตามลวดลายที่ต้องการ
              โดยการแสดงขั้นตอนการสานพัดให้ได้ลวดลายนั้น ๆ
              เหมาะสำหรับผู้ใช้งานฝึกหัด หรือผู้ชำนาญการสานพัดแล้ว
            </p>
          </div>

          <div class="space-y-1 text-xs leading-5">
            <div>
              <span class="font-semibold">บทบาทหน้าที่:</span>

              พัฒนาเว็บแอปพลิเคชัน
            </div>

            <div class="space-y-1">
              <span class="block font-semibold"> เทคโนโลยีที่ใช้: </span>

              <ul class="space-y-1">
                <template v-for="tool in secondProjectTools">
                  <li>
                    <a
                      class="flex items-center gap-1"
                      :href="tool.href"
                      target="_blank"
                    >
                      <component :is="tool.icon" class="w-6 h-6" />

                      <span class="text-xs">{{ tool.label }}</span>
                    </a>
                  </li>
                </template>
              </ul>
            </div>

            <div>
              <span class="font-semibold">ผลลัพธ์:</span>

              ผู้ใช้งานในชุมชนสานพัดสามารถสานพัดตามลวดลายที่ต้องการได้ง่ายขึ้น
            </div>

            <div class="space-y-2">
              <p>
                <span class="font-semibold"> ตัวอย่าง: </span>
                <a
                  class="text-primary underline"
                  href="https://weaving.thepsatri.com"
                  target="_blank"
                >
                  https://pea-weaving.vercel.app
                </a>
              </p>

              <img class="w-24 h-24" src="/weave-qrcode.png" alt="QR Code" />
            </div>
          </div>
        </div>
      </div>

      <footer class="absolute bottom-0 w-full p-2 text-xs">
        <p class="text-center">
          เอกสารนี้จัดทำขึ้นโดยใช้ Vue 3 สามารถดูรายละเอียดได้ที่
          <a
            class="underline"
            href="https://github.com/novian-star/portfolio"
            target="_blank"
          >
            https://github.com/novian-star/portfolio
          </a>
        </p>
      </footer>
    </div>
  </PapgerPage>
</template>
