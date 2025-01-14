# Rede YOLOv3 detecção de objetos

Este repositório contém a implementação de um modelo para a Detecção de Objetos 
utilizando Transfer Learning de uma rede YOLOv3 (You Only Look Once), 
que é uma arquitetura para detecção de objetos em tempo real. 
Após ser treinado um modelo YOLO é capaz de detectar objetos personalizados em imagens, 
como "cavalo","carro","mochila" e outros, usando a framework Darknet.


### Requisitos

- Google Colab
- Darknet (repositório oficial de YOLO)

### Como usar

1. **Clonar o Repositório**

   Clone o repositório para o seu ambiente local ou para o Google Colab:

   ```bash
   git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   ```
   
2. **Compile o Framework**

   Acesse o repositório e faça a compilação do framework Darknet:

   ```bash
   %cd darknet
   !make
   ```
   
3. **Download dos pesos**

   Baixe os pesos pré-treinados para o modelo:

   ```bash
   !wget https://pjreddie.com/media/files/yolov3.weights
   ```

4. **Detecte objetos**

   Selecione imagens para detectar os objetos presentes na cena:

   ```bash
   !./darknet detect cfg/yolov3.cfg yolov3.weights data/[imagem].jpg
   ```
4. **Visualize o resultado**

   A imagem que contem o resultado da detecção encontra-se em:

   ```bash
   /darknet/predictions.jpg
   ```
