FROM python:3.10-slim

# Define o diretório de trabalho
WORKDIR /app

EXPOSE 8000

COPY . .
# Copia os arquivos Pipfile e Pipfile.lock para o diretório de trabalho

# Instala o pipenv
RUN pip install pip --upgrade
RUN pip install pipenv

# Instala as dependências do projeto
RUN pipenv install --system --deploy

# Comando para executar a aplicação usando o Uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--reload"]

