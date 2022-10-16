<template>
  <div
    class="sticky top-0 z-30 flex justify-center w-full h-16 transition-all duration-100 bg-opacity-90 backdrop-blur bg-base-100 text-base-content"
  >
    <nav class="w-full navbar">
      <div class="flex flex-1 md:gap-1 lg:gap-2">
        <div class="flex items-center gap-2">
          <a class="px-2 flex-0 btn btn-ghost">
            <div class="inline-flex text-lg transition-all duration-200 font-title text-primary md:text-3xl">
              <span class="normal-case text-base-content">featherCloud</span>
            </div>
          </a>
        </div>
      </div>
      <div class="flex-0">
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
      </div>
    </nav>
  </div>
  <div class="flex items-center justify-center min-h-full px-4 py-12 sm:px-6 lg:px-8">
    <div class="w-full max-w-md space-y-8">
      <div class="w-full shadow-2xl card bg-base-100">
        <div class="card-body">
          <div>
            <img class="w-auto h-12 mx-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" alt="Your Company" />
            <h2 class="mt-6 text-3xl font-bold tracking-tight text-center text-gray-900">登录</h2>
            <div class="form-control">
              <label class="label">
                <span class="label-text">账号</span>
              </label>
              <input type="text" placeholder="账号" class="border border-gray-300 input input-primary" />
            </div>
            <div class="form-control">
              <label class="label">
                <span class="label-text" type="password">密码</span>
              </label>
              <input type="password" placeholder="密码" class="border border-gray-300 input input-primary" />
            </div>
            <div class="flex items-center justify-between mt-6">
              <div class="flex items-center">
                <input
                  id="remember-me"
                  name="remember-me"
                  type="checkbox"
                  class="w-4 h-4 text-indigo-600 border border-gray-400 rounded checkbox focus:ring-indigo-500"
                />
                <label for="remember-me" class="block ml-2 text-sm text-gray-900">记住我</label>
              </div>
              <div class="text-sm">
                <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">忘记密码?</a>
              </div>
            </div>
            <div class="mt-6 form-control">
              <button class="btn btn-primary">Login</button>
            </div>
          </div>
        </div>
      </div>
      <!-- <form class="mt-8 space-y-6" action="#" method="POST">
        <input type="hidden" name="remember" value="true" />
        <div class="-space-y-px rounded-md shadow-sm">
          <div>
            <label for="email-address" class="sr-only">Email address</label>
            <input
              id="email-address"
              name="email"
              type="email"
              autocomplete="email"
              required=""
              class="relative block w-full px-3 py-2 text-gray-900 placeholder-gray-500 border border-gray-300 rounded-none appearance-none rounded-t-md focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm"
              placeholder="Email address"
            />
          </div>
          <div>
            <label for="password" class="sr-only">Password</label>
            <input
              id="password"
              name="password"
              type="password"
              autocomplete="current-password"
              required=""
              class="relative block w-full px-3 py-2 text-gray-900 placeholder-gray-500 border border-gray-300 rounded-none appearance-none rounded-b-md focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm"
              placeholder="Password"
            />
          </div>
        </div>

        <div class="flex items-center justify-between">
          <div class="flex items-center">
            <input
              id="remember-me"
              name="remember-me"
              type="checkbox"
              class="w-4 h-4 text-indigo-600 border-gray-300 rounded focus:ring-indigo-500"
            />
            <label for="remember-me" class="block ml-2 text-sm text-gray-900">Remember me</label>
          </div>

          <div class="text-sm">
            <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">Forgot your password?</a>
          </div>
        </div>

        <div>
          <button
            type="submit"
            class="relative flex justify-center w-full px-4 py-2 text-sm font-medium text-white bg-indigo-600 border border-transparent rounded-md group hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
          >
            <span class="absolute inset-y-0 left-0 flex items-center pl-3">
              <LockClosedIcon class="w-5 h-5 text-indigo-500 group-hover:text-indigo-400" aria-hidden="true" />
            </span>
            Sign in
          </button>
        </div>
      </form> -->
    </div>
  </div>

  <!-- <div class="container"> -->
  <!-- <div class="logo">
      <img :src="logo" width="240" />
    </div>
    <LoginBanner />
    <div class="content">
      <div class="content-inner">
        <LoginForm />
      </div>
      <div class="footer">
        <Footer />
      </div>
    </div> -->
  <!-- </div> -->
</template>

<script setup lang="ts">
  // import Footer from '/@/components/Footer/index.vue';
  // import LoginBanner from './components/banner.vue';
  // import LoginForm from './components/login-form.vue';
  // import logo from '/@/assets/icons/svg/logo.svg';
  import { useAppStore } from '/@/store';

  const theme = localStorage.getItem('theme');

  const appStore = useAppStore();

  if (theme == 'dark') {
    document.documentElement.classList.add('dark');
    document.body.setAttribute('arco-theme', 'dark');
  } else {
    document.documentElement.classList.remove('dark');
    document.body.removeAttribute('arco-theme');
  }
  const changeTheme = (the: string) => {
    console.log(the);
    appStore.theme = the;
    console.log(appStore.theme);
  };
</script>

<style lang="less" scoped>
  .container {
    display: flex;
    height: 100vh;

    .banner {
      width: 550px;
      background: linear-gradient(163.85deg, #1d2129 0%, #00308f 100%);
    }

    .content {
      position: relative;
      display: flex;
      flex: 1;
      align-items: center;
      justify-content: center;
      padding-bottom: 40px;
    }

    .footer {
      position: absolute;
      right: 0;
      bottom: 0;
      width: 100%;
    }
  }

  .logo {
    position: fixed;
    top: 24px;
    left: 22px;
    z-index: 1;
    display: inline-flex;
    align-items: center;

    &-text {
      margin-right: 4px;
      margin-left: 4px;
      color: var(--color-fill-1);
      font-size: 20px;
    }
  }
</style>
