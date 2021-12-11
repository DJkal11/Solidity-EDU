<script>
  import { Link } from "svelte-routing";
</script>

<div class="transition">
  <div class="p-5 heading-center ipad-center">
    <h3 class="text-2xl mt-2">Featured Topics</h3>

    <div
      class="rounded-3xl mt-5 display-category1 h-72 relative category-ipad category-medium-screen categeory-small-screen"
    >
      <Link to="/Basics"
        ><div class="bg-red-400 category absolute bottom-0 w-full rounded-3xl">
          <h1 class="text-2xl ml-3 p-2 text-white">Basics of solidity</h1>
          <p class="text-lg ml-3 p-2 pt-0 text-white">2 min read</p>
        </div></Link
      >
    </div>

    <div
      class="rounded-3xl mt-5 display-category2 h-72 relative category-ipad category-medium-screen categeory-small-screen"
    >
      <Link to="SmartContracts"
        ><div class="bg-red-400 category absolute bottom-0 w-full rounded-3xl">
          <h1 class="text-2xl ml-3 p-2 text-white">Smart contracts</h1>
          <p class="text-lg ml-3 p-2 pt-0 text-white">2 min read</p>
        </div></Link
      >
    </div>
  </div>
</div>

<style>
  .display-category1 {
    background-image: url("/programming.jpg");
    background-size: cover;
  }

  .display-category2 {
    background-image: url("/tech.jpg");
    background-size: cover;
  }

  .category {
    transition: 0.4s ease-out;
  }

  .category:hover {
    background-color: rgb(255, 38, 0);
  }

  .transition {
    animation-name: fadeInUp;
    animation-duration: 0.25s;
    transition-timing-function: ease-in;
    animation-fill-mode: both;
  }

  @keyframes fadeInUp {
    0% {
      opacity: 0;
      transform: translate3d(0, 100%, 0);
    }

    100% {
      opacity: 1;
      transform: none;
    }
  }

  @media (max-width: 1050px), (min-width: 768px) {
    .ipad-center {
      text-align: center;
    }

    .category-ipad {
      width: 25rem;
      margin: auto;
      margin-top: 2rem;
    }
  }

  @media (max-width: 415px), (min-width: 380px) {
    .category-medium-screen {
      width: 20rem;
    }
  }

  @media (max-width: 320px) {
    .categeory-small-screen {
      width: 15rem;
    }
  }
</style>
