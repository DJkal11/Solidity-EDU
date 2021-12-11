<script>
  import { Link } from "svelte-routing";
</script>

<div class="w-full grid-desktop transition grid-ipad small-display">
  <div class="p-5 intro-heading text-ipad text-small-display">
    <h3 class="text-3xl mt-2 heading-size">
      Learn about the fundamentals of solidity
    </h3>
    <p class=" mt-7 text-lg">
      If you’re looking to learn Solidity, it is an opportunity that could
      change your life for the better
    </p>
    <Link to="/Category"
      ><button
        class="mt-5 w-28 p-2 rounded-full learn-btn bg-red-400 text-white"
        >Learn</button
      ></Link
    >
  </div>

  <div class="p-5">
    <img
      class="image-desktop img-ipad img-small-display"
      src="studying.svg"
      alt=""
    />
  </div>
</div>

<style>
  .learn-btn {
    transition: 0.4s ease-out;
  }

  .learn-btn:hover {
    background-color: rgb(255, 38, 0);
  }

  @media (min-width: 800px) {
    .grid-desktop {
      display: grid;
      grid-template-columns: 600px auto;
    }

    .intro-heading {
      padding: 100px;
      margin-top: 70px;
    }

    .heading-size {
      font-size: 4rem;
      line-height: 3.5rem;
    }

    .image-desktop {
      width: 40rem;
      margin-top: 40px;
    }
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
    .grid-ipad {
      display: flex;
      flex-direction: row;
    }

    .text-ipad {
      padding: 3rem;
      margin-top: 7rem;
    }

    .img-ipad {
      margin-top: 7rem;
    }
  }

  @media (max-width: 599px) {
    .small-display {
      display: grid;
      grid-template-columns: auto;
    }

    .text-small-display {
      margin-top: 0rem;
    }

    .img-small-display {
      margin-top: 0rem;
    }
  }
</style>
