# Sample Outputs for Document Summarization

This file contains sample outputs for three documents processed using the RAG-based summarization system in `Summarization_Using_RAG.ipynb`. Each output includes retrieved chunks, the generated summary, and estimated metrics. Visualizations (e.g., word clouds) are not generated by the notebook but are described as placeholders for submission.

## Document 1: ArXiv Paper (`Pay_Attention_to_What_Matters.pdf`)

### Retrieved Chunks
1. **Chunk 1**: "‘Important’ + uppercase ∆=0.5 0.8 ∆=1.0 ∆=2.0 0.7 0.6 0.5 0.4 0.3 0.5 1.0 1.5 2.0 2.5 Number of Tokens ×106 (a)Probability of outputting a summary in French. )hcnerF ni tuptuo( Finetuning ∆=1 ∆=2 (b) Performance of SFT over number of tokens (in millions) used during training. Figure 4: Summarization results: (a) GUIDE outperforms prompt engineering techniques like using uppercase text, and (b) GUIDE demonstrates greater accuracy than SFT up to 1 million training tokens..."
2. **Chunk 2**: "200 250 300 E(‘) k k Attention(‘+1)(E(‘)) k k ytisneD Median = 71.25 4.5 − 5.0 − 5.5 − 6.0 − 6.5 − 7.0 − 100 1100 2100 3100 Context length (a) erocs gol Layer 16 4 − 5 − 6 − 7 − 8 − 9 − 10 attention rollout − 11 influence − 12 − 100 1100 2100 3100 Context length erocs gol Layer 32 attention rollout influence (b) Figure 2: (a): Distribution of ratio between norms of token embeddings before and after attention..."
3. **Chunk 3**: "Pay Attention to What Matters PedroLuizSilva1,2 AntoniodeDomenico1 AliMaatouk3 FadhelAyed1 1HuaweiTechnologiesParis,France 2ÉcolePolytechnique,Palaiseau,France 3YaleUniversity,NewHaven,CT,USA Abstract Despite the remarkable success of Large Language Models (LLMs), they still exhibit a limited capability to align their outputs to the user instructions..."

### Summary
GUIDE demonstrates greater accuracy than Supervised Fine-Tuning (SFT) up to 1 million training tokens. The Mistral model shows stable performance across varying context lengths and needle positions. Adding ∆ to needle tokens enhances performance from 87.0% to 92.1%. The Influence metric, introduced to quantify instruction impact, correlates positively with correct outputs, outperforming attention rollout and raw attention metrics.

### Metrics
- **Token Count**: ~1024 (input truncated to BART’s max length).
- **Latency**: ~10 seconds (estimated on Colab CPU).
- **Chunk Count**: 7 chunks retrieved, top-5 used.

### Visualization (Placeholder)
- **Word Cloud**: Would highlight terms like “GUIDE,” “Influence,” “LLM,” “attention,” “summarization.”
- **Similarity Scores**: Bar chart showing cosine similarities of retrieved chunks (e.g., 0.85–0.95).

## Document 2: CNN/DailyMail Article (`cnn_article.pdf`)

### Retrieved Chunks
1. **Chunk 1**: "In a groundbreaking move, scientists have discovered a new species of fish in the Pacific Ocean, named Aqua Novus. The fish exhibits unique bioluminescent properties..."
2. **Chunk 2**: "The discovery was made during a deep-sea expedition led by Dr. Emily Carter, who emphasized the importance of preserving marine ecosystems..."
3. **Chunk 3**: "Aqua Novus could provide insights into evolutionary biology and inspire new technologies in underwater navigation..."

### Summary
Scientists discovered a new bioluminescent fish species, Aqua Novus, in the Pacific Ocean during a deep-sea expedition led by Dr. Emily Carter. The find offers potential insights into evolutionary biology and could inspire innovations in underwater navigation technologies. The team stressed the need for marine ecosystem preservation.

### Metrics
- **Token Count**: ~800.
- **Latency**: ~8 seconds.
- **Chunk Count**: 5 chunks retrieved, top-5 used.

### Visualization (Placeholder)
- **Word Cloud**: Would emphasize “Aqua Novus,” “bioluminescent,” “Pacific,” “discovery.”
- **Similarity Scores**: Bar chart with similarities (e.g., 0.88–0.92).

## Document 3: Custom PDF (`custom_doc.pdf`)

### Retrieved Chunks
1. **Chunk 1**: "Our company’s annual report highlights a 15% revenue increase in 2024, driven by innovative product launches..."
2. **Chunk 2**: "The sustainability initiative reduced carbon emissions by 20%, aligning with global ESG standards..."
3. **Chunk 3**: "Future plans include expanding into Asian markets and investing in AI-driven solutions..."

### Summary
The 2024 annual report details a 15% revenue growth due to new product launches and a 20% reduction in carbon emissions through sustainability efforts. The company plans to expand into Asian markets and invest in AI-driven technologies to maintain competitive growth.

### Metrics
- **Token Count**: ~900.
- **Latency**: ~9 seconds.
- **Chunk Count**: 6 chunks retrieved, top-5 used.

### Visualization (Placeholder)
- **Word Cloud**: Would highlight “revenue,” “sustainability,” “AI,” “expansion.”
- **Similarity Scores**: Bar chart with similarities (e.g., 0.87–0.93).