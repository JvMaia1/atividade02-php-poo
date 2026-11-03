# PHP com POO: Atividade 2

> **Objetivo:** Completar o backend em PHP de uma página de aluguel de veículos (um carro e uma moto). O HTML e o CSS já vêm prontos; o foco é a implementação das classes e a instanciação dos objetos.

---

## 🎯 Conceitos Praticados

- `Classes e Objetos`
- `Propriedades e Métodos`
- `Encapsulamento (private e getters)`
- `Método Construtor (__construct)`
- `Herança (extends e parent::__construct)`
- `Abstração (classe e método abstract)`
- `Polimorfismo`

---

## 📁 Estrutura do Projeto

```text
atividade02-php-poo/
├── src/
│   ├── Veiculo.php       # Classe abstrata base
│   ├── Carro.php         # Classe concreta (extends Veiculo)
│   └── Moto.php          # Classe concreta (extends Veiculo)
├── estilo.css            # Estilos (fornecido)
├── index.php             # Carrega classes, instancia objetos e exibe os cards
└── atividade.md
```

---

## 🚗 Especificação dos Veículos

| Veículo | Atributos Comuns | Atributo Específico | Diária |
| :--- | :--- | :--- | :--- |
| **Carro** | `marca`, `modelo`, `ano` | `quantidadePortas`: **4** | **R$ 150,00** |
| **Moto** | `marca`, `modelo`, `ano` | `cilindradas`: **300** | **R$ 70,00** |

---

## 📋 Checklist de Tarefas

### 1. `src/Veiculo.php` (Classe Abstrata)
- [x] Declarar a classe abstrata `Veiculo`.
- [x] Definir como `private` as propriedades: `$marca`, `$modelo` e `$ano`.
- [x] Implementar o `__construct($marca, $modelo, $ano)`.
- [x] Criar os métodos getters para as 3 propriedades.
- [x] Declarar o método abstrato `calcularDiaria(): float`.

### 2. `src/Carro.php` (Herança)
- [x] Criar a classe `Carro` herdando de `Veiculo` (`extends Veiculo`).
- [x] Definir a propriedade privada `$quantidadePortas`.
- [x] Implementar o `__construct()` chamando `parent::__construct(...)` e inicializando `$quantidadePortas`.
- [x] Criar o getter para `quantidadePortas`.
- [x] Implementar o método `calcularDiaria()`, retornando `150.00`.

### 3. `src/Moto.php` (Herança)
- [x] Criar a classe `Moto` herdando de `Veiculo` (`extends Veiculo`).
- [x] Definir a propriedade privada `$cilindradas`.
- [x] Implementar o `__construct()` chamando `parent::__construct(...)` e inicializando `$cilindradas`.
- [x] Criar o getter para `cilindradas`.
- [x] Implementar o método `calcularDiaria()`, retornando `70.00`.

### 4. `index.php` (Integração e Exibição)
- [x] Carregar as classes necessárias com `require_once`.
- [x] Instanciar um objeto de `Carro` e um objeto de `Moto`.
- [x] Usar os getters e o método `calcularDiaria()` para preencher os valores nos cards HTML.

---

## ⚠️ Regras e Boas Práticas

> [!IMPORTANT]
> - **Não instanciar `Veiculo`:** Por ser abstrata, ela serve apenas como molde para as classes filhas.
> - **Zero duplicação:** Não redeclare `$marca`, `$modelo` ou `$ano` dentro de `Carro` ou `Moto`.
> - **Uso de `parent::__construct()`:** Repasse os atributos comuns para a superclasse no construtor das filhas.
> - **Separação de responsabilidades:** Mantenha classes isoladas em `src/` e deixe o `index.php` responsável apenas por instanciar e renderizar.
> - **Escopo enxuto:** Não use banco de dados nem formulários. Altere o HTML/CSS somente se estritamente necessário.

---

## 🚀 Passo a Passo & Entrega

1. **Repositório:** Criar repositório público chamado `atividade02-php-poo`.
2. **Arquivos Base:** Baixar `index.php` e `estilo.css` do Teams e mover para a raiz do repositório.
3. **Desenvolvimento:** Criar a pasta `src/` e implementar as classes conforme checklist.
4. **Execução:** Subir o servidor local (`php -S localhost:8000`) e testar a exibição.
5. **Entrega:** Postar o link do repositório no canal do Teams.
