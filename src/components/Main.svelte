<script>
    import Step from "./Step.svelte";

    let steps = [
        {name:"Smoljames Store", icon:"fa-solid fa-cart-shopping", url: ""},
        {name: "Ultimate Todos", icon:"fa-solid fa-list-check", url: "https://planit-right.vercel.app/"},
        {name:"Social Media", icon:"fa-solid fa-diagram-project", url: "https://github.com/Osalira/ChillWave"},
    ];

    let benefits = [
        {name:'a software engineering Student', 
        description:'I taught myself to code using free online resources and absolutely fell in love with the' +  
        'creativity and problem solving that is involved in developing and engineering innovative new softwares' +
         ". That's why i decided to study Software Engineering.",
        },
        {name:'a learning enthusiast',
         description: 'Starting off with HTML & CSS, JavaScript and evolving my knowledge base to include JavaScript' + 
         'frameworks, backend programming, design, cloud services and much much more.',
        },
        {name:'an excellent communicator', 
        description: "Communication is key and it's a paramount value of mine. I believe in transparency"+
        "and constructive communication above all else. This helps me develop deep relationships and" +
         "ensures my effectiveness and productivity in any work space with any team.",
        },
    ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8
        lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Benjamin</span> Osalira
        <br />
        Full Stack
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite tech</span> includes JavaScript
        , React.js/Next.js, PostgreSQL, MongoDB, Node.js + Express.js & java, python3 !
      </p>
      <!-- svelte-ignore a11y-missing-attribute -->
      <a
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative
            overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950
            cursor-pointer"
        href="https://www.linkedin.com/in/benjamin-osalira-2012162b0/"
        target="_blank"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20
        goup-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <!-- svelte-ignore a11y-img-redundant-alt -->
      <img
        src={"images/profile6.png"}
        alt="Logo image"
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="felx flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        <!-- Curious to <span class="poppins text-violet-400">see</span> my work? -->
      </h3>
    </div>
    <!-- <a
      href="https://www.npmjs.com/"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white
        flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play" />
      <p>Wacth the videos</p>
    </a> -->
    <!-- "lg:grid-cols-3" is the class that's needed to have three projects side by side -->
    <div class="grid grid-cols-1 lg:grid-cols gap-12 lg:gap-10">
      <!-- <Step step={steps[0]}>
        <p>
          Smoljames stor is a merchandising store created innerWidth
          <strong class="text-violet-400"
            >Next.js Commerce.js Stripe & Node.js + Express.js!</strong
          > Commerce.js is a product CMS and Stripe is used for all transaction handling.
        </p>
      </Step> -->
      <Step step={steps[1]} url={steps[1].url}>
        <p>
          PlanItRight is a Full Stack
          <strong class="text-violet-400"
            >Node.js + Express.js, EJS, MongoDB, JavaScript, CSS, and HTML!</strong
          > featuring robust user authentication using Passport for Local OAuth and Google OAuth. 
            It offers an intuitive interface for users to manage tasks efficiently, ensuring data 
           persistence and real-time interaction. 
        </p>
      </Step>
      <Step step={steps[2]} url={steps[2].url}>
        <p>
          ChillWave is a <strong class="text-violet-400"
            >React & Bootstrap</strong
          >
          web application that allows users to
          <strong class="text-violet-400">Connect</strong> with people who share the 
          same interests in the
          <strong class="text-violet-400">Same City.</strong> Built with
          <strong class="text-violet-400"
            >React, Bootstrap, Css, HTML5, JavaScript and MongoDB</strong
          > •	Users can post and comment on the posts of other users.
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0
        before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0
        after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm;text-4 md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span>me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am . . .
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="fle gap-6 sm:gap-8">
            <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 
            font-semibold">
                0{index+1}
            </p>
            <div class="flex flex-col gap-6 sm:gap-8">
                <h3 class="text-2xl sm:text-3xl md:text-5xl">
                    {benefit.name}
                </h3>
                <p>{benefit.description}</p>
            </div>
        </div>
      {/each}
    </div>
    <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete</span> Package</h5>
    <!-- <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"> -->
        <!-- <table class="bg-white text-slate-700 rounded text-center">
            <thead class="border-b border-solid border-slate-200">
                <tr class="">
                    <th></th>
                    <th class="whitespace-nowrap p-2 px-4">
                        Candidate #1
                    </th>
                    <th class="whitespace-nowrap p-2 px-4">
                        Candidate #2
                    </th>
                    <th class="whitespace-nowrap p-2 px-4">
                        Candidate #3
                    </th>
                    <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">
                        Me
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                    text-sm whitespace-nowrap">Dedication</td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-green-500"></i></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                    text-sm whitespace-nowrap">Critical Thought</td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-green-500"></i></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                    text-sm whitespace-nowrap">Interpersonnal Skills</td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-green-500"></i></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                    text-sm whitespace-nowrap">Programming ability</td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-slate-500"></i></td>
                    <td><i class="fa-solid fa-check text-green-500"></i></td>
                </tr>
            </tbody>
        </table> -->
    <!-- </div> -->
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
        <p>Scroll to see more &rarr;</p>
    </div>
    <!-- vf -->
  </section>
</main>
