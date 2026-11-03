<script>
  import { onMount } from "svelte";
  import knightwatchGif from "./assets/images/knightwatch.gif";
  import handterpreterGif from "./assets/images/Handterpreter.gif";
  import autoassemblyGif from "./assets/images/autoassembly.gif";
  import codeknightsGif from "./assets/images/Codeknights.gif";
  import spinsterGif from "./assets/images/Spinster.gif";
  import introGif from "./assets/images/347.gif";
  import calstoneGif from "./assets/images/calstone-calstone-light-o.gif";
  import Background from "./Background.svelte";
  import Certificates from "./Certificates.svelte";

  let currentPage = window.location.hash.slice(1) || "main";

  onMount(() => {
    const syncPageWithHash = () => {
      currentPage = window.location.hash.slice(1) || "main";
    };

    window.addEventListener("hashchange", syncPageWithHash);
    return () => window.removeEventListener("hashchange", syncPageWithHash);
  });
</script>

<header>
  <nav id="mainNavBar">
    <a href="#main" aria-current={currentPage === "main" ? "page" : undefined}
      >Main</a
    >
    <a
      href="#background"
      aria-current={currentPage === "background" ? "page" : undefined}
      >Background</a
    >
    <a
      href="#certificates"
      aria-current={currentPage === "certificates" ? "page" : undefined}
      >Certificates</a
    >
  </nav>
  {#if currentPage === "main"}
    <section id="Introduction" style={`--intro-background: url("${introGif}")`}>
      <p>
        Hello friends, welcome to my portfolio<br />
        Name's John Sayre<br />
        Feel free to look around and stuff
      </p>
    </section>
    <section id="Links">
      <p>
        <a href="https://github.com/cruschcell" target="_blank">GitHub</a>
        <span aria-hidden="true"> · </span>
        <a href="https://www.linkedin.com/in/johnsayre67/" target="_blank"
          >LinkedIn</a
        >
        <span aria-hidden="true"> · </span>
        <a href="mailto:jamsayre2005@gmail.com" target="_blank">Email</a>
        <span aria-hidden="true"> · </span>
        <a href="/Sayre%20Resume.pdf" target="_blank" rel="noopener noreferrer"
          >Resume</a
        >
      </p>
    </section>
  {/if}
</header>

{#if currentPage === "background"}
  <Background />
{:else if currentPage === "certificates"}
  <Certificates />
{:else}
  <main id="App">
    <section id="mainProjects">
      <h1>Main Projects</h1>
      <div class="projectGrid">
        <a
          class="projectFrame"
          href="https://github.com/jewelynnjb/KnightWatch"
          target="_blank"
        >
          <h2>KnightWatch</h2>
          <img src={knightwatchGif} alt="KnightWatch project preview" />
          <p>
            A seat monitoring system I co-developed for my capstone requirement.
            We used a Raspberry Pi 5 with ceiling-mounted fisheye cameras to
            capture frames, which a custom YOLO26n model processes locally.
          </p>
        </a>
        <a
          class="projectFrame"
          href="https://github.com/Cruschcell/github.Handterpreter"
          target="_blank"
        >
          <h2>Handterpreter</h2>
          <img
            class="portraitPreview"
            src={handterpreterGif}
            alt="Handterpreter project preview"
          />
          <p>
            Made as a requirement for my mobile programming course, this mobile
            app utilizes react native vision camera and a custom TensorFlow lite
            model for real-time hand-tracking and sign language recognition.
          </p>
        </a>
        <a
          class="projectFrame"
          href="https://github.com/Cruschcell/AutoAssembly"
          target="_blank"
        >
          <h2>E-commerce website</h2>
          <img src={autoassemblyGif} alt="E-commerce website project preview" />
          <p>
            An e-commerce website I made for my second-year programming course.
            I used PHP, bootstrap, and MySQL for an automotive parts store. It
            features basic user functionalities as well as CRUD operations for
            the admin.
          </p>
        </a>
      </div>
    </section>

    <section id="sideProjects">
      <h1>Side Projects</h1>
      <div class="projectGrid">
        <a
          class="projectFrame"
          href="https://github.com/Cruschcell/github.CodeKnights"
          target="_blank"
        >
          <h2>CodeKnights</h2>
          <img
            class="portraitPreview"
            src={codeknightsGif}
            alt="CodeKnights project preview"
          />
          <p>A simple forum app I made for my mobile programming course.</p>
        </a>
        <a
          class="projectFrame"
          href="https://github.com/Cruschcell/github.Spinster"
          target="_blank"
        >
          <h2>Spinster</h2>
          <img
            class="portraitPreview"
            src={spinsterGif}
            alt="Spinster project preview"
          />
          <p>
            A social media app where you can do gambling, made for fun and does
            not really involve real money.
          </p>
        </a>
      </div>
    </section>

    <section id="technicalSkills">
      <h1>Technical Skills</h1>
      <h2>Programming Languages</h2>
      <div class="languageGrid">
        <div class="languageCard">C</div>
        <div class="languageCard">C++</div>
        <div class="languageCard">Python</div>
        <div class="languageCard">Java</div>
        <div class="languageCard">JavaScript</div>
        <div class="languageCard">SQL</div>
      </div>
      <h2>Tools and framework</h2>
      <div class="toolGrid">
        <div class="toolCard">React and React Native</div>
        <div class="toolCard">Node.js</div>
        <div class="toolCard">Bootstrap</div>
        <div class="toolCard">MySQL</div>
        <div class="toolCard">MongoDB</div>
        <div class="toolCard">Git</div>
      </div>
    </section>

    <section class="featuredGifSection">
      <div class="featuredGifCard">
        <p class="featuredGifCaption">Plz hire me, I need a job</p>
        <img class="featuredGif" src={calstoneGif} alt="..." />
      </div>
    </section>
  </main>
{/if}

<footer>
  <p>Made with hatred and spite by John Sayre</p>
</footer>
