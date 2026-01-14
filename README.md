DOCUMENTAÇÃO DO PROJETO

Este é um projeto de finaçização de semetre do curso de ADS (Análise e Desenvolvimento de Sistemas)

1. Objetivo

O projeto estabelece comunicação entre um programa Java e uma impressora térmica utilizando uma DLL nativa. A integração é feita com a biblioteca JNA, permitindo executar funções da DLL diretamente dentro da aplicação Java. O sistema possibilita abrir e fechar conexões, enviar textos, QR Codes, arquivos e comandos de controle para a impressora.

2. Funcionamento Geral

O arquivo principal reúne:

Mapeamento da DLL através de uma interface JNA.

Métodos para configurar e abrir a conexão com a impressora.

Funções para enviar dados de impressão.

Seleção de arquivos para impressão.

Tratamento básico de erros e mensagens ao usuário.

Menu simples de interação.

O programa é totalmente executado em linha de comando, com algumas interações gráficas apenas na seleção de arquivos.

3. Passo a Passo do Fluxo do Sistema
Passo 1 – Escolha do tipo de conexão

O sistema exibe as opções disponíveis (USB, RS232, TCP/IP, Bluetooth ou impressoras Android). Após a escolha, o tipo é armazenado para uso nas funções da DLL.

Passo 2 – Carregamento da DLL

A DLL responsável pela comunicação com a impressora é carregada via JNA. A partir daí, todas as funções nativas ficam acessíveis pelo Java.

Passo 3 – Abertura da conexão

Com base no tipo selecionado, o programa solicita os parâmetros necessários (ex.: porta, endereço IP, velocidade) e tenta abrir a conexão com a impressora utilizando as funções da DLL.

Passo 4 – Escolha da ação do usuário

O usuário pode selecionar diferentes operações, como:

Imprimir texto digitado.

Imprimir conteúdo de um arquivo.

Imprimir QR Code.

Enviar comandos adicionais, como avanço de papel ou corte.

Consultar o status da impressora.

Passo 5 – Envio dos dados

Os dados fornecidos (texto, bytes do arquivo, conteúdo do QR Code) são encaminhados à DLL, que realiza a comunicação direta com a impressora.

Passo 6 – Finalização

Ao final das operações, o programa encerra a comunicação chamando a função de fechamento da conexão. O usuário é informado sobre a conclusão do processo.

4. Recursos Implementados

Seleção de arquivos com interface gráfica.

Leitura de arquivos como bytes para envio direto à impressora.

Codificação correta de caracteres.

Chamadas diretas à DLL usando JNA.

Tratamento simples, porém funcional, de erros e mensagens ao usuário.

Menu interativo para navegação das funções.

5. Processo mais comum: imprimir texto

Usuário seleciona o tipo de conexão.

O sistema abre a comunicação com a impressora.

O usuário digita o texto que deseja imprimir.

O texto é convertido e enviado para a DLL.

A impressora realiza a impressão.

A conexão é encerrada.
