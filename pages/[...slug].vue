<template>
  <main>
    <ContentNavigation v-slot="{ navigation }">
      <nav>
        <TheNav :navigation="navigation"/>
      </nav>
    </ContentNavigation>
    <ContentDoc />
    <NuxtLink v-if="$route.path !== '/'" to="/">Back to home</NuxtLink>
  </main>
</template>
