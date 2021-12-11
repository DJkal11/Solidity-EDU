<script>
  import { Link } from "svelte-routing";
</script>

<div class="transition">
  <div class="flex flex-row space-x-32 link" />

  <div class="center">
    <h1 class="text-4xl font-bold p-5">Solidity</h1>
    <div class="flexing text-left pad w-full">
      <p class="p-5 text-padding text-xl">
        Solidity is statically typed, supports inheritance, libraries and
        complex user-defined types among other features. With Solidity you can
        create contracts for uses such as voting, crowdfunding, blind auctions,
        and multi-signature wallets.
      </p>

      <img
        class="p-5  rounded-full m-auto basic-img"
        src="java.jpg"
        alt="coding"
      />
    </div>

    <div class="flexing text-left pad w-full img-reverse">
      <img class="rounded-full p-5 basic-img" src="basics.jpg" alt="" />
      <p class="p-5 text-padding text-xl">
        When deploying contracts, you should use the latest released version of
        Solidity. Apart from exceptional cases, only the latest version receives
        security fixes. Furthermore, breaking changes as well as new features
        are introduced regularly. We currently use a 0.y.z version number to
        indicate this fast pace of change.
      </p>
    </div>
  </div>
</div>

<style>
  .link > :global(a) {
    text-decoration: none;
  }

  :global(a) {
    text-decoration: none;
  }

  @media (min-width: 900px) {
    .center {
      text-align: center;
      padding-left: 50px;
      padding-right: 50px;
    }

    .pad {
      padding-left: 1rem;
      padding-right: 1rem;
    }

    .flexing {
      display: flex;
      flex-direction: row;
      justify-content: center;
      padding: 1rem;
    }

    .text-padding {
      margin-top: 7rem;
      padding-left: 5rem;
      padding-right: 5rem;
    }

    .basic-img {
      width: 40%;
    }
  }

  @media (max-width: 900px) {
    .img-reverse {
      display: flex;
      flex-direction: column-reverse;
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
