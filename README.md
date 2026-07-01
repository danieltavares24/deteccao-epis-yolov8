# Detecção de EPIs com YOLOv8

Sistema de visão computacional para monitoramento automático do uso de equipamentos de proteção individual (capacetes e uniformes) em ambiente industrial.

## Performance do Modelo
O modelo foi treinado por 50 épocas utilizando Transfer Learning sobre o YOLOv8n.
- **mAP50:** 96.8% (Precisão Geral)
- **Precisão:** 93.8%
- **Recall:** 92.0%
- **Tempo de Inferência:** 2.53ms (Altíssima velocidade)

## Tecnologias e Desafios
- **Framework:** Ultralytics YOLOv8
- **Hardware:** GPU NVIDIA T4 (CUDA)
- **Dataset:** 600 imagens anotadas (4 classes: head, work_hat, clothes, work_clothes)

### Superação de Obstáculos:
Durante o desenvolvimento, realizei o troubleshooting de infraestrutura no Google Colab, corrigindo problemas de alocação de GPU e normalização de caminhos (paths) no arquivo de configuração YAML.

**Projeto independente desenvolvido por Daniel Tavares de França — 2026.**
