# Auditoria de senhas do Active Directory

O script é utilizado para testar a qualidade das senhas de contas do Active Directory. Ele oferece três opções:

 - Testar a qualidade das senhas no Active Directory - esta opção testa a qualidade das senhas de todas as contas do Active Directory no servidor e domínio especificados. O teste é realizado sem o uso de dicionários ou arquivos de senhas vazadas.
 - Testar a qualidade das senhas no Active Directory usando dicionários - esta opção testa a qualidade das senhas de todas as contas do Active Directory no servidor e domínio especificados, mas usa um arquivo de dicionário de senhas para verificar a qualidade das senhas. Se uma senha for encontrada no dicionário, ela será considerada fraca.
 - Testar a qualidade das senhas no Active Directory usando HaveIBeenPwned - esta opção testa a qualidade das senhas de todas as contas do Active Directory no servidor e domínio especificados, mas usa um arquivo de senhas vazadas de HaveIBeenPwned para verificar a qualidade das senhas. Se uma senha for encontrada no arquivo de senhas vazadas, ela será considerada fraca.

O script utiliza o módulo DSInternals do PowerShell para realizar a verificação da qualidade das senhas, o que permite que o teste seja realizado mesmo em contas em que o valor de senha não esteja armazenado no Active Directory (por exemplo, contas de computador). O script exibe um menu de opções para que o usuário escolha qual opção deseja executar e, em seguida, executa o código correspondente à opção escolhida.

# Como usar o script 
Para executar este script, é necessário que a pessoa tenha acesso a um ambiente com o Active Directory instalado e configurado

 - Módulo PowerShell DSInternals instalado 
 - Permissões suficientes para ler contas do Active Directory.

Definir as variáveis $servidor, $dominio, $dicionario e $HaveIBeenPwned de acordo com o ambiente em que está trabalhando. 

O arquivo de dicionário de senhas e o arquivo HaveIBeenPwned também devem ser baixados e colocados nos caminhos especificados nas variáveis $dicionario e $HaveIBeenPwned.

Acesse https://haveibeenpwned.com/Passwords e faça o download da lista de senhas versão NTLM	Version 8 (ordered by hash)
