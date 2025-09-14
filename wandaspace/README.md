# 🔊 Classificação de Sons de Motores com Machine Learning

Este projeto tem como objetivo **classificar áudios de motores em funcionamento normal e motores com falhas** utilizando técnicas de aprendizado de máquina em Python.  
A análise é feita a partir da extração de **features de áudio** (MFCCs, ZCR e Centróide Espectral) e o modelo de classificação escolhido foi o **Random Forest**.

---

## 📂 Estrutura do Projeto

classificacao-audio-motores-automotivos/
│
├── audios/ # Contém os arquivos de áudio utilizados nos testes
├── notebooks/ # Jupyter Notebooks com código e experimentos
│ └── script.ipynb
├── .gitignore # Arquivo para ignorar arquivos/pastas no Git
└── README.md # Documentação principal do projeto


---

## ⚙️ Tecnologias Utilizadas
- [Python 3](https://www.python.org/)
- [Librosa](https://librosa.org/) → extração de características de áudio
- [Scikit-learn](https://scikit-learn.org/) → treinamento e avaliação do modelo
- [Matplotlib](https://matplotlib.org/) → visualização dos resultados
- [NumPy](https://numpy.org/) → manipulação numérica

---

## 🛠️ Metodologia
1. **Pré-processamento**: carregamento de 537 áudios (179 normais e 358 com falhas nos cilindros P1 e P4).  
2. **Extração de features**: aplicação de MFCCs, ZCR e Centróide Espectral, com cálculo da média e concatenação.  
3. **Divisão dos dados**: 80% para treino e 20% para teste usando `train_test_split`.  
4. **Treinamento**: modelo Random Forest com 100 árvores (`n_estimators=100`).  
5. **Avaliação**: cálculo da acurácia, relatório de classificação e visualização PCA.

---

## 📊 Resultados
- O modelo conseguiu diferenciar sons normais de falhos com boa taxa de acerto.  
- Foi gerado um **gráfico PCA** mostrando a separação das classes em duas dimensões.  

---

## 🚀 Como Executar
1. Clone este repositório:
   ```bash
   git clone https://github.com/ValeriaSilvaSantos1/classificacao-audio-motores-automotivos.git
   cd classificacao-audio-motores-automotivos

2. Crie um ambiente virtual e ative-o:
    python -m venv venv
    source venv/bin/activate   # Linux/Mac
    venv\Scripts\activate      # Windows

3. Instale as dependências necessárias:
    pip install numpy librosa scikit-learn matplotlib

4. Execute o notebook:
    jupyter notebook notebooks/script.ipynb

ou abra o arquivo script.ipynb diretamente na IDE de sua preferência.


