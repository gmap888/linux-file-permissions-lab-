# 🔐 Gerenciamento de Permissões de Arquivos no Linux 🐧

Este projeto simula um cenário real de **gestão de permissões de arquivos e diretórios no Linux**, com foco em **segurança da informação, controle de acesso e proteção de dados sensíveis**. Foi realizado como parte de um laboratório de Cibersegurança, voltado para práticas operacionais em ambientes Linux.

## 📚 Descrição do Projeto
Durante este projeto, utilizei comandos do Linux para verificar, interpretar e modificar permissões de arquivos e diretórios, garantindo que apenas usuários autorizados tivessem acesso de leitura, escrita ou execução. O laboratório reflete situações reais do mercado, em que profissionais de segurança precisam proteger arquivos confidenciais e limitar o acesso conforme as políticas da organização.

## 🛠️ Comandos Utilizados

### 🔍 Verificar permissões (incluindo arquivos ocultos):
```bash
ls -la
```

### 🔧 Alterar permissões de arquivos:
- Para o arquivo oculto `.project_x.txt`, garantindo que apenas o usuário e o grupo possam **ler**, sem permissão de escrita para ninguém:
```bash
chmod u=r,g=r,o= .project_x.txt
```

- Para o arquivo `project_k.txt`, removendo permissão de **gravação** do grupo e de outros:
```bash
chmod g-w,o-w project_k.txt
```

### 📂 Alterar permissões de diretórios:
- Para o diretório `drafts`, garantindo que **somente o usuário** possa acessar, ler, gravar e executar, bloqueando totalmente o grupo e outros:
```bash
chmod 700 drafts
```

## 📜 Resultados Obtidos
Após aplicar os comandos, os arquivos e diretórios ficaram com as seguintes permissões:
- `.project_x.txt` → `-r--r-----`
- `project_k.txt` → `-rw-r--r--`
- `drafts` (diretório) → `drwx------`

## 📸 Capturas de Tela
As capturas de tela dos comandos executados e seus resultados estão na pasta `/capturas_de_tela`.

## 🔒 Objetivo
Demonstrar habilidades práticas em:
- Gerenciamento de permissões no Linux
- Controle de acesso a arquivos e diretórios
- Aplicação de boas práticas de segurança da informação
- Operações em linha de comando (CLI)

## 🏁 Conclusão
Este projeto reforça conhecimentos fundamentais para atuação em funções como **SOC Analyst, Cybersecurity Analyst, Blue Team, SysAdmin, Cloud Security,** entre outras áreas de segurança da informação.

---
