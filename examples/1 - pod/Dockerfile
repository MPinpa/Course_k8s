# Define a imagem base
FROM python:3.9

# Define a diretório de trabalho na imagem
WORKDIR /app

# Copia o arquivo de requirements para dentro da imagem
COPY requirements.txt .

# Instala as dependências do Python
RUN pip install --no-cache-dir -r requirements.txt

# Copia o restante dos arquivos da aplicação para dentro da imagem
COPY . .

# Define o comando para executar a aplicação quando a imagem for iniciada
CMD ["python", "app.py"]

# Expõe a porta 5000 na imagem
EXPOSE 80
