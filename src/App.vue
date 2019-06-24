<template>
  <div>
    <Home />
    <Project />
    <Footer />
  </div>
</template>

<script>
import Home from "./components/home";
import Project from "./components/project";
import Footer from "./components/footer";
export default {
  name: "App",
  components: {
    Home,
    Project,
    Footer
  }
};
</script>
