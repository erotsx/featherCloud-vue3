<template>
  <div
    class="sticky top-0 z-30 flex justify-center w-full h-16 transition-all duration-100 border-b bg-opacity-90 backdrop-blur bg-base-100 text-base-content"
  >
    <nav class="w-full navbar">
      <div class="flex flex-1 md:gap-1 lg:gap-2">
        <div class="flex items-center gap-2">
          <a href="/" aria-current="page" aria-label="Homepage" class="px-2 flex-0 btn btn-ghost">
            <div class="inline-flex text-lg transition-all duration-200 font-title text-primary md:text-3xl">
              <span class="normal-case text-base-content">featherCloud</span>
            </div>
          </a>
        </div>
      </div>
      <div class="flex-0">
        <div title="仪表盘" class="gap-1 normal-case btn btn-ghost">
          <a href="/">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="inline-block w-5 h-5 stroke-current md:h-6 md:w-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21 7.5l-9-5.25L3 7.5m18 0l-9 5.25m9-5.25v9l-9 5.25M3 7.5l9 5.25M3 7.5v9l9 5.25m0-9v9"
              />
            </svg>
            <span class="hidden md:inline">仪表盘</span>
          </a>
        </div>
        <div title="文件" class="gap-1 normal-case btn btn-ghost">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="inline-block w-5 h-5 stroke-current md:h-6 md:w-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M2.25 12.75V12A2.25 2.25 0 014.5 9.75h15A2.25 2.25 0 0121.75 12v.75m-8.69-6.44l-2.12-2.12a1.5 1.5 0 00-1.061-.44H4.5A2.25 2.25 0 002.25 6v12a2.25 2.25 0 002.25 2.25h15A2.25 2.25 0 0021.75 18V9a2.25 2.25 0 00-2.25-2.25h-5.379a1.5 1.5 0 01-1.06-.44z"
            />
          </svg>

          <span class="hidden md:inline">文件</span>
        </div>
        <div title="文件" class="gap-1 normal-case btn btn-ghost">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="inline-block w-5 h-5 stroke-current md:h-6 md:w-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M2.25 15.75l5.159-5.159a2.25 2.25 0 013.182 0l5.159 5.159m-1.5-1.5l1.409-1.409a2.25 2.25 0 013.182 0l2.909 2.909m-18 3.75h16.5a1.5 1.5 0 001.5-1.5V6a1.5 1.5 0 00-1.5-1.5H3.75A1.5 1.5 0 002.25 6v12a1.5 1.5 0 001.5 1.5zm10.5-11.25h.008v.008h-.008V8.25zm.375 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z"
            />
          </svg>
          <span class="hidden md:inline">相册</span>
        </div>
        <div title="修改主题" class="dropdown dropdown-end">
          <div tabindex="0" class="gap-1 normal-case btn btn-ghost">
            <svg
              width="20"
              height="20"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              class="inline-block w-5 h-5 stroke-current md:h-6 md:w-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01"
              />
            </svg>
            <span class="hidden md:inline">主题</span>
            <svg
              width="12px"
              height="12px"
              class="hidden w-3 h-3 ml-1 fill-current opacity-60 sm:inline-block"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 2048 2048"
            >
              <path d="M1799 349l242 241-1017 1017L7 590l242-241 775 775 775-775z" />
            </svg>
          </div>
          <div
            class="mt-16 overflow-y-auto shadow-2xl dropdown-content bg-base-200 text-base-content rounded-t-box rounded-b-box top-px w-52"
          >
            <div class="grid grid-cols-1 gap-3 p-3" tabindex="0">
              <div
                class="overflow-hidden rounded-lg outline-base-content outline-2 outline-offset-2 outline"
                data-set-theme="light"
                data-act-class="outline"
                @click="changeTheme('light')"
                ><div data-theme="light" class="w-full font-sans cursor-pointer bg-base-100 text-base-content">
                  <div class="grid grid-cols-5 grid-rows-3">
                    <div class="flex col-span-5 row-span-3 row-start-1 gap-1 px-4 py-3">
                      <div class="flex-grow text-sm font-bold">light</div>
                      <div class="flex flex-wrap flex-shrink-0 gap-1">
                        <div class="w-2 rounded bg-primary"></div> <div class="w-2 rounded bg-secondary"></div>
                        <div class="w-2 rounded bg-accent"></div> <div class="w-2 rounded bg-neutral"></div></div></div
                  ></div>
                </div>
              </div>
              <div
                class="overflow-hidden rounded-lg outline-base-content outline-2 outline-offset-2"
                data-set-theme="dark"
                data-act-class="outline"
                @click="changeTheme('dark')"
                ><div data-theme="dark" class="w-full font-sans cursor-pointer bg-base-100 text-base-content">
                  <div class="grid grid-cols-5 grid-rows-3">
                    <div class="flex col-span-5 row-span-3 row-start-1 gap-1 px-4 py-3">
                      <div class="flex-grow text-sm font-bold">dark</div>
                      <div class="flex flex-wrap flex-shrink-0 gap-1">
                        <div class="w-2 rounded bg-primary"></div> <div class="w-2 rounded bg-secondary"></div>
                        <div class="w-2 rounded bg-accent"></div> <div class="w-2 rounded bg-neutral"></div></div></div></div></div
              ></div>
            </div>
          </div>
        </div>
        <div title="修改语言" class="dropdown dropdown-end">
          <div tabindex="0" class="gap-1 normal-case btn btn-ghost"
            ><svg
              class="inline-block w-4 h-4 fill-current md:h-5 md:w-5"
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 512 512"
            >
              <path d="M363,176,246,464h47.24l24.49-58h90.54l24.49,58H480ZM336.31,362,363,279.85,389.69,362Z" />
              <path
                d="M272,320c-.25-.19-20.59-15.77-45.42-42.67,39.58-53.64,62-114.61,71.15-143.33H352V90H214V48H170V90H32v44H251.25c-9.52,26.95-27.05,69.5-53.79,108.36-32.68-43.44-47.14-75.88-47.33-76.22L143,152l-38,22,6.87,13.86c.89,1.56,17.19,37.9,54.71,86.57.92,1.21,1.85,2.39,2.78,3.57-49.72,56.86-89.15,79.09-89.66,79.47L64,368l23,36,19.3-11.47c2.2-1.67,41.33-24,92-80.78,24.52,26.28,43.22,40.83,44.3,41.67L255,362Z"
              />
            </svg>
            <svg
              width="12px"
              height="12px"
              class="hidden w-3 h-3 ml-1 fill-current opacity-60 sm:inline-block"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 2048 2048"
            >
              <path d="M1799 349l242 241-1017 1017L7 590l242-241 775 775 775-775z" />
            </svg>
          </div>
          <div
            class="w-56 mt-16 overflow-y-auto shadow-2xl dropdown-content bg-base-200 text-base-content rounded-t-box rounded-b-box top-px"
          >
            <ul class="gap-1 p-3 menu menu-compact" tabindex="0">
              <li
                ><button class="flex"
                  ><img
                    loading="lazy"
                    width="20"
                    height="20"
                    alt="English"
                    src="https://cdnjs.cloudflare.com/ajax/libs/twemoji/14.0.0/svg/1f1ec-1f1e7.svg"
                  />
                  <span class="flex justify-between flex-1">English </span></button
                >
              </li>
              <li
                ><button class="flex active"
                  ><img
                    loading="lazy"
                    width="20"
                    height="20"
                    alt="中文"
                    src="https://cdnjs.cloudflare.com/ajax/libs/twemoji/14.0.0/svg/1f1e8-1f1f3.svg"
                  />
                  <span class="flex justify-between flex-1">中文 </span></button
                >
              </li>
            </ul>
          </div>
        </div>
        <div title="个人中心" class="dropdown dropdown-end">
          <label tabindex="0" class="btn btn-ghost btn-circle avatar">
            <div class="w-10 rounded-full">
              <img src="https://placeimg.com/80/80/people" />
            </div>
          </label>
          <div
            class="w-56 mt-16 overflow-y-auto shadow-2xl dropdown-content bg-base-200 text-base-content rounded-t-box rounded-b-box top-px"
          >
            <ul tabindex="0" class="gap-1 p-3 menu menu-compact">
              <li>
                <a class="justify-between">
                  Profile
                  <span class="badge">New</span>
                </a>
              </li>
              <li><a>Settings</a></li>
              <li><a>Logout</a></li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </div>
  <!-- <header class="antialiased bg-white Male text-slate-500 dark:text-slate-400 dark:bg-slate-900">
    <div
      class="sticky top-0 z-40 w-full backdrop-blur flex-none transition-colors duration-500 lg:z-50 lg:border-b lg:border-slate-900/10 dark:border-slate-50/[0.06] bg-white/95 supports-backdrop-blur:bg-white/60 dark:bg-transparent"
    >
      <div class="mx-auto max-w-8xl">
        <div class="px-4 py-4 border-b border-slate-900/10 lg:px-8 lg:border-0 dark:border-slate-300/10">
          <div class="relative flex items-center text-2xl sm:text-2xl font-blimone">
            <router-link to="/" class="mr-3 flex-none w-[2.0625rem] md:w-auto leading-6 dark:text-slate-200">Fast-Vue3</router-link>
            <div class="relative items-center hidden ml-auto lg:flex">
              <nav class="text-sm font-semibold leading-6 text-slate-700 dark:text-slate-200">
                <ul class="flex space-x-8">
                  <li>
                    <router-link to="/demo" class="hover:text-sky-500 dark:hover:text-sky-400">GithubDemo</router-link>
                  </li>
                  <li>
                    <router-link to="/login" class="hover:text-sky-500 dark:hover:text-sky-400">Login</router-link>
                  </li>
                </ul>
              </nav>
              <div class="flex items-center pl-6 ml-6 border-l border-slate-200 dark:border-slate-800">
                <el-tooltip :content="theme === 'light' ? '设置暗黑主题' : '设置明亮主题'">
                  <el-button
                    class="nav-btn"
                    :shape="'circle'"
                    type="info"
                    plain
                    :icon="theme === 'dark' ? Sunny : Moon"
                    circle
                    size="small"
                    @click="toggleTheme()"
                  />
                </el-tooltip>
                <a
                  href="https://github.com/MaleWeb/fast-vue3"
                  target="_bank"
                  class="block ml-6 text-slate-400 hover:text-slate-500 dark:hover:text-slate-300"
                >
                  <SvgIcon name="svg-github" size="small" color="#999999" />
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header> -->
</template>

<script setup lang="ts">
  import { themeChange } from 'theme-change';
  import { onMounted } from 'vue';
  // import SvgIcon from '../SvgIcon/index.vue';
  // import { ref } from 'vue'
  // import { useDark, useToggle } from '@vueuse/core';
  import { useAppStore } from '/@/store';
  // import { Sunny, Moon } from '@element-plus/icons-vue';

  onMounted(() => {
    if (theme) {
      document.documentElement.setAttribute('data-theme', theme.value);
    }
    themeChange(false);
  });
  // const title = ref('I want to study typescript')
  // 检测浏览器系统主题
  // const darkThemeMq = window.matchMedia('(prefers-color-scheme: dark)')
  const appStore = useAppStore();
  // const useStore = useUserStore()
  const theme = computed(() => {
    return appStore.theme;
  });
  // const isDark = useDark({
  //   selector: 'body',
  //   attribute: 'arco-theme',
  //   valueDark: 'dark',
  //   valueLight: 'light',
  //   storageKey: 'arco-theme',
  //   onChanged(dark: boolean) {
  //     appStore.toggleTheme(dark);
  //   },
  // });
  // const toggleTheme = useToggle(isDark);
  const changeTheme = (the: string) => {
    console.log(the);
    appStore.theme = the;
    console.log(appStore.theme);
  };
</script>
<style lang="less">
  .prose {
    color: #334155;
    font-size: 0.875em;
    font-variant-ligatures: none;

    code {
      color: #0f172a;
      font-family: Fira Code VF, ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, Liberation Mono, Courier New, monospace;

      &::before {
        content: '`';
      }

      &::after {
        content: '`';
      }
    }

    &.dark\:prose-dark {
      color: #94a3b8;

      code {
        color: #e2e8f0;
      }
    }
  }
</style>
