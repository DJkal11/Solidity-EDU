<script>
    import { Link } from "svelte-routing"
    
    </script>
    
    <div class="w-full transition">
        
        <div class="text-center">
            <h1 class="p-5 text-4xl">Our Mission</h1>
            <p class="text-xl p-5 pad">Our mission is to educate people about ethereum and solidity concepts that will help make their learning journey easier.</p>

             <div>
                 <img class="m-auto w-96" src="about.svg" alt="about pic" />
             </div>

            <h3 class="p-5 text-4xl">About</h3>
            <p class="text-xl p-5 pad">This application shares information about solidity to help simplify complex solidity concepts and help you to code better applications 
                and ma ke more secure smart contracts.
            </p>
        </div>
         
    
        
      </div>
    
      <style>
    
    
    
    
        @media (min-width: 800px){
        .pad{
            padding-left: 15rem;
            padding-right: 15rem;
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
      