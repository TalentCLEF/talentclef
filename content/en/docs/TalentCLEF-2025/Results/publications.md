---
title: Publications
date: 2017-01-05
categories: [Examples]
weight: 3
type: docs  
---
<style>
.talentclef-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0 8px;
  font-family: 'Segoe UI', Arial, sans-serif;
}

.talentclef-table th, .talentclef-table td {
  background: #fff;
  padding: 0.9em 1em;
  border: none;
}

.talentclef-table th {
  background: #1d3557;
  color: #fff;
  font-weight: 600;
  text-align: left;
  letter-spacing: 0.03em;
}

.talentclef-table tr {
  box-shadow: 0 3px 10px 0 rgba(60, 60, 80, 0.08);
  border-radius: 10px;
}

.talentclef-table td {
  vertical-align: middle;
}

/* TITLE COLUMN: ahora sin restricciones y más ancha */
.talentclef-title {
  max-width: 750px;
  min-width: 450px;
  font-size: 1em;
  font-weight: 500;
  /* Quita truncados */
  overflow: visible;
  text-overflow: unset;
  white-space: normal;
  word-break: break-word;
}

/* LINK COLUMN: solo subraya y color estándar */
.talentclef-link a {
  color: #1d3557;
  text-decoration: underline;
  background: none;
  padding: 0;
  border-radius: 0;
  font-weight: 500;
  font-size: 0.98em;
  transition: color 0.18s;
}
.talentclef-link a:hover {
  color: #457b9d;
  background: none;
}

/* Botón de copiar: igual */
.copy-btn {
  background: #145370;
  color: #fff;
  border: none;
  border-radius: 8px;
  padding: 0.45em 1.2em 0.45em 0.9em;
  font-size: 1em;
  font-weight: 500;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 0.4em;
  transition: background 0.18s;
}
.copy-btn:hover, .copy-btn:active {
  background:rgb(9, 36, 49);
  color: #fff;
}

.copy-btn .copy-icon {
  display: inline-block;
  font-size: 1.15em;
  vertical-align: middle;
}

.copy-btn2 {
  background: #1976d2;
  color: #fff;
  border: none;
  border-radius: 8px;
  padding: 0.42em 1.2em 0.42em 0.9em;
  font-size: 1em;
  font-weight: 500;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 0.4em;
  transition: background 0.18s;
}
.copy-btn2:hover, .copy-btn2:active {
  background: #115293;
  color: #fff;
}
</style>

{{< alert color="warning" >}}<i class="fas fa-exclamation-triangle"></i> Links to the CEUR Proceedings [here](https://ceur-ws.org/Vol-4038)
{{< /alert >}}


## Overview paper
  <p style="font-size: 1.06em; margin-bottom: 0.7em;">
    <strong>Please, cite:</strong>
  </p>
  <blockquote style="margin: 0 0 1em 0; font-size: 0.97em; color: #222; border-left: 3px solid #1976d2; padding-left: 1em;">
    Luis Gasco, Hermenegildo Fabregat, Laura García-Sardiña, Paula Estrella, Daniel Deniz, Álvaro Rodrigo and Rabih Zbib. 2025. Overview of the TalentCLEF 2025: Skill and Job Title Intelligence for Human Capital Management. In International Conference of the Cross-Language Evaluation Forum for European Languages. Springer.  
    <a href="https://www.arxiv.org/abs/2507.13275" target="_blank">[View preprint on arXiv]</a>
    <a href="https://link.springer.com/chapter/10.1007/978-3-032-04354-2_24" target="_blank">[View Springer paper]</a>
  </blockquote>

  <div style="margin-bottom: 0.6em;">
    <label for="bibtex-citation" style="font-size:0.88em; color:#1976d2; font-weight:500; margin-bottom: 0.3em; display:block;">
      BibTeX citation:
    </label>
    <pre id="bibtex-citation" style="background:#f2f5fa; width: 80%;color:#123; padding:0.8em 1em; border-radius:7px; font-size:0.8em; margin:0 0 0.4em 0; border:1px solid #dde5ef;">
@inproceedings{gasco2025overview,
  title={{Overview of the TalentCLEF 2025: Skill and Job Title Intelligence for Human Capital Management}},
  author={Gasco, Luis and Fabregat, Hermenegildo and Garc\'{\i}a-Sardi{\~n}a, Laura and Estrella, Paula and Deniz, Daniel and Rodrigo, \'{A}lvaro and Zbib, Rabih},
  booktitle={{Experimental IR Meets Multilinguality, Multimodality, and Interaction}},
  publisher={{Springer Nature Switzerland}},
  address={{Cham}},
  pages={{464--485}},
  isbn={{978-3-032-04354-2}},
  year={2025},
}
    </pre>
    <button class="copy-btn2" type="button" style="margin-top:2px;">
      <span class="copy-icon" style="margin-right:6px;">📋</span>
      Copy
    </button>
    <span class="copy-success" style="color:#1976d2; font-weight:500; margin-left:10px; display:none;">Copied!</span>
  </div>


## Participant papers

<table class="talentclef-table">
  <thead>
    <tr>
      <th style="width:100px;">Team</th>
      <th style="width:340px;">Title</th>
      <th style="width:90px;">Link</th>
      <th style="width:140px;">Bibtex</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Iagox</td>
      <td class="talentclef-title">Semantic Matching of Jobs and Skills Using LLMs and S-BERT</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_376.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{beyondtitles2025,
  title={{Semantic Matching of Jobs and Skills Using LLMs and S-BERT}},
  author={Iago Xabier Vázquez García, Rodrigo Sedano Puente, Silvia González González and Javier Sedano Franco},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>DS@GT TalentCLEF</td>
      <td class="talentclef-title">Multilingual Job Title Matching with MPNet-Based Sentence Transformers</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_366.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{mpnetmatcher2025,
  title={{Multilingual Job Title Matching with MPNet-Based Sentence Transformers}},
  author={Adam Brikman, Michael Sana and Holden Ruegger},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>NLPnorth</td>
      <td class="talentclef-title">NLPnorth @ TalentCLEF 2025: Comparing Discriminative, Contrastive, and Prompt-Based Methods for Job Title and Skill Matching</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_377.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{nlpnorth2025,
  title={{NLPnorth @ TalentCLEF 2025: Comparing Discriminative, Contrastive, and Prompt-Based Methods for Job Title and Skill Matching}},
  author={Mike Zhang and Rob van der Goot},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>UDII-UPM</td>
      <td class="talentclef-title">UDII-UPM at TalentCLEF 2025: Task A-Multilingual Job Title Matching</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_373.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{udiiupm2025,
  title={{UDII-UPM at TalentCLEF 2025: Task A-Multilingual Job Title Matching}},
  author={Javier Rodríguez-Vidal, Ascensión López-Vargas, Pablo Manuel Vigara Gallego, Francisco Javier Del Álamo and Ángel García-Beltrán},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>moali</td>
      <td class="talentclef-title">Enhancing Job-Skill Matching with LLM-Driven Data Augmentation and Fine-Tuned Bi-Encoders</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_363.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{llmdaug2025,
  title={{Enhancing Job-Skill Matching with LLM-Driven Data Augmentation and Fine-Tuned Bi-Encoders}},
  author={Mohab Ali},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>NT</td>
      <td class="talentclef-title">NT Team at Multilingual Job Title Matching Task A: Job Matching via Large Language Model-Based Description Generation and Retrieval</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_370.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{ntteam2025,
  title={{NT Team at Multilingual Job Title Matching Task A: Job Matching via Large Language Model-Based Description Generation and Retrieval}},
  author={Thuy Nga Ho, Thi Thanh Tuyen Ho and Van Thin Dang},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>SCaLAR</td>
      <td class="talentclef-title">Fine-Tuned Sentence Transformer for Multilingual Job Title Matching</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_365.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{finetunedst2025,
  title={{Fine-Tuned Sentence Transformer for Multilingual Job Title Matching}},
  author={Chinmay Bhangale, Prajwal Gabhane and Anand Kumar M},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>AlexU-NLP</td>
      <td class="talentclef-title">AlexU-NLP at TalentCLEF 2025: Curriculum-Driven Hybrid Retrieval for Multilingual Job Title Matching</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_364.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{alexunlp2025,
  title={{AlexU-NLP at TalentCLEF 2025: Curriculum-Driven Hybrid Retrieval for Multilingual Job Title Matching}},
  author={Rana Barakat, Omar Mokhtar, Marwan Torki and Nagwa Elmakky},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>SkillSeekers</td>
      <td class="talentclef-title">Enhancing Human Capital Management: AI Techniques for Candidate Matching and Skill Extraction</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_371.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{humancapitalai2025,
  title={{Enhancing Human Capital Management: AI Techniques for Candidate Matching and Skill Extraction}},
  author={Ahtisham Uddin, Muhammad Hasan Nizami, Muhammad Talha Salani and Ayesha Saeed},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>HULAT-UC3M</td>
      <td class="talentclef-title">HULAT-UC3M at TalentCLEF: ArtificialIntelligence and Natural Language Processing applied to HR Management</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_374.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{hulatuc3m2025,
  title={{HULAT-UC3M at TalentCLEF: ArtificialIntelligence and Natural Language Processing applied to HR Management}},
  author={Álvaro Tejera Villar and Isabel Segura Bedmar},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>COTECMAR–UTB</td>
      <td class="talentclef-title">Linking Job Titles and ESCO Skills with Sentence Transformer Embeddings</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_368.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{cotecmarutb2025,
  title={{COTECMAR--UTB at TalentCLEF 2025: Linking Job Titles and ESCO Skills with Sentence Transformer Embeddings}},
  author={Jhonattan Llamas, Edwin Puertas, Jairo Serrano and Juan Martinez},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>Ixa</td>
      <td class="talentclef-title">A Two-Stage Multilingual Job Title Matching System: Combining Expert Knowledge and LLM-based Ranking</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_372.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{expertrank2025,
  title={{A Two-Stage Multilingual Job Title Matching System: Combining Expert Knowledge and LLM-based Ranking}},
  author={Mar Rodríguez, Olatz Perez-de-Viñaspre and Naiara Perez},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>pjmathematician</td>
      <td class="talentclef-title">pjmathematician at TalentCLEF 2025: Enhancing Job Title and Skill Matching with GISTEmbed and LLM-Augmented Data</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_375.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{pjmathematician2025,
  title={{pjmathematician at TalentCLEF 2025: Enhancing Job Title and Skill Matching with GISTEmbed and LLM-Augmented Data}},
  author={Poojan Vachharajani},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>TechWolf</td>
      <td class="talentclef-title">Multilingual JobBERT for Cross-Lingual Job Title Matching</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_367.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{techwolf2025,
  title={{Multilingual JobBERT for Cross-Lingual Job Title Matching}},
  author={Jens-Joris Decorte, Matthias De Lange and Jeroen Van Hautte},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
    <tr>
      <td>VerbaNexAI</td>
      <td class="talentclef-title">VerbaNex at TalentCLEF2025: Semantic Matching of Multilingual Job Titles through a Framework Integrating ESCO Taxonomy</td>
      <td class="talentclef-link"><a href="https://ceur-ws.org/Vol-4038/paper_369.pdf" target="_blank">Link</a></td>
      <td>
        <button class="copy-btn" data-bibtex="@inproceedings{verbanex2025,
  title={{VerbaNex at TalentCLEF2025: Semantic Matching of Multilingual Job Titles through a Framework Integrating ESCO Taxonomy}},
  author={Melissa Moreno Novoa, Juan Carlos Martínez-Santos, Jairo Serrano and Edwin Puertas},
  booktitle={{CLEF (Working Notes)}},
  year={2025}
}">Copy bibtex</button>
      </td>
    </tr>
  </tbody>
</table>

<script>
document.querySelectorAll('.copy-btn').forEach(btn => {
  btn.addEventListener('click', function() {
    navigator.clipboard.writeText(this.getAttribute('data-bibtex'));
    this.textContent = "Copied!";
    setTimeout(() => { this.textContent = "Copy bibtex"; }, 5000);
  });
});

document.querySelectorAll('.copy-btn2').forEach(function(btn) {
  btn.addEventListener('click', function() {
    const pre = btn.parentElement.querySelector('pre');
    const text = pre.innerText;
    navigator.clipboard.writeText(text);
    btn.nextElementSibling.style.display = "inline";
    setTimeout(() => {
      btn.nextElementSibling.style.display = "none";
    }, 1200);
  });
});
</script>