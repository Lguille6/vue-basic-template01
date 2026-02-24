<template>
  <nav class="flex justify-center gap-4">
    <RouterLink
      to="/"
      class="[&.router-link-active]underline hover:underline hover:underline-offset-4 [&.router-link-active]:underline-offset-4"
    >
      Home
    </RouterLink>
    <RouterLink
      to="/other"
      class="[&.router-link-active]underline hover:underline hover:underline-offset-4 [&.router-link-active]:underline-offset-4"
    >
      Other
    </RouterLink>
  </nav>
</template>
