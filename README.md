# Update code to most recent iteration

# Large Language Model Assertion Pipeline (updated - 2/25/24)
## For question, contact: 

This code is for the large language model assertion pipeline. Detailed instructions coming soon!

### Pipeline flow:
1. Run ```run_umls_synonym_ner.py``` and ```run_dataset_ner.py``` to build NER datasets (recommend using targeted NER prompts instead of broad NER prompts for NER dataset pull)
2. (Optional - highly recommended) Run ```run_ner_cosine_similarity.py``` followed by ```run_llm_filter_cosine_sim_ner_output.py``` to filter NER outputs (filter NER outputs to remove the low-yield named entities --> also helpful to review filtered NER outputs and remove those that are not related to your target entity)
3. Run ```run_extraction.py``` to build target-matcher and extract high-yield text from clinical notes
4. Run ```run_llm_assertion.py``` to generate LLM assertions