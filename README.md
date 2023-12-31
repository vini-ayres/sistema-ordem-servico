# Sistema de Ordem de Serviço (SOS) - IFSP Campus Cubatão

## Visão Geral

O Sistema de Ordem de Serviço (SOS) do IFSP Campus Cubatão é uma plataforma abrangente projetada para gerenciar eficientemente as solicitações de serviços dentro da instituição. Esta documentação integra a descrição geral do projeto com os requisitos e instruções específicas para a implementação usando o framework Laravel.

### Requisitos do Sistema (Laravel)

Para garantir uma implementação bem-sucedida do Sistema de Ordem de Serviço, certifique-se de que seu ambiente atenda aos seguintes requisitos:

- IDE: É recomendado a instalação de uma IDE, preferencialmente Visual Studio Code, para a execução do projeto.
- PHP: Versão 7.4 ou superior;
- XAMPP: É obrigatório que os módulos do Apache e do MySQL sejam instalados;
- Composer: Ferramenta de gerenciamento de dependências para PHP;
- Banco de Dados: Deverá ser utilizado o arquivo "db_ordem_servico.sql" para a implementação do banco.

### Download dos Arquivos Necessários para o Projeto
[Link para download dos arquivos](https://drive.google.com/drive/u/0/folders/1VWuVeIlOkSq6Cskq3Jz5pigge4yVc6LZ)

### Instalação do Projeto Laravel

**1. Instalar o Composer:**

Antes de instalar o Composer, é obrigatório que você já tenha instalado o XAMPP em seu computador. Após ter instalado o XAMPP, execute os seguintes comandos em seu terminal:

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e21205b207c3ff031906575712edab6f13eb0b361f2085f1f1237b7126d785e826a450292b6cfd1d64d92e6563bbde02') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

**2. Clonar o Repositório:**

Abra um terminal na sua IDE e execute os seguintes comandos:

```bash
git clone https://github.com/vini-ayres/sistema-ordem-servico.git
cd sistema-ordem-servico
```

**3. Instalar Dependências do Composer:**

Execute o seguinte comando para instalar as dependências do projeto:

```bash
composer install
```

**4. Configurar Variáveis de Ambiente:**

Abra o arquivo `.laravel.env` em um editor de texto e configure as variáveis de ambiente, incluindo informações do banco de dados, de acordo com a configuração do ambiente XAMPP.

```env
APP_URL=http://localhost # Endereço principal do sistema
DB_CONNECTION=mysql # Nome do SGBD utilizado no sistema
DB_HOST=127.0.0.1 # Endereço IP do servidor do banco de dados
DB_PORT=3306 # Altere para a porta do MySQL no seu ambiente XAMPP
DB_DATABASE=db_ordem_servico # Nome do banco do sistema
DB_USERNAME=root # Nome de usuário para acesso ao banco
DB_PASSWORD=(deixe em branco) # Senha do usuário
```

**5. Ligar os módulos do XAMPP:**

Ligue somente os módulos de Apache e MySQL através do botão "Start" para iniciar o servidor do sistema Laravel.
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/0dceb050-5c65-4b47-a5a2-56a709ebda85)
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/6fa039d1-37e7-4792-b5b0-64e0282b5de4)

**6. Implementação do banco de dados no MySQL:**

Na tela do XAMPP, clique em "Admin" no módulo do MySQL. Em seguida, abrirá uma nova aba no seu navegador com a tela do phpMyAdmin. No campo de usuário, escreva "root" e deixe o campo de senha em branco, e em seguida, clique em "Entrar"
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/3a8c2b9a-eb24-4748-96ba-e770c34c1604)
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/3ea9f948-a63a-4926-b471-731d5b8cc522)
<br><br>
Após logar no phpMyAdmin, clique em "Novo" para criar uma nova base de dados
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/a459f505-7ba4-457c-a74d-f5ba0362d37b)
<br><br>
No campo de nome, escreva "db_ordem_servico" e depois clique em "Criar"
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/ada086db-c779-4b43-a56b-75f98cc5b47d)
<br><br>
Depois de criado sua base de dados, clique em "Importar" para importar seus dados do arquivo "db_ordem_servico.sql".

Lembrando, é necessário tê-lo baixado em seu computador, caso ainda não tenha baixado, faça o download do arquivo neste link: [Link para download dos arquivos](https://drive.google.com/drive/u/0/folders/1VWuVeIlOkSq6Cskq3Jz5pigge4yVc6LZ)
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/ea2f8489-d31d-49ca-be06-e22c4be3b1bc)
<br><br>
Em "Escolher arquivo", selecione o arquivo "db_ordem_servico.sql" já baixado em seu computador, em seguida, role a página para baixo e clique em "Importar". Verifique se o formato está em SQL antes de importar o arquivo.
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/457153be-53af-46b6-9809-c371e1d9633f)
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/62eeb9be-d619-43fc-98c3-9a45911448ff)
<br><br>
Depois de importado, sua base de dados já estará pronta para ser utilizada no Laravel.
<br><br>
![image](https://github.com/vini-ayres/sistema-ordem-servico/assets/131456406/cdfe78ba-ae2d-4add-8365-2b01ce949b4f)

**7. Iniciar o Servidor de Desenvolvimento:**

Para isso, é necessário que primeiramente você esteja no diretório correto da pasta, portanto digite o seguinte comando no terminal para garantir que esteja no caminho correto da pasta do seu projeto:

```bash
cd sistema-ordem-servico
```
Por fim, execute o seguinte comando no seu terminal para iniciar o servidor Laravel:

```bash
php artisan serve
```

Em seguida, acesse o sistema no navegador usando o endereço fornecido pelo comando acima. E assim seu sistema de Ordem de Serviço está pronto para o uso.

---

**Nota:** Certifique-se de ter seguido todos os passos corretamente para garantir uma instalação bem-sucedida do Sistema de Ordem de Serviço.
