<script>
  import highSchoolImage from "./assets/images/LPCNSHSTDC.jpg";
  import letranImage from "./assets/images/Letran.jpg";
  import gamingImage from "./assets/images/gaming.png";
  import aloricaImage from "./assets/images/alorica.png";
  import adconnexionImage from "./assets/images/adcon.jpeg";
  import developmentImage from "./assets/images/dev.jpg";
</script>

<main id="Background">
  <section class="EducationalBackground">
    <h1>Educational Background</h1>
    <div class="educationalBackgroundContainer">
      <img
        src={highSchoolImage}
        alt="Las Piñas City National Senior High School, Talon Dos Campus"
      />
      <div>
        <h2>Las Piñas City National Senior High School - Talon Dos Campus</h2>
        <p>
          I took the STEM strand and especially enjoyed math and science,
          including calculus, probability and statistics, physics, biology, and
          chemistry. I also explored robotics, architecture with AutoCAD, ESP32
          projects, and research in preparation for college.
        </p>
      </div>
    </div>
    <div class="educationalBackgroundContainer">
      <img
        class="letranImage"
        src={letranImage}
        alt="Colegio de San Juan de Letran Manila"
      />
      <div>
        <h2>Colegio de San Juan de Letran Manila</h2>
        <p>
          I’m currently a fourth-year BSIT student specializing in Systems
          Engineering. My coursework includes programming, databases,
          networking, cybersecurity, embedded systems, and algorithms, with a
          growing focus on IoT. I’ve also worked on a capstone and projects for
          programming and mobile development courses. I made the Dean’s List in
          my second year and have maintained my scholarship through college.
        </p>
      </div>
    </div>
  </section>
  <section class="ProfessionalBackground">
    <h1>Professional Background</h1>
    <div class="educationalBackgroundContainer">
      <img src={adconnexionImage} alt="ADConnexion" />
      <div>
        <h2>ADConnexion</h2>
        <p>
          As an intern, I mainly supported digital design work, creating visual
          materials with tools like Photoshop and Canva.
        </p>
      </div>
    </div>
    <div class="educationalBackgroundContainer">
      <img src={aloricaImage} alt="Alorica" />
      <div>
        <h2>Alorica</h2>
        <p>
          I worked as a customer service representative, helping
          telecommunications customers troubleshoot broadband, network, and
          account issues. I guided customers through basic checks, documented
          cases, and escalated more complex problems to higher-tier teams.
        </p>
      </div>
    </div>
  </section>
  <section class="PersonalBackground">
    <h1>Personal Background</h1>
    <div class="educationalBackgroundContainer">
      <img src={gamingImage} alt="Gaming" />
      <div>
        <h2>Gaming</h2>
        <p>I enjoy gaming and would love to create a game of my own someday.</p>
      </div>
    </div>
    <div class="educationalBackgroundContainer">
      <img src={developmentImage} alt="Mobile app development" />
      <div>
        <h2>Building things</h2>
        <p>
          Development is very challenging, but seeing something I made come to
          life made all the hard work worthwhile.
        </p>
      </div>
    </div>
  </section>
</main>
