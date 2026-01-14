# IMPRESSORA

Projeto de finalização de semestre do curso de ADS (Análise e Desenvolvimento de Sistemas).

---

## 🎯 Objetivo
Este projeto estabelece comunicação entre um programa Java e uma impressora térmica utilizando uma DLL nativa. A integração é feita com a biblioteca **JNA**, permitindo executar funções da DLL diretamente na aplicação Java.  
O sistema possibilita abrir e fechar conexões, enviar textos, QR Codes, arquivos e comandos de controle para a impressora.

---

## ⚙️ Funcionamento Geral
O programa é executado principalmente em linha de comando, com algumas interações gráficas apenas na seleção de arquivos.  

Principais componentes:  
- Mapeamento da DLL através de uma interface JNA.  
- Métodos para configurar e abrir a conexão com a impressora.  
- Funções para enviar dados de impressão.  
- Seleção de arquivos para impressão.  
- Tratamento básico de erros e mensagens ao usuário.  
- Menu simples de interação.

---

## 🛠️ Passo a Passo do Fluxo do Sistema

1. **Escolha do tipo de conexão**  
   USB, RS232, TCP/IP, Bluetooth ou impressoras Android. O tipo é armazenado para uso nas funções da DLL.

2. **Carregamento da DLL**  
   A DLL responsável pela comunicação com a impressora é carregada via JNA, tornando todas as funções nativas acessíveis pelo Java.

3. **Abertura da conexão**  
   O programa solicita os parâmetros necessários (porta, IP, velocidade) e tenta abrir a conexão com a impressora.

4. **Escolha da ação do usuário**  
   - Imprimir texto digitado  
   - Imprimir conteúdo de um arquivo  
   - Imprimir QR Code  
   - Enviar comandos adicionais (avançar papel, corte)  
   - Consultar status da impressora

5. **Envio dos dados**  
   Dados (texto, bytes de arquivo, QR Code) são enviados à DLL, que realiza a comunicação com a impressora.

6. **Finalização**  
   Conexão é encerrada e o usuário é informado sobre a conclusão do processo.

---

## ✅ Recursos Implementados
- Seleção de arquivos com interface gráfica.  
- Leitura de arquivos como bytes para envio direto à impressora.  
- Codificação correta de caracteres.  
- Chamadas diretas à DLL usando JNA.  
- Tratamento funcional de erros e mensagens ao usuário.  
- Menu interativo para navegação das funções.

---

## 📝 Exemplo de uso (impressão de texto)
1. Usuário seleciona o tipo de conexão.  
2. O sistema abre a comunicação com a impressora.  
3. Usuário digita o texto que deseja imprimir.  
4. Texto é convertido e enviado para a DLL.  
5. Impressora realiza a impressão.  
6. Conexão é encerrada.

---

## 💻 Tecnologias Utilizadas
- **Java**  
- **JNA** (Java Native Access)  
- **Linha de comando / Interface gráfica mínima**
