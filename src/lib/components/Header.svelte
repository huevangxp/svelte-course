<script lang="ts">

import {LogOut } from 'lucide-svelte';
  let isOpen = $state(false);
  
</script>

<!-- Top Navbar -->
<nav class="fixed top-0 left-0 w-full bg-gray-800 text-white px-4 py-3 flex items-center justify-between z-50 shadow-md">
  <div class="text-lg font-bold">My App</div>
  <!-- Desktop Nav Links -->
  <div class="hidden md:flex space-x-6 align-baseline">

    <!-- add icon -->
     <div class="text-lg font-bold">
      V 1.1.0
     </div>
    <LogOut size={20} />
     
  <!-- Hamburger (Mobile only) -->
 
</nav>

<!-- Slide-in Sidebar (Mobile only) -->
<div
  class="fixed top-0 left-0 h-full w-64 bg-gray-700 text-white transform transition-transform duration-300 z-40 p-6 space-y-4 shadow-lg md:hidden"
  class:translate-x-0={isOpen}
  class:-translate-x-full={!isOpen}
>
  <div class="text-xl font-bold mb-4">Menu</div>
  <a href="/" class="block hover:underline" onclick={() => isOpen = false}>Home</a>
  <a href="/about" class="block hover:underline" onclick={() => isOpen = false}>About</a>
  <a href="/user" class="block hover:underline" onclick={() => isOpen = false}>User</a>
  <a href="/product" class="block hover:underline" onclick={() => isOpen = false}>Product</a>
</div>