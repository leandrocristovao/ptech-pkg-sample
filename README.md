# ptech_pkg_sample 📦

ptech_pkg_sample é um pacote Django que oferece funcionalidades para gerenciamento de configurações usando o modelo `Setting`.

Este pacote tem objetivo de apresentar o básico para a criação de um pacote reutilizável em DJANGO

## 📌 Requisitos

- Python 3.8+
- Django 5.0+

## ⚙️ Instalação

Clone o repositório e instale as dependências necessárias:

    git clone https://github.com/leandrocristovao/ptech_pkg_sample.git
    cd ptech_pkg_sample
    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt

Para instalar em um projeto existente:

    pip install git+https://github.com/leandrocristovao/ptech_pkg_sample.git

No seu projeto Django, abra o arquivo settings.py e adicione:

    INSTALLED_APPS = [
        ...
        "ptech_pkg_sample",
    ]
    
Aplique as migrações

    python manage.py migrate ptech_pkg_sample

Se houver problemas de migração, tente:

    python manage.py makemigrations ptech_pkg_sample
    python manage.py migrate

## 🚀 Importar e Usar no Código

Agora você pode importar os modelos e funcionalidades do pacote normalmente.
Por exemplo, se o pacote define o model Setting:

    from ptech_pkg_sample.models import Setting

    config = Setting.objects.create(key="modo_escuro", value="ativo")
    print(config)

## 🚀 Manter o Pacote Atualizado

Se houver atualizações no repositório, atualize o pacote com:

    pip install --upgrade git+https://github.com/leandrocristovao/ptech_pkg_sample.git

## ✅ Como Executar os Testes

    pytest

