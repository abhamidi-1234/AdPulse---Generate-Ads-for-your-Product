# AdPulse---Generate-Ads-for-your-Product

BLOOM is an open-access decoder-only transformer model, collaboratively developed by hundreds of researchers, aiming to democratize advanced LLM technology. Trained on the ROOTS corpus encompassing diverse languages, BLOOM demonstrates strong performance across various benchmarks, especially after multitasking prompted finetuning.

BLOOM is trained on the ROOTS corpus, a composite collection of 498 Hugging Face datasets amounting to 1.61 terabytes of text that span 46 natural languages and 13 programming languages.

This LLM model has been trained on the Product Descriptions and Ads dataset from Hugging Face and fine-tuned by using Parameter-Efficient Fine-Tuning (PEFT) techniques to generate simple marketing lines for your product.

## Note

I am using the Bloom LLM with 1.7 Billion parameters. Compare this with GPT-4 which has a whopping 1.76 Trillion parameters. So, naturally, the performance of this model is not up to the mark. But Bloom is open-source and free to use. Use other LLMs for better content generation. 

## What is Parameter-Efficient Fine-Tuning (PEFT) of LLMs?

Parameter-Efficient Fine-Tuning (PEFT) enables you to fine-tune a small subset of parameters in a pretrained LLM. The main idea is that you freeze the parameters of a pre-trained LLM, add some new parameters, and fine-tune the new parameters on a new (small) training dataset. Typically, the new training data is specialized for the new task you want to fine-tune your LLM for (e.g., for the clinical domain).

## What are examples of PEFT techniques?

1. Adapters add tunable layers to the various transformer blocks of an LLM. Prefix tuning adds trainable tensors to each transformer block.

2. LoRA (Low-rank adaptation of large language models) has become a widely used technique to fine-tune LLMs. An extension, known as QLoRA, enables fine-tuning on quantized weights, such that even large models such as Llama-2 can be trained on a single GPU. The QLoRA paper states that “ [QLoRA] reduces memory usage enough to finetune a 65B parameter model on a single 48GB GPU while preserving full 16-bit finetuning task performance. QLoRA backpropagates gradients through a frozen, 4-bit quantized pretrained language model into Low Rank Adapters (LoRA).”

## Why is Parameter-Efficient Fine-Tuning important?

Fine-tuning a Large-Language Model (LLMs) has traditionally required retraining its entire set of parameters. However, with even open-source models, such as Llama-2-70b requiring 140GB of GPU memory, this approach is computationally expensive. PEFT enables you to fine-tune a LLM with less resources.
