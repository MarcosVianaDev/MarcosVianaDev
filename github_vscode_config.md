# Instalando e configurando o GitHub no VSCode no linux (Ubuntu)

1) Instale o git: `sudo apt install git`
2) Configure o login:
> * `git config --global user.email "you@example.com"`
> * `git config --global user.name "Your Name"`
3) Configurando o login automático:
> Fonte: https://medium.com/@andgomes/git-github-evitando-informar-usu%C3%A1rio-e-senha-a-cada-push-para-o-github-d8edbb5c6de4
> 1) Crie uma chave ssh: `ssh-keygen -t rsa -b 4096 -C "email_do_github"`, não precisa de senha.
> 2) Iniciamos o ssh-agent: `ssh-agent -s`
> 3) Adicionamos a chave: `ssh-add ~/.ssh/id_rsa`
> 4) Agora só precisamos adicionar a chave SSH à conta do GitHub. Para isso, faça login, clique na foto de perfil no canto superior direito e escolha a opção Settings. Na barra lateral da tela de configuração, clique em SSH and GPG keys.
> 5) Ao clicar em SSH key, escolha um título que represente o computador onde a chave está armazenada, copie todo o conteúdo do arquivo id_rsa.pub(armazenado no diretório /home/usuário/.ssh) e cole no campo Key.
> 6) Depois de clicar em Add SSH key, a chave será listada, com a opção de ser removida posteriormente.