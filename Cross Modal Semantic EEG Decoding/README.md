# Cross Modal Semantic EEG Decoding

Imagine this scenario:

The word **flower** is shown to you as a picture .   
The same word **flower** is presented in written form .  
Finally, the word **flower** is spoken to you out loud .

Question:

Do these modalities converge into a **shared semantic space**, since the meaning is always the same: **Flower**?

# Challenge
Traditional BCIs often require training within a single modality (e.g., only images or only sounds). This restriction reduces flexibility and efficiency, especially for patients who cannot access all modalities (e.g.individuals with hearing or visual impairments).

If a shared semantic space truly exists in the brain, BCIs could be designed to:
+ Train on one modality (e.g., visual).
+ Generalize to other modalities (e.g., auditory or orthographic).
  
# Applications
1. Communication for locked-in patients:
Even if a patient cannot speak or hear, simply imagining visual concepts could be enough for a BCI to decode meaning from the shared semantic space.
2. Reduced training demands:
Users would not need extensive training across every modality; training in one domain could transfer to others.
3. Improved robustness and flexibility:
Focusing on semantic meaning rather than sensory details could yield BCIs that perform better in noisy environments and clinical settings.

# Methods
**Dataset** :  
High-resolution EEG dataset (124 channels, 12 participants).  
**Tasks:**  
perception and imagination.   
**Modalities:**  
pictorial (visual), orthographic (text), auditory (spoken).  
**Preprocessing:**  
Band-pass filtering (1–40 Hz).
Artifact removal via ICA.
Epoch segmentation aligned to stimulus onsets.   
**Modeling:**  
Cross-classification: Train on one modality, test on another.
Representational Similarity Analysis (RSA): Compare EEG embeddings across modalities to identify shared semantic structure.
