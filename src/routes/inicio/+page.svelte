<script lang="ts">
    // import Shopping from "../../components/shopping.cart.svelte";
    
    let valueNull = ''

    const handleOpenMenu = () => {
        let menuContent = document.querySelector(".menu")

        menuContent?.classList.toggle("hidden")
        // console.log("open menu burguer")
    }

    const handleSuggestions = () => {
        console.log("listening onclick event!")
        // alert("hello world")
    }

    const handleSearch = (event:any) => {
        const data = event.target.value
        console.log(data)

        window.alert(data)
    }

</script>
<div class="min-h-screen bg-gray-50 pb-10">
    <!-- Navigation -->
    <div class="mx-auto">
      <!-- mobile navigation -->
      <div class="flex items-center justify-between bg-white px-4 py-6">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="h-6 w-6 text-gray-600"
        on:click={handleOpenMenu}
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <div class="flex items-center">
          <img class="ml-6 h-9 w-9 rounded-full object-cover" src="https://th.bing.com/th/id/R.35161660261a07e85fbe992640402ee5?rik=LNTU1CFpFCmdTw&pid=ImgRaw&r=0" alt="profile" />
        </div>
      </div>
      <nav class="hidden menu">
        <a href="">
          <img src="" alt="" />
          Nuegas
        </a>
        <ul>
          <li>
            <a href="">
              <img src="" alt="" />
              Nuegas
            </a>
          </li>
          <li>
            <a href="">
              <img src="" alt="" />
              Nuegas
            </a>
          </li>
          <li>
            <a href="">
              <img src="" alt="" />
              Nuegas
            </a>
          </li>
          <li>
            <a href="">
              <img src="" alt="" />
              Nuegas
            </a>
          </li>
          <li>
            <a href="">
              <img src="" alt="" />
              Nuegas
            </a>
          </li>
        </ul>
      </nav>
      <!-- End -->


      <!-- Main -->
      <main class="">
        <div class="bg-white px-4">
          <div>
            <h2 class="text-2xl font-semibold text-gray-900">Explora el menú</h2>
            <div class="flex items-center justify-between">
              <div class="my-6 mr-4 flex w-full items-center justify-between rounded-lg border px-3 py-3 sm:w-[350px] sm:flex-initial">
                <input 
                class="w-full text-sm outline-none" 
                type="text" 
                placeholder="Buscar..."
                bind:value={valueNull}
                on:change={handleSearch}
                />
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="h-5 w-6 text-gray-400">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
                </svg>
              </div>
              <div>
                <div class="flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="h-6 w-6 text-gray-500" 
                    on:click={handleSuggestions}
                  >
                    <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6A2.25 2.25 0 016 3.75h2.25A2.25 2.25 0 0110.5 6v2.25a2.25 2.25 0 01-2.25 2.25H6a2.25 2.25 0 01-2.25-2.25V6zM3.75 15.75A2.25 2.25 0 016 13.5h2.25a2.25 2.25 0 012.25 2.25V18a2.25 2.25 0 01-2.25 2.25H6A2.25 2.25 0 013.75 18v-2.25zM13.5 6a2.25 2.25 0 012.25-2.25H18A2.25 2.25 0 0120.25 6v2.25A2.25 2.25 0 0118 10.5h-2.25a2.25 2.25 0 01-2.25-2.25V6zM13.5 15.75a2.25 2.25 0 012.25-2.25H18a2.25 2.25 0 012.25 2.25V18A2.25 2.25 0 0118 20.25h-2.25A2.25 2.25 0 0113.5 18v-2.25z" />
                  </svg>
                  <span class="hidden sm:block">Surgerencias de la AI</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="px-4">
          <div class="my-5 flex items-center justify-between">
            <h2 class="text-lg font-semibold text-gray-900">Mejor calificados</h2>

            <!-- container buttons next and previous page -->
            <div class="flex">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 h-5 w-5 text-gray-500"
              >
                <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="h-5 w-5 text-gray-900">
                <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
              </svg>
            </div>
            <!-- close container buttons -->

          </div>
          <div class="mb-6 sm:w-1/2 rounded-lg bg-white p-6">
            <div class="flex items-center justify-between">
              <div class="flex items-center">
                <img class="mr-2 h-10 w-10 rounded-full object-cover" src="https://th.bing.com/th/id/R.84d84462dd556d362a5902e1cd7c2f07?rik=Zd5vFPFPJ2uFKg&pid=ImgRaw&r=0" alt="product" />
                <div>
                  <h3 class="text-base font-semibold text-gray-900">Café en las rocas</h3>
                  <span class="block text-xs font-normal text-gray-500"></span>
                </div>
              </div>
            
              <!-- button show product here -->
              <a
                class="inline-block rounded-full border border-indigo-600 bg-indigo-600 p-3 text-white hover:bg-transparent hover:text-indigo-600 focus:outline-none focus:ring active:text-indigo-500"
                href="/inicio/shopping"
                >
                <svg
                    class="h-5 w-5 rtl:rotate-180"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                >
                    <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M14 5l7 7m0 0l-7 7m7-7H3"
                    />
                </svg>
            </a>
            </div>
             <!-- close best awards products -->

            <div class="mt-6 flex items-center justify-between text-sm font-semibold text-gray-900">
                <div class="flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-1 h-5 w-6 text-yellow-500">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z" />
                </svg>
                4,7 (750 Reviews)
              </div>
            </div>
          </div>
        </div>

        <!-- others products here -->
        <div class="px-4">
          <div class="my-5">
            <h2 class="text-lg font-semibold text-gray-900">Otros</h2>
          </div>
          <div class="grid sm:grid-cols-2 sm:gap-x-6 lg:grid-cols-3">
            <div class="mb-6 rounded-lg bg-white p-6">
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                <img class="mr-2 h-10 w-10 rounded-full object-cover" src="https://th.bing.com/th/id/R.84d84462dd556d362a5902e1cd7c2f07?rik=Zd5vFPFPJ2uFKg&pid=ImgRaw&r=0" alt="product" />
                  <div>
                    <h3 class="text-base font-semibold text-gray-900">Frappe Oreo</h3>
                  </div>
                </div>
                <!-- button show product here -->
              <button
              class="inline-block rounded-full border border-indigo-600 bg-indigo-600 p-3 text-white hover:bg-transparent hover:text-indigo-600 focus:outline-none focus:ring active:text-indigo-500"
              on:click={()=> console.log("listening click")}
              >
              <svg
                  class="h-5 w-5 rtl:rotate-180"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
              >
                  <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M14 5l7 7m0 0l-7 7m7-7H3"
                  />
              </svg>
          </button>
              </div>
              <p class="my-6 text-sm font-normal text-gray-500">
                El frappé de Oreo es una bebida helada que combina la intensidad del chocolate, la textura de las galletas Oreo y la suavidad de la crema batida. ¡Perfecto para refrescarte! 🍪🥤
              </p>
              <div class="mt-6 flex items-center justify-between text-sm font-semibold text-gray-900">
                <div class="flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-1 h-5 w-6 text-yellow-500">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z" />
                  </svg>
                  4,7 (750 Reviews)
                </div>
              </div>
            </div>
            <div class="mb-6 rounded-lg bg-white p-6">
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <img class="mr-2 h-10 w-10 rounded-full object-cover" src="https://th.bing.com/th/id/R.84d84462dd556d362a5902e1cd7c2f07?rik=Zd5vFPFPJ2uFKg&pid=ImgRaw&r=0" alt="product" />
                  <div>
                    <h3 class="text-base font-semibold text-gray-900">Mocca</h3>
                    <!-- <span class="block text-xs font-normal text-gray-500">Android Developer</span> -->
                  </div>
                </div>
                <!-- button show product here -->
                <button
                class="inline-block rounded-full border border-indigo-600 bg-indigo-600 p-3 text-white hover:bg-transparent hover:text-indigo-600 focus:outline-none focus:ring active:text-indigo-500"
                on:click={()=> console.log("listening click")}
                >
                <svg
                    class="h-5 w-5 rtl:rotate-180"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                >
                    <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M14 5l7 7m0 0l-7 7m7-7H3"
                    />
                </svg>
            </button>

            </div>
              <p class="my-6 text-sm font-normal text-gray-500">
                Es para esos momentos en los que necesitas un capricho indulgente, cuando el mundo se mueve demasiado rápido y tú solo quieres detenerte un instante. Así que, ¿por qué no te sumerges en esta maravilla de sabor? 🍫☕
              </p>
              <div class="mt-6 flex items-center justify-between text-sm font-semibold text-gray-900">
                <div class="flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-1 h-5 w-6 text-yellow-500">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z" />
                  </svg>
                  4,7 (750 Reviews)
                </div>
              </div>
            </div>
            
                      <div class="mb-6 rounded-lg bg-white p-6">
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <img class="mr-2 h-10 w-10 rounded-full object-cover" src="https://th.bing.com/th/id/R.84d84462dd556d362a5902e1cd7c2f07?rik=Zd5vFPFPJ2uFKg&pid=ImgRaw&r=0" alt="product" />
                  <div>
                    <h3 class="text-base font-semibold text-gray-900">Descafeinado</h3>
                    <!-- <span class="block text-xs font-normal text-gray-500">Android Developer</span> -->
                  </div>
                </div>
                <!-- button show product here -->
                <button
                class="inline-block rounded-full border border-indigo-600 bg-indigo-600 p-3 text-white hover:bg-transparent hover:text-indigo-600 focus:outline-none focus:ring active:text-indigo-500"
                on:click={()=> console.log("listening click")}
                >
                <svg
                    class="h-5 w-5 rtl:rotate-180"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                >
                    <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M14 5l7 7m0 0l-7 7m7-7H3"
                    />
                </svg>
            </button>

            </div>
              <p class="my-6 text-sm font-normal text-gray-500">
                Es para esos momentos en los que necesitas un capricho indulgente, cuando el mundo se mueve demasiado rápido y tú solo quieres detenerte un instante. Así que, ¿por qué no te sumerges en esta maravilla de sabor? 🍫☕
              </p>
              <div class="mt-6 flex items-center justify-between text-sm font-semibold text-gray-900">
                <div class="flex items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-1 h-5 w-6 text-yellow-500">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z" />
                  </svg>
                  4,7 (750 Reviews)
                </div>
              </div>
            </div>
            
          </div>
        </div>
      </main>
    </div>
  </div>