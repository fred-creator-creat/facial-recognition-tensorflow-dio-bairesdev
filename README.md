# 🤖 Sistema de Reconhecimento Facial com Deep Learning (TensorFlow & OpenCV)

[![Link do Projeto](https://img.shields.io/badge/DIO-BairesDev-orange)](https://web.dio.me/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow)](https://www.tensorflow.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-5C3EE8?logo=opencv)](https://opencv.org/)

## 📝 Descrição do Projeto
Este projeto foi desenvolvido para o desafio técnico **"Criando um Sistema de Reconhecimento Facial do Zero"**, parte da trilha de formação em Machine Learning da **BairesDev** na plataforma **DIO**. 

O objetivo foi implementar um sistema completo capaz de capturar imagens via webcam, detectar faces e realizar a classificação biométrica em tempo real, utilizando redes neurais convolucionais (CNNs).

---

## 🏗️ Arquitetura do Sistema
O sistema opera através de uma abordagem de **Rede Dual (Two-Stage Pipeline)**:

1.  **Stage 1: Detecção Facial (Segmentation)**
    * Utilização do algoritmo **Haar Cascade** (via OpenCV) para a localização das coordenadas espaciais do rosto (Bounding Boxes).
    * Tratamento de imagem: Conversão para escala de cinza e normalização.

2.  **Stage 2: Classificação e Reconhecimento (Feature Extraction)**
    * Implementação de **Transfer Learning** utilizando a arquitetura **MobileNetV2**.
    * A rede foi ajustada (Fine-Tuning) para identificar o usuário específico (**Fred**) em oposição a classes desconhecidas.
    * Camadas densas finais customizadas com ativação *Softmax* para predição de probabilidade.

---

## 🚀 Tecnologias e Ferramentas
* **Linguagem:** Python 3.x
* **Framework de Deep Learning:** TensorFlow / Keras
* **Visão Computacional:** OpenCV (Open Source Computer Vision Library)
* **Ambiente:** Google Colab (com aceleração de hardware via GPU T4)
* **Interface:** Integração via JavaScript para acesso nativo à Webcam no navegador.

---

## 📈 Performance e Resultados
O modelo demonstrou alta eficácia nos testes unitários:
* **Acurácia de Treinamento:** 100% após 10 épocas.
* **Tempo de Inferência:** Inferior a 150ms por frame.
* **Resultado Visual:** O sistema desenha retângulos dinâmicos (Green Boxes) com o nome do usuário e o nível de confiança (Confidence Score).

---

## ⚙️ Como Executar
1. Abra o arquivo `.ipynb` no Google Colab.
2. Ative a GPU em `Ambiente de Execução > Alterar tipo de ambiente`.
3. Execute as células de configuração e treinamento.
4. Utilize o bloco final para abrir sua câmera e testar o reconhecimento em tempo real.

---

## 👨‍💻 Autor
**Fred** Desenvolvedor focado em Machine Learning e Visão Computacional.

---
*Este projeto tem fins educacionais e demonstra habilidades em Deep Learning, Visão Computacional e integração de frameworks modernos de IA.*
