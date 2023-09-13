# Ambiente Virtual com Python - Microsoft Learn

Passoa passo de como criar um ambiente virtual com python, para trabalhar com instalações e pacotes apenas em um escopo de um software, evitando o conflito de versões entre o projeto e a máquina.

## Passo a passo

### Criar um ambiente virtual

1. Execute venv env, para criar um ambiente virtual chamado env:

    ```cmd
    python -m venv env
    ```

    ou

    ```cmd
    py -m venv env
    ```

    Será criado um novo diretório chamado env para alocar o ambiente virtual.

2. Para ativar o ambiente virtual, execute o seguinte comando no Windows:

    ```cmd
    C:\ .. \env\Scripts\activate
    ```

    ou

    ```cmd
    .\env\Scripts\activate
    ```

3. Instalar dependência (exemplo dateutil):

    ```cmd
    pip install python-dateutil
    ```

3. Verificar dependências:

    ```cmd
    pip freeze
    ```

### Instalar dependências para um projeto importado

1. Verifique se o projeto possui o arquivo requirements.txt.

    Exemplo:

    ```
    src/
        app.py
        requirements.txt
    ```

2. Execute pip install para instalar bibliotecas especificadas em requirements.txt:

    ```
    pip install -r requirements.txt
    ```

### Atualizar um pacote

Execute pip install --upgrade no projeto:

Exemplo de pacote anterior instalado: python-dateutil==2.7.4

    ```
    pip install "python-dateutil==2.7.*" --upgrade
    ```