# versionamento de códigos - conteúdo resumidos das 4 aulas

Resumo de passo a passos úteis para o dia a dia de vocês! 
Prof Tabita e monitora Natalia

---

### COMO FAZER UM FORK:

Fork é como um sistema de cópia de repositório, porém com ligacão ao original. 
Abra o link do repositório, na parte superior dentro da aba code, clique no botão "fork":

![print-fork-1](https://github.com/user-attachments/assets/8928adde-03ac-429d-b0c7-f2224f2ca69f)

Isso irá te direcionar para um repositório dentro do seu perfil, que será seu, mas permanece ligado ao original para buscar atualizações e enviar Pull Requests.

![print-fork-3](https://github.com/user-attachments/assets/c1e5aa3a-9f16-4df3-8c9b-d7470f7f9613)

---

### COMO FAZER CLONE:

No repositório do github clique no botão "Code", escolha a aba local, e o metodo que preferir, usualmente utilizamos o HTTPS. 

![print-clone-1](https://github.com/user-attachments/assets/27efefa9-1d35-4e2e-a304-984a5c2d7338)

Para clonar, duas opções aqui: 
1. No Windows abrir a pasta em que deseja clonar pelo explorer e clicar com o botão direito e na opção "open git bash here".
2. No seu computador abra o git bash (windows) ou terminal (mac e linux) e navegue até o local onde deseja fazer o clone (cópia), você pode escrever **cd** e arrastar a pasta desejada para o terminal que ele pegará o endereço da pasta ou navegar atraves do comando **cd nome-da-pasta**
3. Clone: **git clone url-copiada**
4. Acesse a pasta clonada - **cd nome-da-pasta**. no caso do exemplo abaixo seria **cd cmp25-introducao-programacao-vc-II**.

![git-clone](https://github.com/user-attachments/assets/7c9783d9-2e6d-4b62-b2f6-851e35994be3)

---

### COMO CRIAR BRANCH:

Para versionar precisamos da criação de branchs para garantir a independência do código novo. 
A branch é um ramo/braço do código original que contem ele todo, porém que contem nosso código novo sem afetar a branch principal. 

No terminal: **git checkout -b "nome-da-branch"**

⚠️ importante ⚠️ as branchas não aceitam acento, nem espaço entre palavras. por convenção o nome pode seguir sendo a alteração nova - feature - que você esta fazendo. 
Exemplo, se troquei as informações de endereço e contato do meu site, a branch poderia ser - feat/troca_info_contato.
Isso depende de cada empresa ou de como o dev decide trabalhar se estiver sozinho em um projeto.

---

### COMO VERSIONAR:

Versionar é o processo de gerenciar e registrar alterações no código ao longo do tempo. Os passos acima fazem parte do processo de versionar, mas aqui no caso a gente vai colocar mais em ação o git em si! não a plataforma github.
Após executar suas alterações diárias faça um commit. Para isso o primeiro passo é adicionar as mudanças ao olhar do git, preparar para o commit, chamamos esse momento de "staging area", seria uma "área de preparação".

Usamos o comando: **git add .** ou **git add nome-do-arquivo.html**

Depois de preparar, nós fazemos o commit, que seria o momento de "repository" - momento que adicionamos a mudança ao repositório git local. Porque para efeitos práticos quando alteramos algo no computador sem fazer nada pelo git ele fica salvo só no computador. Ao fazer o **git add** e **git commit** estamos salvando na pasta que o git cria e registra as alterações. 

O comando de commit é: **git commit -m "atualiza informações de contato da empresa"** ⚠️ importante: na mensagem fale o que você alterou ou adicionou ao código em uma frase.

**linha de processo do git:**
pasta local/área de trabalho (working directory) -> área de preparação (staging area) -> repositório / commit (repository) 

Para enviar ao seu repositório externo no github
No terminal: **git push origin nome-da-branch**

---

### COMO ATUALIZAR REPOSITÓRIO

Vamos iniciar separando em dois passos, atualizar fork e atualizar apenas um repositório clonado diretamente, sem fork.

⚠️ sempre antes de puxar atualizações precisamos fazer um commit das alterações em andamento localmente! 

**Para repositório de Fork:**

Na primeira vez que formos puxar atualizações do repositório original do fork precisamo falar para nosso clone local que vamos pegar desse outro repositório. 

Usando o comando: **git remote -v** , podemos identificar o repositório principal que a nossa pasta local, clonada, esta conectada chamado "origin". 

Vamos adicionar o repositório original a essa lista. Ele será identificado como "upstream", que significa neste contexto que ele é de onde puxaremos atualizações externas. 

No terminal, dentro da pasta clonada: **git remote add upstream url-do-repositório-original**

Para puxar atualizações agora é só usar: **git pull upstream**

O pull ou fetch fazem a mesma função, de pedir as atualizações do respositório externo, porém com o git pull ele força um merge do que esta sendo chamado do repositório externo.

![upstream-add](https://github.com/user-attachments/assets/650b9459-19b8-4250-802e-d294bc64ef6e)
![upstream-pull](https://github.com/user-attachments/assets/5879fdb9-1e67-4813-9355-2f7f90a25298)

**Para um clone simples:**
No terminal: **git pull origin** ou **git pull origin nome-da-branch-externa**

---

### PROBLEMAS COM MERGE

Ao puxar atualizações podem haver conflitos de merge, para

---

### COMO FAZER PULL REQUEST EM FORK


