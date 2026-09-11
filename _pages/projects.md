---
layout: single
title: "Selected Projects"
permalink: /projects/
excerpt: "Selected research projects in molecular machine learning and AI for scientific discovery."
author_profile: true
---

My research develops **general machine-learning methods for scientific discovery**, with molecular design and drug discovery as the primary application domain. These selected projects reflect my current focus on pretrained representations, generative models, and reward-guided optimization.

<div class="project-card">
  <div class="project-card__header">
    <div>
      <h2 id="ew-sft">Elite-Weighted Supervised Fine-tuning (EW-SFT)</h2>
      <p class="project-card__meta">Goal-directed molecular optimization · 2026 · Biogen × UMass Amherst</p>
    </div>
    <p class="project-card__links"><a href="https://arxiv.org/abs/2609.00189">Paper <i class="fas fa-external-link-alt" aria-hidden="true"></i></a></p>
  </div>
  <p>EW-SFT is a reward-guided optimization method for adapting molecular generators without deriving a separate trajectory-level reinforcement-learning objective for each architecture. It maintains a rolling elite buffer of genetically evolved, high-scoring molecules and fine-tunes each generator with its native pretraining loss.</p>
  <ul>
    <li><strong>General method:</strong> uses reward-guided elite selection and native-loss adaptation across autoregressive, masked-diffusion, and discrete-flow molecular generators.</li>
    <li><strong>Constrained generation:</strong> evaluated on de novo design, motif extension, and linker design with 3D-shape and 2D-similarity objectives, as well as the PMO benchmark.</li>
  </ul>
  <figure class="project-card__figure">
    <a href="{{ base_path }}/images/ICLR_workflow.pdf" aria-label="Open the EW-SFT workflow figure as a PDF">
      <img src="{{ base_path }}/images/projects/ew-sft-workflow.png" alt="EW-SFT workflow: molecular generators sample candidates, genetic search evolves molecules, oracle scoring selects an elite set, and the generator is updated with an elite-weighted native loss.">
    </a>
    <figcaption>EW-SFT uses a shared selection-and-native-loss update while preserving each generator's own proposal mechanism and training objective.</figcaption>
  </figure>
</div>

<div class="project-card">
  <div class="project-card__header">
    <div>
      <h2 id="ped">Pretrained Embedding Distance (PED)</h2>
      <p class="project-card__meta">Virtual screening and molecular generation · 2026 · Biogen</p>
    </div>
    <p class="project-card__links"><a href="https://arxiv.org/abs/2604.24474">Paper <i class="fas fa-external-link-alt" aria-hidden="true"></i></a> <span aria-hidden="true">·</span> <a href="https://openreview.net/forum?id=HbfrCipfNl">ICML AI4Science <i class="fas fa-external-link-alt" aria-hidden="true"></i></a></p>
  </div>
  <p>PED is a training-free molecular similarity measurement computed from the representations of pretrained molecular foundation models. It provides a shared representation-space measure for ligand-based virtual screening and for steering molecular generation.</p>
  <ul>
    <li><strong>Representation learning for screening:</strong> ranks candidate molecules using distances from pretrained molecular language, diffusion, graph-Transformer, and multimodal models.</li>
    <li><strong>Reward-guided generation:</strong> uses embedding distance as a reward signal for SMILES-based and synthesizable molecular generation, with evaluation of retrieval quality, sample efficiency, diversity, drug-likeness, and model-predicted binding affinity.</li>
  </ul>
  <figure class="project-card__figure">
    <a href="{{ base_path }}/images/PED-Main.pdf" aria-label="Open the PED workflow figure as a PDF">
      <img src="{{ base_path }}/images/projects/ped-workflow.png" alt="Pretrained Embedding Distance workflow connecting virtual screening and reinforcement-learning molecular generation, comparing traditional molecular similarity with distances in pretrained molecular-model embeddings.">
    </a>
    <figcaption>Pretrained embedding distance connects molecular similarity, ligand-based virtual screening, and reward-guided molecular generation.</figcaption>
  </figure>
</div>

<p class="project-note">For my complete publication record, please see my <a href="{{ site.author.googlescholar }}">Google Scholar profile</a>.</p>
