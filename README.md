
# Automatizando Tarefas Pico W

Adicionando linha de código no tasks.json e keybindings.json

- Tasks.json
  
        {
            "label": "Build UF2",
            "type": "shell",
            "command": "cmake -B build ; cmake --build build",
            "group": "build",
            "problemMatcher":[],
            "detail": "Compila o projeto e gera o .uf2"
        },
         {
            "label": "Upload UF2",
            "type": "shell",
            "command": "cp build/*.uf2 'D:\\'",
            "problemMatcher":[],
            "detail": "Copia o .uf2 gerado para o PICO W"
         }

- keybindings.json:
    
         Para acessa use ctrl+K e ctrl + s em seguida vá em Open keybindings shortcuts(json) <img src="Captura de tela 2025-07-29 002543.png" alt="Figurinha" width="100"/> e abrir o keybindings.json
        {
        "key": "shift+alt+b",
        "command": "workbench.action.tasks.runTask",
        "when": "Build UF2"
        },
        {
        "key": "shift+alt+c",
        "command": "workbench.action.tasks.runTask",
        "when": "Upload UF2"
        }


