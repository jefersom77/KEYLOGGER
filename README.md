# 🛡️ Laboratório de Cibersegurança: Keylogger & Ransomware em Python

Este projeto foi desenvolvido como parte de um desafio prático de Cibersegurança. O objetivo é simular o funcionamento de ameaças digitais (malwares) em um ambiente 100% controlado e educacional, focado no entendimento técnico para fins de defesa e mitigação.

---

## ⌨️ Projeto 1: Keylogger Remoto
Simulação de uma ferramenta de monitoramento de entradas de teclado com exfiltração de dados via e-mail.

### 🚀 Funcionalidades
*   **Captura em tempo real:** Monitoramento de todas as teclas pressionadas.
*   **Tratamento de Teclas:** Identificação de teclas especiais (Enter, Espaço, Backspace) e exclusão de modificadores (Shift, Alt, Ctrl).
*   **Envio Periódico:** Uso de `threading` para enviar os logs por e-mail a cada 60 segundos sem travar a execução.
*   **Segurança de Credenciais:** Uso da biblioteca `python-dotenv` para proteger e-mail e senha em arquivos `.env`.

### 🛠️ Tecnologias e Bibliotecas
*   **Python 3.x**
*   **Pynput:** Captura de eventos de hardware.
*   **Smtplib & Email.mime:** Comunicação com servidores SMTP (Gmail).
*   **Threading:** Execução de tarefas em segundo plano.

---

## 🔒 Projeto 2: Ransomware Simulado
Simulação de um sequestro de dados utilizando criptografia de ponta para demonstrar como arquivos são "trancados".

### 🚀 Funcionalidades
*   **Criptografia AES:** Uso da biblioteca `cryptography` (Fernet) para embaralhar arquivos `.txt`.
*   **Geração de Chave:** Criação de uma chave única (`chave.key`) necessária para a recuperação.
*   **Nota de Resgate:** Geração automática de um arquivo `RESGATE.txt` após a infecção.
*   **Descriptografia:** Script dedicado para restaurar os arquivos originais com a chave correta.

### 🛠️ Tecnologias e Bibliotecas
*   **Cryptography:** Implementação de algoritmos de segurança.
*   **OS:** Manipulação de caminhos e diretórios do sistema.

---

## 📸 Demonstração (Prints do Laboratório)

### Keylogger em execução:
![Keylogger Executing](images/keylogger_terminal.png)

### Arquivo Ransomware Criptografado:
![File Encrypted](images/arquivo_criptografado.png)

### Arquivo Recuperado com Sucesso:
![File Decrypted](images/arquivo_recuperado.png)

---

## 🛡️ Reflexão sobre Defesa e Mitigação
Durante este laboratório, foram identificadas as seguintes medidas de proteção essenciais no mundo real:

1.  **EDR e Antivírus:** Soluções modernas detectam o comportamento desses scripts (como monitoramento de teclado ou criptografia em massa) mesmo que o código seja novo.
2.  **Backup 3-2-1:** A defesa mais eficaz contra Ransomware é possuir backups offline. Se os dados originais estão protegidos fora da rede, o sequestro perde o valor.
3.  **Princípio do Menor Privilégio:** Usuários sem permissões de administrador dificultam a execução de scripts maliciosos em pastas críticas do sistema.
4.  **Educação do Usuário:** A conscientização sobre *phishing* e execução de arquivos desconhecidos é a primeira linha de defesa.

---

## ⚠️ Aviso Ético
Este projeto tem fins estritamente **educacionais**. O uso destas técnicas sem autorização explícita em dispositivos de terceiros é ilegal e antiético. O foco aqui é aprender a **defender**, entendendo como o ataque funciona.

