# Reasoning_Model
Building a reasoning model 
- Unsloth for efficient fine-tuning
- Llama 3.1-8B as the LLM to add reasoning capabilities to using GRPO.

The steps are simple:

1) Load the model
↳ We start by loading the Llama 3.1-8B model and tokenizer using Unsloth.

2) Define LoRA config
↳ We must use efficient techniques like LoRA to avoid fine-tuning the entire model weights.

3) Prepare dataset
↳ We use GSM8K, a math word problem dataset, and structure prompts to enforce step-by-step reasoning.

4) Define reward functions
↳ We create custom reward functions to reinforce reasoning.

5-6) Define GRPO trainer and train
↳ Lastly, we train using GRPO, an RL method to enhance reasoning. GRPO improves model performance without the need for a separate value function used in PPO.

Compare results
↳ Before fine-tuning, Llama 3 failed simple reasoning tasks.
↳ After GRPO fine-tuning, it explains its reasoning and gives the correct answer.
