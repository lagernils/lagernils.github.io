---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<style>
  .cv-embed-desktop {
    border: 1px solid #e0e0e0;
    border-radius: 6px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  }
  .cv-embed-desktop iframe {
    border: none;
    display: block;
    width: 100%;
    height: 800px;
  }
  .cv-embed-mobile {
    display: none;
    text-align: center;
    padding: 2em 1em;
    border: 1px solid #e0e0e0;
    border-radius: 6px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  }
  .cv-embed-mobile a {
    display: inline-block;
    padding: 0.75em 1.5em;
    background-color: #494e52;
    color: #fff;
    border-radius: 4px;
    text-decoration: none;
    font-size: 1.1em;
  }
  @media (max-width: 768px) {
    .cv-embed-desktop {
      display: none;
    }
    .cv-embed-mobile {
      display: block;
    }
  }
</style>

<div class="cv-embed-desktop">
  <iframe src="/files/Nils_Lager_CV.pdf"></iframe>
</div>

<div class="cv-embed-mobile">
  <p>PDF preview is not supported on mobile browsers.</p>
  <a href="/files/Nils_Lager_CV.pdf" target="_blank">Open CV (PDF)</a>
</div>
