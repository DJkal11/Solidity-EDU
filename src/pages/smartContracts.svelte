<script>
  import { Link } from "svelte-routing";
</script>

<div class="w-full transition">
  <div class="display-topic w-full h-96 text-center">
    <div class="p-5 text-white link">
      <h1 class="text-5xl mt-20">The fundamentals of smart contracts</h1>
    </div>
  </div>

  <div>
    <h1 class="text-4xl font-bold p-5">Description</h1>
    <p class="text-lg p-5 text-gray-600">
      Smart contracts are simply programs stored on a blockchain that run when
      predetermined conditions are met. They typically are used to automate the
      execution of an agreement so that all participants can be immediately
      certain of the outcome.
    </p>
  </div>

  <div class="m-auto text-center button-position">
    <Link to="/SmartContractsFull"
      ><button
        class="w-28 bg-red-400 read-btn text-white p-2 rounded-full m-auto"
        >Read more</button
      ></Link
    >
  </div>
</div>

<style>
  .display-topic {
    background-image: url("/matrix.jpg");
    background-size: cover;
    border-bottom-right-radius: 25%;
    border-bottom-left-radius: 25%;
  }

  .link > :global(a) {
    text-decoration: none;
  }

  :global(a) {
    text-decoration: none;
  }

  .read-btn {
    transition: 0.4s ease-out;
  }

  .read-btn:hover {
    background-color: rgb(255, 38, 0);
  }

  @media (min-width: 800px) {
    .button-position {
      text-align: left;
      margin-left: 17px;
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
</style>
