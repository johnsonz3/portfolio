<template>
  <div>
    <Navbar/>
    <Index/>
    <FooterSection/>
  </div>
</template>

<script>

import Navbar from '../layouts/navbar.vue';
import Index from '../layouts/mainPage.vue';
import FooterSection from '../layouts/FooterSection.vue';
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyDMkDLh1PLvN4wWo4Rv4XKuY15fb7ie5oA",
  authDomain: "jzhang-portfolio.firebaseapp.com",
  projectId: "jzhang-portfolio",
  storageBucket: "jzhang-portfolio.appspot.com",
  messagingSenderId: "400428664856",
  appId: "1:400428664856:web:3e41f69959341762115b6d",
  measurementId: "G-RZ135PVEC2"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);

export default {
  name: 'IndexPage',
  components: {
    Navbar,
    Index,
    FooterSection
  }
}
</script>
