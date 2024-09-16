# Usar uma imagem base com Python
FROM python:3.12.3-slim
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Definir o diretório de trabalho dentro do contêiner
WORKDIR /app

# Copiar os arquivos do diretório atual para o contêiner
COPY . /app

# Instalar as dependências
RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

# Configurar o contêiner para abrir um shell interativo por padrão
ENTRYPOINT ["/bin/bash"]
