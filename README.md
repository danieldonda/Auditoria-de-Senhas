# Auditoria de senhas do Active Directory
Para executar este script, é necessário que a pessoa tenha acesso a um ambiente com o Active Directory instalado e configurado

 - Módulo PowerShell DSInternals instalado 
 - Permissões suficientes para ler contas do Active Directory.

Definir as variáveis $servidor, $dominio, $dicionario e $HaveIBeenPwned de acordo com o ambiente em que está trabalhando. 

O arquivo de dicionário de senhas e o arquivo HaveIBeenPwned também devem ser baixados e colocados nos caminhos especificados nas variáveis $dicionario e $HaveIBeenPwned.
