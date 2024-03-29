## Comandos Git
*git config --global user.name""*  
*git config --global user.email""*  
*git config --global core.editor* _nvim_/vim/vi/emacs  
*git config --list* -> verifica as configurações do repositorio  
**git init** -> inicializa o repositório  
*git status* -> reporta como está o status do repositório no momento  
*git add _(Arquivo)_* -> adicona ao git (unmodified/staged)  
*git commit* -> cria um snapshot  
*git commit -m _"Legenda"_* -> cria o commit para versionamento  
*git log* -> resumo do que aconteceu  
*git log --decorate* -> resumo do que aconteceu com mais detalhes  
*git log --author=_"(Nome do Autor)"_* -> log sobre determinado autor  
*git shortlog* -> resumo bem sintético  
*git shortlog -sn* -> mais sintético que o anterior  
*git log --graph* -> forma gráfica, quase como uma linha do tempo  
*git show _(hash)_* -> abre informações sobre determinado hash  
*git diff* -> olha as diferenças antes de realizar commit (Revisão)  
*git diff --name-only* -> mostra apenas o nome dos arquivos pre-commit  
*git checkout _(nome do arquivo)_* -> retorna o arquivo para última versão antes da edição (antes do commit)  
*git reset HEAD* -> volta o staged antes do commit  
_***depois usar o git checkout _(arquivo)_ para voltar ele para edição anterior***_  
*git reset --soft* -> pega as modificações, mata o commit mas mantém o arquivo em staged  
*git reset --mixed* -> (+)soft e volta as alterações do arquivo  
*git reset --hard* -> (+)mixed e mata o commit  
_**git reset --hard altera o histórico do commit**_  
## Gerando SSH
Abra o terminal, cole o texto abaixo e substitua por seu email:  
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"  
Será criado uma nava chave ssh  
Será pedido se deseja alterar endereço de onde a chave será salva, normalmente mantem o padrão  
Depois será pedido uma frase "secreta" e normalmente se deixar sem frase e pressiona enter  
Será salvao em ~/.ssh e o arquivo é id_rsa.pub  
cat id_rsa.pubdo  
Vá agora em Settings->SSH and GPG keys  
New SSH Key  
Cole o conteudo, identifique sua chave, salve digite a senha.  
## create a new repository on the command line (ssh)
echo "# github" )) README.md  
git init  
git add README.md  
git commit -m "first commit"  
git remote add origin git@github.com:(usuario)/(repositorio).git  
git push -u origin master  
## push an existing repository from the command line (ssh)##  
git remote add origin git@github.com:(usuario)/(repositorio).git  
git push -u origin master  
### Criando repositório manualmente i(https)  
git init  
git add README.md  
git commit -m "first commit"  
git remote add origin https://github.com/(usuario)/(repositorio).git  
git push -u origin master  
### push an existing repository from the command line (https)  
git remote add origin https://github.com/(usuario)/(repositorio).git  
git push -u origin master  
*git clone* -> clona o repositório, não aceita pull/requesties  
*git fork* -> (+)clone e permite pull/requesties  
*branch* -> é um ponteiro móvel que leva o commit  
___**pode modificar os arquivos sem alterar o local principal(master)  
facilmente desligável   
multiplas pessoas trabalhando em diferentes branchies  
evita conflitos de alterações**___  
*git checkout -b (nome)* -> o *-b* cria novo branch  
*git branch* -> mostra os branchies existentes  
*git checkout (nome do branch)* -> altera o branch atual para o desejado  
*git branch -D (nome do branch)* -> *-D* deleta o branch  
*git merge* -> operação não destrutiva, cira um novo commit com a junção de tudo  
*git rebase* -> evita commits extras; histórico linear  
*.gitignore* -> não trackeia alguns arquivs e pastas  
***Ver [github/gitignore](https://github.com/gitignore)***  
*git stash* -> gera uma imagem sem commit, util para trabalhos em execução
*alias* -> cria atalhos/apelidos para comandos git  
**git config --global alias.s status**  
*Versoes:*  
*git tag -a 1.0.0 -m "Conteudo da versão dos arquivos contidos"*  
*git push origin master --tags* -> ficam salvas como releases  
*git tag* -> mostra as tags  
*git revert (hash)* -> reverte o commit; apaga o que tinha feito; não perde o histórico do que foi feito, diferente do *reset --hard*  
*git tag -d (numero do tag)* -> apaga o tag local  
*git push origin:(numero)* -> apaga o tag remoto // serve para branch também  



