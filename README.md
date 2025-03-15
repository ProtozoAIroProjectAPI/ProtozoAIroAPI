# ProtozoAIro

**ProtozoAIro** é uma API de classificação de imagens que identifica se uma célula está parasitada ou não pelo protozoário da malária. Desenvolvida em **Python** com **Flask**, **Keras** e **TensorFlow**, ela recebe uma imagem em formato **Base64** e retorna um resultado indicando a presença ou ausência de parasitas.

## ✨ Funcionalidades

- Receber uma imagem no formato **Base64**
- Classificar a imagem em **parasitada** ou **não parasitada**
- Retornar a probabilidade associada à classificação

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

## 📍 Licença

Este projeto está sob a licença **MIT**.
---

💡 **ProtozoAIro** - Facilitando o diagnóstico automatizado da malária! ⚕️

