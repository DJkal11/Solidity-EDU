<script>
  import { Router, Link, Route } from "svelte-routing";
  import Intro from "./intro.svelte";
  import Category from "./category.svelte";
  import Basics from "./pages/basics.svelte";
  import BasicsFull from "./fullPages/basics-full.svelte";
  import SmartContracts from "./pages/smartContracts.svelte";
  import SmartContractsFull from "./fullPages/smartContracts-full.svelte";
  import About from "./About.svelte";
  import GiCube from "svelte-icons/gi/GiCube.svelte";
</script>

<main class="w-screen h-full background">
  <Router>
    <nav class="bg-white">
      <ul class="flex flex-row  flex-space border-2">
        <li class="link ">
          <Link to="/"
            ><div class="flex flex-row ml-5 p-2 cube logo">
              <div class="icon">
                <GiCube />
              </div>
              <h1 class="text-3xl ml-2 logo-small-mobile">Solidity</h1>
            </div></Link
          >
        </li>
        <div class="link ">
          <Link to="/Category"
            ><li class="text-2xl p-3 nav-mobile nav-item-small-device">
              Content
            </li></Link
          >
        </div>
        <div class="link">
          <Link to="/About"
            ><li class="text-2xl p-3 nav-mobile nav-item-small-device">
              About
            </li></Link
          >
        </div>
      </ul>
    </nav>

    <Route path="/" component={Intro} />
    <Route path="/Category" component={Category} />
    <Route path="/Basics" component={Basics} />
    <Route path="/BasicsFull" component={BasicsFull} />
    <Route path="/SmartContracts" component={SmartContracts} />
    <Route path="/SmartContractsFull" component={SmartContractsFull} />
    <Route path="/About" component={About} />
  </Router>
</main>

<style lang="postcss" global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  @import url("https://fonts.googleapis.com/css2?family=Raleway:wght@500&display=swap");

  main {
    font-family: "Raleway", sans-serif;
  }

  .logo {
    transition: 0.4s ease-out;
  }

  .logo:hover {
    color: tomato;
  }

  li {
    transition: 0.4s ease-out;
  }

  li:hover {
    color: tomato;
  }

  .link > :global(a) {
    text-decoration: none;
    color: black;
  }

  :global(a) {
    text-decoration: none;
  }

  .background {
    background-image: url("/Meteor-white.svg");
    background-size: auto;
    background-repeat: repeat;
  }

  .icon {
    width: 2.5rem;
  }

  @media (min-width: 800px) {
    .flex-space {
      gap: 40px;
    }
  }

  @media (max-width: 600px) {
    .nav-mobile {
      font-size: 1rem;
    }

    .flex-space {
      gap: 0px;
    }
  }

  @media (max-width: 380px) {
    .logo-small-mobile {
      font-size: 1.2rem;
    }
    .cube {
      margin-left: 2px;
    }
  }

  @media (max-width: 320px) {
    .nav-item-small-device {
      font-size: 0.8rem;
    }
  }
</style>
