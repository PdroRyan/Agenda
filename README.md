📒 Agenda de Contatos em C (Versão com Vetor Fixo)
Este é um projeto simples de agenda de contatos em linguagem C, utilizando vetores fixos, leitura e escrita em arquivo CSV, e um menu interativo em terminal. Ideal para iniciantes praticarem manipulação de arquivos, estruturas básicas e menus em C.

✅ Funcionalidades
📥 Adicionar novo contato (nome + telefone)

📄 Imprimir todos os contatos cadastrados

❌ Marcar contatos como deletados

💾 Salvar automaticamente os contatos no arquivo .csv

📂 Carregar os dados salvos na próxima execução

🧱 Estrutura do Código
struct contato: armazena nome e telefone

Vetor fixo de contatos com capacidade máxima (N = 50)

Funções principais:

addContato: adiciona um novo contato

imprimircontatos: imprime todos os contatos não deletados

deletarContato: marca contato como deletado

salvarContatoArquivo: salva um contato (modo append)

salvarTodosContatos: sobrescreve o arquivo com todos os contatos válidos

carregarContatos: carrega os contatos a partir do arquivo

📌 Como executar
Certifique-se de atualizar o caminho do arquivo no #define ARQUIVO para um local válido no seu sistema, por exemplo:

c
Copiar
Editar
#define ARQUIVO "contatos.csv"
Compile com gcc:

bash
Copiar
Editar
gcc -o agenda agenda.c
./agenda
🧾 Formato do Arquivo CSV
Cada linha representa um contato no formato:

Copiar
Editar
nome,telefone
Maria,999999999
Joao,888888888
Contatos "deletados" são salvos como:

lua
Copiar
Editar
Deletado,----
🎯 Limitações
Capacidade limitada a 50 contatos (#define N 50)

Contatos deletados continuam ocupando espaço no vetor

Contatos não são realmente removidos do vetor, apenas marcados
