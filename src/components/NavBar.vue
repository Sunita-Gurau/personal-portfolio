<template>
  <header class="relative h-screen w-full">
    <!-- Background Image Wrapper -->
    <div class="absolute inset-0 w-full h-full">
      <img
        class="w-full h-full object-cover"
        src="https://images.unsplash.com/photo-1441015401724-70d16b783f5c?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="Flower and sky"
      />
      <!-- Black Overlay -->
      <div class="absolute inset-0 bg-black opacity-50"></div>
      <!-- overlay -->
    </div>
    <div
      class="h-screen flex flex-col justify-center items-center absolute top-0 left-0 w-full z-20 text-white text-5xl"
    >
      <div class="text-center">
        Hi there! My name is Sunita Gurau and <br />
        I'm a <span class="text-[#ff88ba]">front-end developer.</span>
      </div>
      <div class="cursor-pointer bg-[#9f305f] rounded-full py-2 px-4 m-6 text-xl">
        <a href="/Sunita_Gurau_CV.pdf" download="Sunita_Gurau_CV" class="inline-block">
          <button class="cursor-pointer">Download the CV</button>
        </a>
      </div>
    </div>
    <!-- Navbar -->
    <nav class="absolute top-0 left-0 w-full z-20">
      <ul
        class="navigation max-w-[90vw] flex flex-wrap justify-end items-center relative mx-auto py-8"
      >
        <input type="checkbox" id="check" />

        <span
          class="menu text-white flex [&>li]:pl-8 [&>li>a]:text-center [&>li>a]:relative [&>li>a]:transition [&>li>a]:duration-200 [&>li>a]:ease-in-out [&>li>a]:font-medium [&>li>a]:text-lg"
        >
          <li><a href="#">About me</a></li>
          <li><a href="#">My skills</a></li>
          <li><a href="#">Portfolio</a></li>
          <li><a href="#">Contacts</a></li>

          <label for="check" class="close-menu">
            <Icon iconName="CloseIcon" svgFill="fill-white" />
          </label>
        </span>

        <label for="check" class="open-menu">
          <Icon iconName="TogglerMenu" />
        </label>
      </ul>
    </nav>
  </header>
</template>

<script setup lang="ts">
import Icon from './Icon.vue'
</script>
<style scoped>
.close-menu,
.open-menu {
  position: absolute;
  cursor: pointer;
  display: none;
}

.open-menu {
  top: 50%;
  right: 20px;
  transform: translateY(-50%);
}

.close-menu {
  top: 20px;
  right: 20px;
}

#check {
  display: none;
}

@media (max-width: 800px) {
  .menu {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 73%;
    height: 100vh;
    position: fixed;
    top: 0;
    right: -100%;
    z-index: 100;
    background-color: #000;
    color: #fff;
    transition: all 0.5s ease-in-out;
    text-transform: uppercase;
    font-size: 24px;
  }

  .menu li {
    margin-top: 40px;
  }

  .menu li a {
    padding: 10px;
  }

  .close-menu,
  .open-menu {
    display: block;
  }

  #check:checked ~ .menu {
    right: 0;
  }
}
</style>
