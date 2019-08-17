## INSTALANDO E CONFIGURANDO O BROKER MQTT MOSQUITTO

  
<li>
<p>INSTALANDO O BROKER MQTT MOSQUITTO<br>

    sudo apt install mosquitto

    sudo apt intall mosquitto-clients
</li>

</li>
<p>CONFIGURANDO O BROKER MQTT MOSQUITTO<br>

    sudo nano /etc/mosquitto/mosquitto.conf
</li>

</li>
<p>DENTRO DESTE ARQUIVO, LOCALIZE E APAGUE A SEGUINTE LINHA:<br>
  
    include_dir /etc/mosquitto/conf.d
</li>

</li>
<p>APÓS ISTO, INCLUA ESTAS LINHAS:<br>
  
    allow_anonymous false
  
    password_file /etc/mosquitto/pwfile
  
    listener 1883
  Salve o arquivo pressionando CTRL + X, depois Spara salvar e Enterpara sair do editor de arquivos Nano
</li>

</li>
<p>CRIANDO USUARIO<br>
  
    sudo mosquitto_passwd -c /etc/mosquitto/pwfile nomesuario
##### Password : #cria a senha para o usuario
##### depois pede para o usuario repetir a senha novamente

    cat /etc/moquitto/pwfile
    
##### Conferir o arquivo do usuario 
##### Vai aparecer a senha criptografada 
</li>








