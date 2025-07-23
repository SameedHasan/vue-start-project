<script setup>
import Navbar from '@/components/Navbar.vue';
import { RouterView } from 'vue-router';
import Hero from './components/Hero.vue';
import HomeCards from './components/HomeCards.vue';
import JobListings from './components/JobListings.vue';
</script>
<template>
   <Navbar />
   <Hero title="Test Title" subtitle="Find the Vue job that fits your skills and needs"/>
   <HomeCards/>
   <JobListings :limit="3" :showButton="true"/>
</template>