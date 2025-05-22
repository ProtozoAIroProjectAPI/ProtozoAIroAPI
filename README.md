# 🦟 ProtozoAIro

**ProtozoAIro** é uma API de classificação de imagens que identifica se uma célula está parasitada ou não pelo protozoário da malária. Desenvolvida em **Python** com **Flask**, **Keras** e **TensorFlow**, ela recebe uma imagem em formato **Base64** e retorna um resultado indicando a presença ou ausência de parasitas.

Para isso, foi treinada uma **rede neural convolucional (CNN) sequencial simples**, cujo modelo final foi salvo em dois arquivos: `network.json` (que armazena a estrutura da rede) e `weights.hdf5` (que contém os pesos aprendidos). A **API carrega esses arquivos ao iniciar e utiliza o modelo treinado** para realizar a classificação das imagens recebidas.



# 📁 Dataset Utilizado
O modelo foi treinado utilizando o dataset de células infectadas e não infectadas por malária disponível no [Kaggle](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria), contendo **27.500 imagens** divididas igualmente entre as classes **parasitada** e **não parasitada**. Os dados foram separados da seguinte forma:

- **Treinamento**: 70% dos dados  
- **Teste**: 30% dos dados


# 📊 Resultados do Modelo
- **Acurácia**: 95,78%

- **F1 Score**: 96,00%

- **Recall**: 96,00%

- **Precision**: 96,00%

## ✨ Funcionalidades

- Receber uma imagem no formato **Base64**
- Classificar a imagem em **parasitada** ou **não parasitada**
- Retornar a probabilidade associada à classificação


# 📐 Diagramas UML
- 📌 **Caso de Uso**: 
O diagrama de caso de uso ilustra as interações principais entre o usuário (cliente) e o sistema ProtozoAIro, incluindo o envio da imagem e o recebimento da classificação.
<p align="center">
  <img src="https://i.postimg.cc/2SmNbnfs/casodeusoprotozoairo.jpg" alt="Diagrama de Caso de Uso" width="400" height="300" />
</p>



- 📌 **Fluxo de Dados**: 
O diagrama de fluxo de dados detalha o caminho percorrido pelos dados desde o envio da imagem até o retorno da resposta com a classificação final.

<p align="center">
  <img src="https://i.postimg.cc/Kztd8YHG/Diagrama-Fluxo.png" alt="Diagrama de Fluxo de Dados" width="400" height="300">
</p>



## 👤 Requisitos

Certifique-se de ter instalado:

- Python 3.10+
- Flask
- TensorFlow
- Keras

Para instalar as dependências:

```bash
pip install -r requirements.txt
```


## 🚶‍♂️ Executando a API

1. Clone o repositório:

```bash
git clone https://github.com/ProtozoAIroProjectAPI/ProtozoAIroAPI.git
```

2. Execute a API:

```bash
python app.py
```

A API será iniciada em `http://localhost:5000`.

## 🔍 Endpoints

### 1. **Classificar Imagem**

**POST** `/predict`

**Requisição:**

```json
{
  "image": "<imagem_em_base64>"
}
```

**Resposta de Sucesso:**

```json
{
  "predict": "parasitada"
}
```
**ou**

```json
{
  "predict": "não parasitada"
}
```

**Resposta de Erro:**

```json
{
  "error": "Nenhuma imagem fornecida"
}
```

## 🌐 Usando a API em Produção

Você pode acessar a API em funcionamento sem precisar configurar nada:

```bash
https://protozoairoapi.up.railway.app/predict
```

## 📊 Melhorias Futuras
- Implementar autenticação via token
- Utilizar um servidor com maior capacidade de processamento.

---

💡 **ProtozoAIro** - Pensou em malária, pensou em ProtozoAIro! ⚕️

