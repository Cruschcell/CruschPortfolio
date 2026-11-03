<script>
  const certificates = [
    { name: "Cisco Cybersecurity Certificate", file: "CiscoCyberSecCert.pdf" },
    { name: "Database Certificate", file: "DatabaseCert.pdf" },
    { name: "Networking Certificate", file: "NetworkingCert.pdf" },
  ];
</script>

<main class="certificatesPage">
  <h1>Certificates</h1>
  <div class="certificateGrid">
    {#each certificates as certificate}
      <article class="projectFrame certificateCard">
        <div class="certificatePreview">
          <iframe
            src={`${import.meta.env.BASE_URL}${certificate.file}#toolbar=0&navpanes=0&scrollbar=0`}
            title={`Preview of ${certificate.name}`}
          ></iframe>
          <a
            class="certificatePreviewLink"
            href={`${import.meta.env.BASE_URL}${certificate.file}`}
            target="_blank"
            rel="noopener noreferrer"
            aria-label={`Open ${certificate.name} PDF in a new tab`}
          ></a>
        </div>
        <h2>{certificate.name}</h2>
      </article>
    {/each}
  </div>
</main>
