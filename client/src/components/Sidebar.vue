<template>
    <!-- give the sidebar z-50 class so its higher than the navbar if you want to see the logo -->
    <!-- you will need to add a little "X" button next to the logo in order to close it though -->
    <div class="w-1/2 md:w-1/3 lg:w-64 fixed md:top-0 md:left-0 h-screen lg:block bg-gray-100 border-r z-30" :class="sideBarOpen ? '' : 'hidden'" id="main-nav">

          <div class="w-full h-20 border-b flex px-4 items-center mb-8">
            <a href="/dashboard" class="tracking-widest font-normal text-2xl text-mikyored pl-4 hover:text-red-900">Dashboard</a>
          </div>

          <div class="mb-4 px-4">
            <p class="pl-4 text-sm font-semibold mb-1">Main</p>
            <div class="w-full flex items-center text-mikyored h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer">
              <svg class="h-6 w-6 fill-current mr-2" viewBox="0 0 20 20">
                <path d="M18.121,9.88l-7.832-7.836c-0.155-0.158-0.428-0.155-0.584,0L1.842,9.913c-0.262,0.263-0.073,0.705,0.292,0.705h2.069v7.042c0,0.227,0.187,0.414,0.414,0.414h3.725c0.228,0,0.414-0.188,0.414-0.414v-3.313h2.483v3.313c0,0.227,0.187,0.414,0.413,0.414h3.726c0.229,0,0.414-0.188,0.414-0.414v-7.042h2.068h0.004C18.331,10.617,18.389,10.146,18.121,9.88 M14.963,17.245h-2.896v-3.313c0-0.229-0.186-0.415-0.414-0.415H8.342c-0.228,0-0.414,0.187-0.414,0.415v3.313H5.032v-6.628h9.931V17.245z M3.133,9.79l6.864-6.868l6.867,6.868H3.133z"></path>
              </svg>
              <a href="/dashboard" class="text-gray-700">Dashboard</a>
            </div>
            <div class="w-full flex items-center text-mikyored h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer">
              <svg class="h-6 w-6 fill-current mr-2" viewBox="0 0 20 20">
                <path d="M17.431,2.156h-3.715c-0.228,0-0.413,0.186-0.413,0.413v6.973h-2.89V6.687c0-0.229-0.186-0.413-0.413-0.413H6.285c-0.228,0-0.413,0.184-0.413,0.413v6.388H2.569c-0.227,0-0.413,0.187-0.413,0.413v3.942c0,0.228,0.186,0.413,0.413,0.413h14.862c0.228,0,0.413-0.186,0.413-0.413V2.569C17.844,2.342,17.658,2.156,17.431,2.156 M5.872,17.019h-2.89v-3.117h2.89V17.019zM9.587,17.019h-2.89V7.1h2.89V17.019z M13.303,17.019h-2.89v-6.651h2.89V17.019z M17.019,17.019h-2.891V2.982h2.891V17.019z"></path>
              </svg>
              <a href="/profile" class="text-gray-700">Account</a>
            </div>
          </div>

          <div class="mb-4 px-4">
            <p class="pl-4 text-sm font-semibold mb-1">Widgets</p>
            <div class="w-full flex items-center text-mikyored h-10 pl-4 hover:bg-gray-200 rounded-lg cursor-pointer">
              <svg class="h-6 w-6 fill-current mr-2" viewBox="0 0 20 20">
              <path d="M14.613,10c0,0.23-0.188,0.419-0.419,0.419H10.42v3.774c0,0.23-0.189,0.42-0.42,0.42s-0.419-0.189-0.419-0.42v-3.774H5.806c-0.23,0-0.419-0.189-0.419-0.419s0.189-0.419,0.419-0.419h3.775V5.806c0-0.23,0.189-0.419,0.419-0.419s0.42,0.189,0.42,0.419v3.775h3.774C14.425,9.581,14.613,9.77,14.613,10 M17.969,10c0,4.401-3.567,7.969-7.969,7.969c-4.402,0-7.969-3.567-7.969-7.969c0-4.402,3.567-7.969,7.969-7.969C14.401,2.031,17.969,5.598,17.969,10 M17.13,10c0-3.932-3.198-7.13-7.13-7.13S2.87,6.068,2.87,10c0,3.933,3.198,7.13,7.13,7.13S17.13,13.933,17.13,10"></path>
              </svg>
              <a href="/widgets" class="text-gray-700">Add Widget</a>
            </div>
          </div>
        </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
    name: 'Sidebar',
    computed: {
        ...mapState(['sideBarOpen'])
    }
}
</script>