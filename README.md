# Debugger Visual Code 

 - PHP IN VSCODE
 - NODE IN VSCODE

 ## PHP
 
 1 - Colar a extenssão do xdebuge no arquivo na pasta ext do php no xampp
 
1.1 - https://xdebug.org/wizard baixar dll.

2 - Colar as sequintes configurações no arquivo php.ini

	[XDebug]
	xdebug.remote_enable = 1
	xdebug.remote_autostart = 1
	zend_extension = 'C:\xampp\php\ext\php_xdebug-2.5.5-5.6-vc11-x86_64.dll'


3 - Instalar a extenssão PHP Debug

4 - Apontar, em settings do Visual Code no campo executablePath o arquivo php.exe do xampp 

	"php.validate.run": "onType",
	"php.validate.executablePath": "C:\\xampp\\php\\php.exe"
 
5 - Criar o arquivo lancher.json do Visual Code, disponível no campo de deputação (Icone Aranha).  

5.1 - Colar esses dados no script.
        
            // Use IntelliSense to learn about possible attributes.
            // Hover to view descriptions of existing attributes.
            // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
            "version": "0.2.0",
            "configurations": [
                {
                    "name": "Listen for Xdebug",
                    "type": "php",
                    "request": "launch",
                    "port": 9000
                },
                {
                    "name": "Launch currently open script",
                    "type": "php",
                    "request": "launch",
                    "program": "${file}",
                    "cwd": "${fileDirname}",
                    "port": 9000
                }
            ]
        
6 - Reiniciar o apache

7 - Reiniciar o Visual Code

8 - Marcar o breakpoint e utilizar e ativar o debug.

9 - Realizar a chamda da função. 

<hr>

## Node.js

1 - Criar o arquivo lancher.json do Visual Code, disponível no campo de deputação (Icone Aranha).  
2 - Colar as sequintes configurações. 

    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "pwa-node",
            "request": "attach",
            "protocol": "inspector",
            "restart": true,
            "name": "Launch Program",
            "skipFiles": [
                "<node_internals>/**"
            ],
        }
    ]


3 - Criar o arquivo nodemon.json na raiz do projeto e colar as sequintes configurações: 

    "execMap": {
        "js" : "node --inspect"
    }



4 - Reiniciar servidor node

5 - Utilizar marcar breakpoint e realizar a deputação.

