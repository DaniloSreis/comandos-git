# Comandos git

| Comando | Explicação |
|---------|------------|
| `git init` | Inicia um repositório git. |
| `git remote add origin link-do-repositório` | Conecta o repositório local com o remoto. |
| `git add .` | Adiciona todos os arquivos modificados para a área de commit. |
| `git add nome-do-arquivo nome-do-outro-arquivo` | Adiciona um arquivo ou arquivos específicos para a área de commit. |
| `git commit -m 'mensagem que explica as modificações feitas'` | Cria um commit. |
| `git commit --amend -m 'nova mensagem'` | Muda a mensagem de um commit (OBS: faça isso antes de um `git push`). |
| `git restore nome-do-arquivo` | Volta para o estado anterior do arquivo. |
| `git reset --soft hash-do-commit-que-você-quer-voltar` | Volta para um commit anterior, mantém as modificações feitas nos arquivos e deixa-os no staging area, prontos para serem commitados. |
| `git reset --mixed hash-do-commit-que-você-quer-voltar` | Volta para um commit anterior, mantém as modificações feitas nos arquivos e limpa o staging area, colocando-os no working directory. |
| `git reset --hard hash-do-commit-que-você-quer-voltar` | Volta para um commit anterior, tira as modificações feitas nos arquivos, remove-os do staging area e reverte as alterações feitas no working directory. |
| `git reset nome-do-arquivo` ou `git restore --staged nome-do-arquivo` | Tira o arquivo da staging area. |
| `git push -u origin nome-da-branch` | Envia as alterações locais do repositório Git para o repositório remoto, define o repositório remoto e a branch remota para a qual enviaremos as alterações. Depois disso, não precisamos mais identificar para o `git push` e `git pull` a branch para a qual queremos enviar ou buscar as modificações. |
| `git push` | Envia o commit para um repositório. |
| `git push origin nome-da-branch` | Envia o commit para uma branch específica do repositório. |
| `git status` | Mostra se há arquivos modificados, arquivos preparados para commit (staged) e arquivos não rastreados. |
| `git log` | Mostra o histórico de commits do repositório. |
| `git pull` | Verifica se há novos arquivos no repositório remoto e atualiza o seu repositório local, caso haja. |
| `git checkout -b nome-da-nova-branch` | Cria uma nova branch. |
| `git checkout nome-da-branch` | Troca de uma branch para outra. |
| `git branch -v` | Lista todas as branches locais e seu último commit. |
| `git merge nome-da-branch` | Junta a branch especificada à branch `main`. |
| `git branch -d nome-da-branch` | Deleta a branch especificada. |
| `git clone link-do-repositório --branch nome-da-branch --single-branch` | Clona apenas uma branch de um repositório remoto. |
