# llm_moral_plasticity

## Research Question:
Are the “moral values” of LLMs robust to morally irrelevant situational distractors? We investigate this question as part of our CSE 481M Natural Language Processing Capstone project. This repository serves as a platform to reproduce our results.

![image](https://github.com/user-attachments/assets/9d9c3c53-c526-4755-8b58-a1e8e0ec6d89)


## Useful Commands

Run evaluation with specified experiment, dataset, model, and question types:

```bash
CUDA_VISIBLE_DEVICES=0 python -m src.evaluate \
  --experiment-name "moraltest" \
  --dataset "moralchoice_high_ambiguity" \
  --model "google/flan-t5-small" \
  --question-types "ab" \
  --eval-nb-samples 5 \
  --eval-max-tokens 1
```

Run result collection on experiment and specified dataset:

```bash
python -m src.collect \
  --experiment-name "moraltest" \
  --dataset "moralchoice_high_ambiguity"
```

