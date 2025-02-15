# backup-smb-googledrive
Comando para execução de backup sincronizado em agenda no Windows
<h2>Configuração</h2>
<p>Baixar os arquivos e configurara os diretorios de comandos no arquivo bakup_site.bat</p>

	robocopy -MIR \\IP_SERVIDOR_SMB\NOME_PASTA_COMPARTILHADA "G:\Meu Drive\NOME_PASTA_GDRIVER"
</br>
<p>Modificar a execução da loacalização do seu arquivo bakup_site.bat no arquivo exe.vbs</p>

	set objshell = wscript.createobject("wscript.shell")
 	objshell.run("C:\Scripts\backup_site.bat"),0, true
</br>
<p>Depois abar o "Agendador de Tarefas" do Windows e crie uma tarefa para rodar o arquivo exe.vbs</p>
