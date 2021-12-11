<script>
  import { Link } from "svelte-routing";
</script>

<div class="transition">
  <div class="flex flex-row space-x-32 link" />

  <div class="center">
    <h1 class="text-4xl font-bold p-5">Smart Contracts</h1>
    <p class="p-5 pad">
      Smart contracts work by following simple “if/when…then…” statements that
      are written into code on a blockchain. A network of computers executes the
      actions when predetermined conditions have been met and verified. These
      actions could include releasing funds to the appropriate parties,
      registering a vehicle, sending notifications, or issuing a ticket. The
      blockchain is then updated when the transaction is completed. That means
      the transaction cannot be changed, and only parties who have been granted
      permission can see the results.
    </p>

    <img class="p-5 rounded-3xl m-auto" src="solidity.svg" alt="coding" />
    <p class="p-5 pad">
      Within a smart contract, there can be as many stipulations as needed to
      satisfy the participants that the task will be completed satisfactorily.
      To establish the terms, participants must determine how transactions and
      their data are represented on the blockchain, agree on the
      “if/when...then…” rules that govern those transactions, explore all
      possible exceptions, and define a framework for resolving disputes.
    </p>
  </div>
</div>

<style>
  .link > :global(a) {
    text-decoration: none;
  }

  :global(a) {
    text-decoration: none;
  }

  @media (min-width: 800px) {
    .center {
      text-align: center;
      padding-left: 50px;
      padding-right: 50px;
    }

    .pad {
      padding-left: 10rem;
      padding-right: 10rem;
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
