## 1. Inicializando o Git

**Cenário:** Você está iniciando um novo projeto e deseja utilizar o Git para gerenciar as alterações de código.

**Passo a passo:**
1. Navegue até o diretório do seu projeto usando o terminal.
2. Execute o comando `git init` para inicializar um repositório Git no diretório atual.

---

## 2. Gerenciando arquivos com Git

**Cenário:** Você fez alterações em arquivos do seu projeto e deseja salvá-las no repositório Git.

### Comandos para adicionar arquivos ao staging area:
1. **`git add .`**: Adiciona novos arquivos e alterações em arquivos existentes (não inclui arquivos excluídos).
2. **`git add -A`**: Adiciona tudo (novos arquivos, modificações e exclusões).
3. **`git add -u`**: Atualiza apenas mudanças em arquivos modificados e excluídos, sem incluir novos arquivos.
4. **`git add <arquivo ou diretório>`**: Adiciona um arquivo ou diretório específico ao staging area.

### Passo a passo:
1. Verifique o status dos arquivos modificados com `git status`.
2. Adicione os arquivos que deseja incluir no próximo commit com um dos comandos acima, dependendo do cenário.
3. Faça o commit das alterações utilizando `git commit -m "mensagem do commit"` para salvar as mudanças no histórico do Git.

---

## 3. Revertendo mudanças com `checkout` e `reset`

### Cenário 1: Desfazendo alterações não comitadas

**Cenário:** Você fez alterações em um arquivo, mas deseja restaurar a versão anterior sem comprometer essas mudanças no repositório.

**Passo a passo:**
1. Verifique o histórico de commits com `git log` para identificar o commit de interesse.
2. Use `git checkout IDdoCommit nomedoarquivo` para restaurar o arquivo para a versão daquele commit específico.

### Cenário 2: Desfazendo um commit

**Cenário:** Você cometeu mudanças, mas agora deseja desfazê-las completamente.

**Passo a passo:**
1. Execute `git log` para encontrar o ID do commit que deseja desfazer.
2. Utilize `git reset IDdoCommit` para desfazer o commit. As alterações serão mantidas no diretório de trabalho, mas o commit será removido do histórico.

---

## 4. Usando tags para marcar versões

**Cenário:** Você está lançando uma nova versão do software e deseja marcar esse ponto no histórico do Git.

**Passo a passo:**
1. Execute `git tag -a v1.0 -m "Versão 1.0"` para criar uma tag anotada para a nova versão.
2. A tag será vinculada ao commit atual, servindo como uma marcação específica para essa versão.

---

## 5. Trabalhando com branches

**Cenário:** Você está desenvolvendo uma nova funcionalidade e deseja isolá-la do código principal.

**Passo a passo:**
1. Crie um novo branch para a funcionalidade usando `git checkout -b nomedobranch`.
2. Desenvolva a funcionalidade no novo branch e faça commits conforme necessário.

### Integração da funcionalidade no branch principal:
- **Se você fizer `git merge` enquanto estiver na sua branch de funcionalidade**, as mudanças da `main` serão mescladas na sua branch de funcionalidade.
- **Se você fizer `git merge` estando na `main`**, as mudanças da sua branch de funcionalidade serão mescladas na `main`.

**Passo a passo para integrar na `main`:**
1. Volte para a branch principal com `git checkout main`.
2. Certifique-se de que a `main` está atualizada com o repositório remoto, executando `git pull`.
3. Depois, execute `git merge nomedobranch` para trazer as alterações da sua branch de funcionalidade para a `main`.

---

## 6. Enviando alterações para o repositório remoto

**Cenário:** Você fez alterações significativas no código e deseja enviá-las para o repositório remoto.

**Passo a passo:**
1. Certifique-se de que todas as alterações estão comitadas localmente usando `git commit`.
2. Execute `git push` para enviar as alterações para o repositório remoto.

---

## 7. Resolvendo conflitos

**Cenário:** Você e outro colaborador fizeram alterações conflitantes no mesmo arquivo.

**Passo a passo:**
1. Após fazer um `git pull` para trazer as últimas alterações do repositório remoto, você pode encontrar um conflito.
2. Edite manualmente o arquivo conflitante para resolver as diferenças entre as mudanças.
3. Depois de resolver o conflito, adicione o arquivo corrigido com `git add` e faça o commit das mudanças para finalizar a resolução do conflito.
