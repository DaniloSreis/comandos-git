# Comandos Git Essenciais

## Inicialização e Configuração

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git init` | Inicializa um novo repositório Git local | Cria a estrutura `.git` no diretório atual |
| `git remote add origin <URL>` | Conecta o repositório local a um repositório remoto | Substitua `<URL>` pelo endereço do repositório remoto |

## Gerenciamento de Alterações

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git add .` | Adiciona TODAS as alterações para a área de staging | Prepara tudo para commit |
| `git add <arquivo(s)>` | Adiciona arquivos específicos para a área de staging | Pode especificar múltiplos arquivos |
| `git commit -m "mensagem"` | Registra as alterações no histórico com uma mensagem descritiva | Mensagens claras são essenciais |
| `git commit --amend -m "nova mensagem"` | Altera a mensagem do último commit | Use apenas antes de fazer push |
| `git restore <arquivo>` | Descarta alterações não commitadas de um arquivo | Retorna ao estado do último commit |

## Histórico e Versionamento

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git reset --soft <hash>` | Retorna a um commit anterior, mantendo alterações em staging | Ideal para reescrever commits |
| `git reset --mixed <hash>` | Retorna a um commit anterior, mantendo alterações no working directory | Padrão do comando reset |
| `git reset --hard <hash>` | Retorna a um commit anterior, DESCARTANDO TODAS as alterações | Use com cautela - alterações são perdidas |
| `git reset <arquivo>` ou `git restore --staged <arquivo>` | Remove arquivo da área de staging | Mantém as alterações no working directory |

## Trabalho Remoto

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git push -u origin <branch>` | Envia commits e configura upstream para a branch | -u define a branch remota padrão |
| `git push` | Envia commits para o repositório remoto padrão | Usa após configurar upstream |
| `git push origin <branch>` | Envia commits para uma branch específica no remoto | |
| `git pull` | Obtém alterações do remoto e faz merge automaticamente | Equivalente a `git fetch` + `git merge` |

## Status e Informação

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git status` | Mostra o estado atual: alterações, arquivos staged, etc | Comando de diagnóstico essencial |
| `git log` | Exibe o histórico de commits | Use `--oneline` para versão compacta |

## Gerenciamento de Branches

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git checkout -b <branch>` | Cria uma nova branch e muda para ela | Atalho para branch + checkout |
| `git checkout <branch>` | Muda para a branch especificada | |
| `git branch -v` | Lista todas as branches locais com último commit | |
| `git merge <branch>` | Incorpora alterações da branch especificada na branch atual | Normalmente usado na main/master |
| `git branch -d <branch>` | Remove a branch local especificada | A branch deve estar mergeada |

## Clonagem

| Comando | Descrição | Observações |
|---------|-----------|-------------|
| `git clone <URL> --branch <branch> --single-branch` | Clona apenas uma branch específica do repositório | Reduz tempo e espaço em disco |