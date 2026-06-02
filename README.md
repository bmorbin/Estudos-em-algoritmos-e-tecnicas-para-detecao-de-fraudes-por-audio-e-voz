# Estudos-em-algoritmos-e-t-cnicas-para-detec-o-de-fraudes-por-udio-e-voz
Estudos em algoritmos e técnicas para detecção de fraudes por áudio e voz para a máteria PSI5123: APRENDIZAGEM DE MÁQUINA DE SINAIS DE ÁUDIO E VOZ (2026/1) Escola Politécnica

Dataset: https://www.kaggle.com/datasets/mohammedabdeldayem/the-fake-or-real-dataset/data (for-2-seconds)

```mermaid
graph LR

classDef input fill:#111,stroke:#fff,color:#fff;
classDef block fill:#1f4e79,stroke:#fff,color:#fff;
classDef act fill:#d9534f,stroke:#fff,color:#fff;
classDef pool fill:#f0ad4e,stroke:#fff,color:#000;
classDef reg fill:#5bc0de,stroke:#fff,color:#000;
classDef fc fill:#5cb85c,stroke:#fff,color:#000;
classDef out fill:#222,stroke:#5cb85c,color:#fff;

%% ===== ENTRADA =====
A["Entrada<br/>40 × 63"]:::input

%% ===== BLOCO 1 =====
B1["Conv1D (40→16)<br/>k=3, p=1"]:::block
C1["ReLU"]:::act
D1["MaxPool k=2"]:::pool

%% ===== BLOCO 2 =====
B2["Conv1D (16→16)<br/>k=3, p=1"]:::block
C2["ReLU"]:::act
D2["MaxPool k=2"]:::pool
R["Dropout p=0.2"]:::reg

%% ===== CLASSIFICAÇÃO =====
F["Flatten<br/>240"]:::fc
G["Linear 240→2"]:::fc
H["Saída<br/>Real / Fake"]:::out

%% ===== FLUXO =====
A --> B1 --> C1 --> D1 --> B2 --> C2 --> D2 --> R --> F --> G --> H
```

Referências:

[1] J. Yi, Y. Lei, R. K. Das, H. Li, C. E. A. Mullis, and S. Narayanan, “A Survey of Audio Deepfake Detection,” arXiv preprint arXiv:2308.14970, 2023.

[2] H. D. Pham, D. V. Nguyen, H. N. Nguyen, T. T. Nguyen, and D. D. Le, “Audio Deepfake Detection Using Different Filter-Based Cepstral Features and Ensemble Learning,” in Proc. International Symposium on Intelligent Signal Processing and Communication Systems (ISPACS), 2024, doi: 10.1109/IS262782.2024.10704095.

[3] S. Davis and P. Mermelstein, “Comparison of Parametric Representations for Monosyllabic Word Recognition in Continuously Spoken Sentences,” IEEE Transactions on Acoustics, Speech, and Signal Processing, vol. 28, no. 4, pp. 357–366, Aug. 1980, doi: 10.1109/TASSP.1980.1163420.

[4] X. Zhou, D. Garcia-Romero, R. Duraiswami, C. Espy-Wilson, and S. Shamma, “Linear versus Mel Frequency Cepstral Coefficients for Speaker Recognition,” in Proc. IEEE Workshop on Automatic Speech Recognition and Understanding (ASRU), Waikoloa, HI, USA, 2011, pp. 559–564, doi: 10.1109/ASRU.2011.6163888.

[5] A. C. Leon, “Descriptive and Inferential Statistics,” in Comprehensive Clinical Psychology, A. S. Bellack and M. Hersen, Eds. Oxford, U.K.: Pergamon, 1998, pp. 243–285, doi: 10.1016/B0080-4270(73)00264-9.
