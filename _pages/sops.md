---
layout: page
title: Standard Operating Procedures
permalink: /sops/
---

A collection of Standard Operating Procedures(SOP) for various PGC projects:

<div class="file-library-wrapper">
  <div class="file-library">

  {% for file in site.data.sops %}
    <div class="file-card">
      <h3>{{ file.title }}</h3>
      <p>{{ file.description }}</p>
      <a href="/assets/sops/{{ file.filename }}" download class="button button--primary button--small">Download</a>
    </div>
  {% endfor %}

  </div>
</div>

<style>
.file-library-wrapper {
  width: 100vw;                           
  margin-left: calc(-50vw + 50%);         
  padding: 2rem 4vw;
  box-sizing: border-box;
}


.file-library {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.file-card {
  background-color: var(--background-color);
  border: 1px solid var(--background-alt-color);
  border-radius: 12px;
  padding: 2rem;
  min-height: 220px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: box-shadow 0.2s ease;
}

.file-card .button {
  padding: 10px 16px; /* Less than the original 20px 24px */
  font-size: 15px;
  align-self: start;  /* Prevents it from stretching */
}


.file-card:hover {
  box-shadow: 0 4px 12px rgba(0,0,0,0.06);
}

.file-card h3 {
  margin-top: 0;
  font-size: $font-size-h3;
  color: var(--heading-font-color);
}

.file-card p {
  font-size: 16px;
  line-height: 1.5;
  color: var(--text-color);
  margin-bottom: 1rem;
}
</style>