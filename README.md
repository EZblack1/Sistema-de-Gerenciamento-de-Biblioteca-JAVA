# Sistema de Gerenciamento de Biblioteca - POO_252_P1

## Informações do Projeto

**Disciplina:** Programação Orientada a Objetos  
**Projeto:** P1 - Introdução aos Conceitos Básicos de Orientação a Objetos em Java  
**Hierarquia Escolhida:** Linha 1 - Material → Livro, Revista  

## Justificativa da Escolha

Escolhemos a hierarquia **Material → Livro, Revista** porque:
- É um domínio familiar e prático (biblioteca/livraria)
- Permite demonstrar claramente os conceitos de OO
- Oferece contexto rico para implementar funcionalidades variadas
- Facilita a compreensão dos relacionamentos entre classes

## Estrutura do Projeto

```
POO_252_P1_Sistema_Biblioteca/
└── src/
    ├── Material.java           # Classe base
    ├── Livro.java             # Subclasse 1
    ├── Revista.java           # Subclasse 2
    └── GerenciadorBiblioteca.java # Classe principal
```

## Conceitos Implementados

### 1. Encapsulamento
- **Atributos privados** em todas as classes
- **Getters e setters** com validações
- **Validações implementadas:**
  - Preço não pode ser negativo
  - Ano de publicação entre 1 e 2025
  - Título e autor não podem ser vazios
  - Número de páginas deve ser positivo

### 2. Construtores
- **Construtor padrão** em todas as classes com valores default
- **Construtor sobrecarregado** com todos os parâmetros
- **Uso do super()** nas subclasses para chamar construtores da superclasse

### 3. Herança
- **Classe base:** `Material` com atributos comuns
- **Subclasses:** `Livro` e `Revista` herdam de `Material`
- **Atributos específicos:**
  - Livro: `numeroPaginas`, `ehFiccao`
  - Revista: `edicao`, `tema`

### 4. Sobrescrita de Métodos
- **`exibirInformacoes()`** sobrescrito nas subclasses
- **Reutilização** do método da superclasse com `super.exibirInformacoes()`
- **Informações específicas** adicionadas em cada subclasse

### 5. Sobrecarga de Métodos
- **Na classe Material:**
  - `calcularValorEmprestimo()` - valor base
  - `calcularValorEmprestimo(double desconto)` - com desconto
  - `calcularValorEmprestimo(double desconto, double taxaAtraso)` - com desconto e taxa

- **Na classe Livro:**
  - `calcularValorEmprestimo(int diasEmprestimo)` - baseado na duração

- **Na classe Revista:**
  - `calcularValorEmprestimo(String tipoUsuario)` - baseado no tipo de usuário
  - `calcularValorEmprestimo(String tipoUsuario, String periodicidade)` - completo

## Funcionalidades Implementadas

### Classe Material
- Gerenciamento de informações básicas (título, autor, ano, preço)
- Cálculo de valor de empréstimo com diferentes parâmetros
- Validações de entrada de dados

### Classe Livro
- Informações específicas (páginas, gênero)
- Cálculo de tempo estimado de leitura
- Classificação por tamanho (pequeno, médio, grande)
- Cálculo de empréstimo baseado na duração

### Classe Revista
- Informações específicas (edição, tema)
- Identificação de edições especiais
- Categorização por tema
- Cálculos diferenciados por tipo de usuário e periodicidade

### Classe GerenciadorBiblioteca
- **Demonstrações organizadas** de todos os conceitos
- **Criação interativa** de novos materiais
- **Polimorfismo** com array de Material
- **Interface amigável** via console

## Como Executar

1. **Compilar:**
   ```bash
   cd src
   javac *.java
   ```

2. **Executar:**
   ```bash
   java GerenciadorBiblioteca
   ```

## Demonstrações do Programa

O programa executa automaticamente as seguintes demonstrações:

1. **Construtores:** Criação de objetos com construtores padrão e sobrecarregado
2. **Encapsulamento:** Modificação de atributos via setters com validações
3. **Herança/Polimorfismo:** Tratamento de subclasses como Material
4. **Sobrecarga:** Diferentes versões dos métodos de cálculo
5. **Interativa:** Criação de novo material com entrada do usuário

## Exemplos de Saída

### Demonstração de Herança
```
Material 1:
=== INFORMAÇÕES DO MATERIAL ===
Título: 1984
Autor: George Orwell
Ano de Publicação: 1949
Preço: R$ 35,90
Número de Páginas: 328
Gênero: Ficção
Tipo: LIVRO
```

### Demonstração de Sobrecarga
```
--- CÁLCULOS DE EMPRÉSTIMO ---
Valor base: R$ 3,59
Com 20% desconto: R$ 2,87
Com 10% desconto + 15% taxa atraso: R$ 3,72
```

## Critérios Atendidos

✅ **Escolha e Adaptação da Hierarquia:** Sistema de biblioteca com Material → Livro, Revista  
✅ **Encapsulamento:** Atributos privados com getters/setters validados  
✅ **Herança:** Subclasses herdam corretamente da classe base  
✅ **Construtores:** Padrão e sobrecarregado implementados  
✅ **Sobrecarga:** Múltiplas versões de métodos implementadas  
✅ **Sobrescrita:** Métodos personalizados nas subclasses  
✅ **Funcionalidade:** Programa completo e demonstrativo  
✅ **Qualidade do Código:** Bem organizado e comentado  

## Características Técnicas

- **Linguagem:** Java
- **Paradigma:** Orientação a Objetos
- **Interface:** Console (Scanner)
- **Validações:** Implementadas em todos os setters
- **Documentação:** Comentários explicativos em todo o código
- **Organização:** Separação clara de responsabilidades