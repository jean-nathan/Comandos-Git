## 2. Inicializando o Git

**Cenário:** Você está iniciando um novo projeto e deseja utilizar o Git para gerenciar as alterações de código.

**Passo a passo:**
1. Navegue até o diretório do seu projeto no terminal.
2. Execute o comando `git init` para iniciar um repositório Git no diretório.

## 3. Gerenciando arquivos com Git

**Cenário:** Você fez algumas alterações em arquivos do seu projeto e deseja salvá-las no repositório Git.

**Passo a passo:**
1. Verifique o status dos arquivos com `git status` para ver quais foram modificados.
2. Adicione os arquivos que deseja salvar no próximo commit com `git add nomedoarquivo`.
3. Comite as alterações utilizando `git commit -m "mensagem do commit"` para salvar as alterações no histórico do Git.

## 5. Revertendo mudanças com checkout e reset

**Cenário 1:** Você fez algumas alterações em um arquivo, mas deseja desfazê-las e restaurar a versão anterior.

**Passo a passo:**
1. Verifique o histórico de commits com `git log` para encontrar o ID do commit anterior.
2. Utilize `git checkout IDdoCommit nomedoarquivo` para restaurar o arquivo para o estado do commit anterior.

**Cenário 2:** Você fez um commit e deseja desfazê-lo completamente.

**Passo a passo:**
1. Utilize `git log` para encontrar o ID do commit que deseja desfazer.
2. Execute `git reset IDdoCommit` para desfazer o commit, mantendo as alterações no diretório de trabalho.

## 6. Usando tags para marcar versões

**Cenário:** Você está lançando uma nova versão do seu software e deseja marcar essa versão no histórico do Git.

**Passo a passo:**
1. Execute `git tag -a v1.0 -m "Versão 1.0"` para criar uma tag para a nova versão.
2. Esta tag será anexada ao commit atual como uma marcação específica da versão.

## 7. Trabalhando com branches

**Cenário:** Você está desenvolvendo uma nova funcionalidade em seu projeto e deseja isolá-la do código principal.

**Passo a passo:**
1. Crie um novo branch para a funcionalidade com `git checkout -b nomedobranch`.
2. Desenvolva a funcionalidade no novo branch, fazendo commits conforme necessário.
3. Quando a funcionalidade estiver pronta para ser integrada ao código principal, mude de volta para o branch principal com `git checkout main` e faça o merge com `git merge nomedobranch`.

## 8. Enviando alterações para o repositório remoto

**Cenário:** Você fez algumas alterações significativas no código e deseja enviá-las para o repositório remoto.

**Passo a passo:**
1. Certifique-se de ter as alterações confirmadas localmente com `git commit`.
2. Execute `git push` para enviar as alterações para o servidor remoto.

## 9. Resolvendo conflitos

**Cenário:** Você e outro colaborador fizeram alterações conflitantes no mesmo arquivo.

**Passo a passo:**
1. Após fazer `git pull` para atualizar seu repositório local com as alterações do remoto, você identifica um conflito.
2. Edite o arquivo conflitante para resolver as diferenças manualmente.
3. Adicione as alterações ao commit com `git add` e faça o commit para resolver o conflito.

Esses são cenários comuns de uso dos comandos do Git.
