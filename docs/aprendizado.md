# Memorial Educacional: POO em PHP

Documento síntese da construção pedagógica da `atividade02-php-poo`, registrando os conceitos fundamentais de Orientação a Objetos compreendidos e as formulações conceituais exatas utilizadas durante as checagens ativas de domínio.

---

## 1. Abstração e Contrato de Classes (`abstract`)

- **Mecânica:** A classe base `Veiculo` serve exclusivamente como molde e não pode gerar instâncias diretas.
- **Formulação exata:**
  > *"classes abstratas nao podem ser instanciadas, temos que criar uma subclasse nao abstrata pra isso"*
- **Métodos abstratos sem corpo (`calcularDiaria()`):** Obrigatoriedade de implementação nas classes filhas concretas. Se a subclasse não implementar:
  > *"da ruim"* (o PHP emite erro fatal por descumprimento de contrato).

---

## 2. Encapsulamento (`private` e Métodos de Acesso)

- **Mecânica:** Propriedades `$marca`, `$modelo` e `$ano` definidas como `private` ficam blindadas contra acesso e modificação direta, inclusive pelas próprias classes filhas.
- **Formulação exata:**
  > *"consegue n, é privado ou seja ela pode acessar via metodo herdado"*
- **Tentativa de atribuição direta na filha (`$this->marca = ...`):**
  > *"erro, é privada da classe pai"* (exige delegação ao construtor pai via `parent::__construct()`).

---

## 3. Herança e Reúso (`extends` e `parent::`)

- **Mecânica:** `Carro` e `Moto` herdam todo o comportamento público de `Veiculo` sem duplicar código.
- **Formulação exata ao acessar métodos não declarados no arquivo da subclasse:**
  > *"foi herdado de veiculo com extends"*

---

## 4. Polimorfismo na Prática

- **Mecânica:** Diferentes classes concretas respondem à mesma chamada de método (`calcularDiaria()`) de formas específicas, permitindo iterar coleções heterogêneas sem condicionais `if/else`.
- **Formulação exata do funcionamento do loop:**
  > *"funciona pq o contato de veiculo garante que ambas terao esse metodo"*
  > Identificação do conceito: *"Polimorfismo"*

---

## 5. Resolução de Dependências (`require_once`)

- **Mecânica:** Inclusão modular em cascata. O arquivo de entrada `index.php` importa apenas as especializações.
- **Formulação exata da ausência de importação direta de `Veiculo.php` no `index.php`:**
  > *"pq as subclasses ja fazem isso em seus arquivos"*

---

## 6. Extensibilidade e Princípio Aberto/Fechado (OCP)

- **Mecânica:** Para incluir novos tipos no sistema (como um `Caminhao`), o código preexistente não é alterado, apenas estendido.
- **Formulação exata para adição de novos modelos:**
  > *"teria que criar uma nova subclasse que usasse veiculo como classe pai"*
