# SQL-Engage Dataset
**An emotion-aware synthetic SQL error dataset for adaptive feedback and engagement modeling in educational environments.**  
Developed at the [Adaptive Learning & Gamification Lab (ALGL)](https://hazraimran.ca/algl), Northeastern University Vancouver.  

---

## Overview  
Learning to write SQL queries is challenging for many students. Traditional autograders provide generic messages such as *“syntax error,”* which offer little instructional value or emotional support.  
The **SQL-Engage Dataset** was created to advance research on **adaptive educational feedback systems** that combine:  
- **Natural Language Processing (NLP)** for error understanding,  
- **Machine Learning** for SQL error classification, and  
- **Behavioral and emotional modeling** for engagement-aware feedback design.  

This dataset provides a structured foundation for developing systems that can identify SQL query errors, infer user engagement or frustration, and generate contextually supportive feedback messages.

---

## Dataset Schema  
Each record represents one learner query instance with associated error and feedback annotations.

| Column | Description |
|---------|--------------|
| **query** | SQL statement (correct or incorrect). |
| **error_type** | Main category: {syntax, schema, logic, construction}. |
| **error_subtype** | Fine-grained subtype (23 total, e.g., *missing semicolon*, *undefined column*, *inefficient query*). |
| **emotion** | Inferred or simulated learner emotion (*happy*, *frustrated*, *neutral*, *focused*, etc.). |
| **feedback_target** | Supportive, hint-based feedback message tailored to the error and emotional state. |
| **intended_learning_outcome** | Concept reinforced by this feedback (e.g., SELECT syntax, JOIN logic). |

---

## Data Generation and Provenance  

| Stage | Details |
|-------|----------|
| **Schema Context** | Cybernetic Sabotage database with tables: Employees, Robots, Logs, Incidents, Access_Codes. |
| **Initial Generation (500 samples)** | Generated using **GPT-3.5-Turbo**, manually reviewed and validated. |
| **Augmentation (1,000 samples)** | Produced with **Llama-3.1-70B** using subtype-specific prompts; refined using **Claude 3 Sonnet** and **ChatGPT**. |
| **Environment** | Python 3.13.2 using `pandas` and `openai` APIs. |
| **Structure** | 1,500 total samples covering 4 major error types and 23 subtypes. |
| **Nature** | Fully synthetic, balanced, and manually validated for linguistic and logical diversity. |

---

## Intended Research Applications  
- SQL **error classification** and **taxonomy development**  
- **Adaptive feedback** modeling in intelligent tutoring systems  
- **Emotion- and engagement-aware learning analytics**  
- Benchmarking for **NLP/LLM-based educational feedback**  
- Reinforcement or retrieval-augmented feedback generation pipelines  

---

## Attribution  

**Dr. Hazra Imran** — *Lead Researcher & Dataset Architect*  
> Concept design, taxonomy definition, feedback modeling, validation framework, and documentation.  

**Yan Wang** — *Research Assistant*  
> Data generation, Python implementation, and manual quality review under supervision.  

Developed within the [Adaptive Learning & Gamification Lab (ALGL)](https://hazraimran.ca/algl), Northeastern University Vancouver.  

---

## License  
This dataset is released under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License.  
You may share and adapt the material for non-commercial research and educational purposes with appropriate credit to the authors.

---

## Citation  

If you use this dataset, please cite:  

**APA Format**  
Imran, H., & Wang, Y. (2025). *SQL-Engage: An Emotion-Aware Synthetic SQL Error Dataset for Adaptive Feedback and Engagement Modeling.* Adaptive Learning and Gamification Lab, Northeastern University Vancouver. https://github.com/hazra-imran/sql-engage-dataset  

**BibTeX**  
```bibtex
@dataset{imran2025sqlengage,
  title        = {SQL-Engage: An Emotion-Aware Synthetic SQL Error Dataset for Adaptive Feedback and Engagement Modeling},
  author       = {Imran, Hazra and Wang, Yan},
  year         = {2025},
  institution  = {Northeastern University Vancouver, Adaptive Learning and Gamification Lab},
  doi          = {10.5281/zenodo.17555894},
  url          = {https://doi.org/10.5281/zenodo.17555894},
  license      = {CC BY 4.0}
}
```

---

## Future Work  
This dataset serves as the foundation for an integrated adaptive feedback system that unites:  
- SQL error classification via NLP/LLM models,  
- Keystroke-based engagement and emotion inference, and  
- Context-adaptive feedback generation.  

Future releases will include the **feedback generation ruleset**, **engagement dataset (SQL-Engage-v2)**, and baseline **ML/NLP notebooks** for reproducible benchmarking.

---

**© 2025 Adaptive Learning & Gamification Lab (ALGL), Northeastern University Vancouver**  
https://hazraimran.ca/algl  



