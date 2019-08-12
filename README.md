git config --global user.name""
git config --global user.email""
git config --global core.editor nvim/vim/vi/emacs
git config --list -> verifica as configurações do repositorio
git init -> inicializa o repositório
git status -> reporta como está o status do repositório no momento
git add <Arquivo> -> adicona ao git (unmodified/staged)
git commit -> cria um snapshot
git commit -m "Legenda" -> cria o commit para versionamento
git log -> resumo do que aconteceu
git log --decorate -> resumo do que aconteceu com mais detalhes
git log --author="<Nome do Autor>" -> log sobre determinado autor
git shortlog -> resumo bem sintético
git shortlog -sn -> mais sintético que o anterior
git log --graph -> forma gráfica, quase como uma linha do tempo
git show <hash> -> abre informações sobre determinado hash
git diff -> olha as diferenças antes de realizar commit (Revisão)
git diff --name-only -> mostra apenas o nome dos arquivos pre-commit
