# Exercício Guiado - Introdução ao Git e GitHub

## Programação Orientada a Dados

## Parte 1: Configuração Inicial do Git

```
Para poder utilizar o Git com integração ao GitHub, existem alguns detalhes que
precisamos configurar. Vamos seguir os passos abaixo para garantir que tudo esteja
funcionando corretamente.
```
1. **Instalando o Git:**
    Verifique se o Git está instalado na sua máquina.
    Abra o terminal e digite:

```
git --version
```
```
Se o Git não estiver instalado, siga as instruções de instalação de acordo com o seu
sistema operacional, conforme apresentado no final dos slides da última aula.
```
2. **Configuração do Git com GitHub:**
    Configure seu nome de usuário e email (estes devem ser os mesmos usados no
    GitHub para que a integração seja feita com sucesso).

```
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
3. **Gerando e Configurando a Chave SSH (Opcional):**
    Atualmente, o GitHub recomenda o uso de chaves SSH para autenticação, como
    uma forma de incrementar a seguraça do acesso aos repositórios.
    São duas as alternativas possíveis para autenticação: usar um token de acesso
    pessoal ou gerar uma chave SSH.
    Usando SSH:
       Gere uma chave SSH para conectar-se ao GitHub sem precisar digitar um
       token a cada push/pull.


## Parte 2: Criando e Clonando um Repositório

## Parte 3: Trabalhando com Git

```
ssh-keygen -t rsa -b 4096 -C "seuemail@example.com"
```
```
Adicione a chave SSH ao seu agente SSH:
```
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```
```
Copie a chave pública gerada e adicione ao seu perfil no GitHub.
Obtenha a chave pública usando o comando
```
```
cat ~/.ssh/id_rsa.pub
```
```
Usando Token de Acesso Pessoal:
Crie um token de acesso pessoal no GitHub e use-o para autenticar suas
operações no lugar da senha exigida na hora de interagir com o GitHub.
```
1. **Criando um Repositório no GitHub:**
    No GitHub, crie um novo repositório com o nome aula-pod.
    Escolha a opção de inicializar o repositório com um arquivo README.md.
2. **Clonando o Repositório:**
    No terminal, navegue até o diretório onde deseja armazenar o repositório localmente.
    Clone o repositório usando o comando:

```
git clone git@github.com:seuusuario/aula-pod.git
```
```
Navegue para dentro da pasta do repositório clonado:
```
```
cd aula-pod
```
1. **Verificando o Status do Repositório:**
    Crie um novo arquivo exemplo.txt e adicione algum conteúdo nele.


## Parte 4: Trabalhando com Branches

```
Verifique o status do repositório para ver quais arquivos foram modificados:
```
```
git status
```
2. **Adicionando Arquivos ao Controle de Versão:**
    Adicione o arquivo exemplo.txt para a Staging Area, preparando-o para ser
    comitado:

```
git add exemplo.txt
```
3. **Comitando as Mudanças:**
    Comite as mudanças, adicionando uma mensagem descritiva:

```
git commit -m "Adiciona arquivo de exemplo"
```
4. **Visualizando o Histórico de Commits:**
    Veja o histórico de commits do repositório:

```
git log
```
5. **Enviando as Mudanças para o GitHub:**
    Envie suas mudanças para o repositório remoto no GitHub:

```
git push origin main
```
```
O comando funciona ao colocarmos git push seguido de para onde iremos enviar
a branch atualizada origin e qual a branch que enviaremos main.
```
6. Vale lembrar, os comandos status e log são comandos que não alteram o status do
    repositório, sendo apenas informativos. Utilize sempre que achar necessário!
1. **Criando uma Nova Branch:**
    Crie uma nova branch chamada nova-funcionalidade:

```
git branch nova-funcionalidade
```

## Parte 5: Sincronizando com o Repositório Remoto

```
Liste todas as branches do repositório:
```
```
git branch
```
```
A nova branch será criada, mas você ainda estará na branch principal.
```
2. **Mudando para a Nova Branch:**
    Troque para a nova branch:

```
git checkout nova-funcionalidade
```
```
Verifique se você está na nova branch:
```
```
git branch
```
```
Agora, você pode começar a fazer modificações na nova branch sem afetar a branch
principal.
```
3. **Fazendo Modificações na Nova Branch:**
    Modifique o arquivo exemplo.txt ou crie um novo arquivo.
    Adicione e comite as mudanças:

```
git add.
git commit -m "Adiciona mudanças na nova branch"
```
```
Observe que foi utilizado o comando git add. para adicionar todas as mudanças
ao commit, ao invés de adicionar os arquivos especificamente.
Verifique o histórico de commits da nova branch:
```
```
git log
```
4. **Enviando a Nova Branch para o GitHub:**
    Envie a nova branch para o repositório remoto:

```
git push origin nova-funcionalidade
```

1. **Puxando Mudanças do Repositório Remoto:**
    Antes de fazer novas modificações, sempre é bom garantir que seu repositório local
    está atualizado:

```
git pull origin main
```
2. **Voltando para a Branch Principal:**
    Mude para a branch main:

```
git checkout main
```
3. **Integrando a Nova Branch na Principal:**
    Faça o merge da branch nova-funcionalidade na branch main:

```
git merge nova-funcionalidade
```
4. **Enviando as Alterações para o Repositório Remoto:**

```
Envie as alterações integradas para o GitHub:
```
```
git push origin main
```
5. **Deletando a Nova Branch:**
    Após integrar a nova funcionalidade na branch principal, você pode deletar a branch
       nova-funcionalidade:

```
git branch -d nova-funcionalidade
```

Autor: ##### Prof. Otávio Parraga

