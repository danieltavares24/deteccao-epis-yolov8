# Detecção de EPIs com YOLOv8

Sistema de visão computacional para monitoramento automático do uso 
de equipamentos de proteção individual (capacetes e uniformes) em 
ambiente industrial.

Projeto independente desenvolvido por Daniel Tavares de França — 2026.

---

## Objetivo

Monitorar automaticamente o uso correto de EPIs (capacetes e uniformes) 
em ambientes industriais, reduzindo riscos de acidentes e eliminando a 
necessidade de inspeção manual contínua.

---

## Performance do Modelo

| Métrica | Resultado |
|---|---|
| mAP@50 | **96.8%** |
| Precisão | 93.8% |
| Recall | 92.0% |
| Tempo de inferência | 2.53ms/imagem |

Treinamento: 50 épocas · Transfer Learning sobre YOLOv8n · GPU NVIDIA T4

---

## Exemplos de Detecção

### Predições do modelo
![Predições batch 0](val_samples/val_batch0_pred.jpg)
![Predições batch 1](val_samples/val_batch1_pred.jpg)
![Predições batch 2](val_samples/val_batch2_pred.jpg)

### Ground Truth (labels reais)
![Labels batch 0](val_samples/val_batch0_labels.jpg)

---

## Métricas de Treinamento

![Resultados gerais](metrics/results.png)
![Curva F1](metrics/BoxF1_curve.png)
![Curva PR](metrics/BoxPR_curve.png)
![Matriz de Confusão](metrics/confusion_matrix_normalized.png)
![Distribuição de labels](metrics/labels.jpg)

---

## Stack Tecnológica

- **Framework:** Ultralytics YOLOv8
- **Linguagem:** Python
- **Hardware:** GPU NVIDIA T4 (Google Colab)
- **Dataset:** 600 imagens anotadas manualmente
- **Classes:** `head`, `work_hat`, `clothes`, `work_clothes`

---

## Estrutura do Repositório

deteccao-epis-yolov8/
├── Projet_EPI.ipynb          # Pipeline completo de treinamento
├── meu_projeto.yaml          # Configuração do dataset
├── metrics/                  # Curvas e métricas de treinamento
├── val_samples/              # Amostras de validação com predições
├── weights/                  # Pesos do modelo treinado
└── README.md

---

## Como Executar

pip install ultralytics

yolo predict model=weights/best.pt source=sua_imagem.jpg

---

© 2026 Daniel Tavares de França | Visão Computacional & IA
