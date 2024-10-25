---
cssclasses:
  - list-cards
link: https://www.brunoribas.com.br/so/slides-fs/FS-metodos-alocacao-caciano-eduardo.pdf
---
Quick demo:
# Alocação Contígua
- **O que é?**: Armazena arquivos em blocos adjacentes no disco.
- **Como funciona?**: Quando um arquivo é salvo, ele ocupa um espaço contínuo, como um livro em uma estante. Leia mais em: [[alocação contígua complemento]]
- **Vantagens**: Acesso rápido, pois o cabeçote de leitura não precisa se mover muito.
- **Desvantagens**: Dificuldade em encontrar espaço livre conforme o disco é fragmentado, o que pode levar a desperdício de espaço.

# Alocação Encadeada
- **O que é?**: Armazena arquivos em blocos não adjacentes, com cada bloco apontando para o próximo.
- **Como funciona?**: É como uma corrente; cada bloco contém um ponteiro para o próximo bloco do arquivo.
- **Vantagens**: Mais flexível com o espaço, pois não precisa de um espaço contínuo.
- **Desvantagens**: O acesso pode ser mais lento, já que o sistema precisa seguir os ponteiros para encontrar todos os blocos.

# Alocação Indexada
- **O que é?**: Usa uma tabela de índice para rastrear onde os blocos de um arquivo estão localizados.
- **Como funciona?**: Um bloco especial contém um índice que aponta para todos os outros blocos do arquivo.
- **Vantagens**: Permite acessar rapidamente qualquer parte do arquivo, pois você tem um índice centralizado.
- **Desvantagens**: Pode exigir mais espaço para armazenar o índice, especialmente para arquivos muito grandes.