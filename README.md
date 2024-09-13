# Guia de Configuração do Terraform e NGINX na Azure 

Criei este repositório com a intenção de atender o desafio do curso Microsoft Azure - Localizando Serviços por Categoria

Este guia explica o processo de configuração de uma máquina virtual (MV) na Azure usando o Terraform e a instalação do NGINX.

# Pré-requisitos
Antes de começar, certifique-se de ter:

Conta na Azure.
Azure CLI instalada e configurada.
Terraform instalado.

# Passo 1: Configuração do Ambiente
Instalar o Terraform

Instalar o Azure CLI

# Passo 2: Configuração do Terraform
sobre o Arquivo main.tf

Certifique-se de preencher as informações necessárias, como nomes de recursos, localizações, e credenciais de acesso. Essas informações são essenciais para que o Terraform possa criar e configurar a infraestrutura corretamente.

Inicializar o Terraform

Navegue até o diretório onde está o main.tf e execute o seguinte comando para inicializar o Terraform:

terraform init

Prossiga com o comando:

terraform plan

Aplicar a Configuração

Para aplicar a configuração e criar a MV na Azure, execute:

terraform apply
Confirme a operação quando solicitado.

# Passo 3: Conectar à Máquina Virtual
Conecte-se à MV usando o IP obtido:

ssh adminuser@<IP_DA_MV>

# Passo 4: Instalar o NGINX
Atualizar o Sistema

Uma vez conectado à MV, atualize o sistema com:

sudo apt-get update
sudo apt-get upgrade

Instalar o NGINX

Instale o NGINX com o comando:

sudo apt-get install nginx

Verificar a Instalação

Verifique se o NGINX está funcionando acessando o IP da MV em um navegador web. Você deverá ver a página padrão do NGINX.

# Passo 5: Limpeza (Opcional)
Se desejar destruir a infraestrutura criada, execute:

terraform destroy
Confirme a operação quando solicitado.

