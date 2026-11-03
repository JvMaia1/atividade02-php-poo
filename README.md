# Atividade 02 - PHP com POO

Projeto de catálogo de locação de veículos desenvolvido para fixação e aplicação prática dos pilares da Orientação a Objetos em PHP.

---

## 📁 Estrutura do Projeto

```text
atividade02-php-poo/
├── src/
│   ├── Veiculo.php        # Classe abstrata base (contrato, propriedades privadas e getters)
│   ├── Carro.php          # Subclasse com especialização de portas e diária própria
│   └── Moto.php           # Subclasse com especialização de cilindradas e diária própria
├── docs/
│   └── aprendizado.md     # Memorial de fixação com os conceitos validados durante o processo
├── index.php              # Ponto de entrada, instanciação dos objetos e renderização visual
├── estilo.css             # Estilização dos cartões de exibição
├── atividade.md           # Enunciado e checklist original da atividade
└── README.md              # Documentação básica do projeto
```

---

## 🚀 Como Executar

Inicie o servidor embutido do PHP na raiz do projeto:

```bash
php -S localhost:8000
```

Acesse em seu navegador: `http://localhost:8000`

---

## 🧠 Workflow de Desenvolvimento

O desenvolvimento foi conduzido através de um fluxo de **Pair Programming com validação ativa de domínio**:

- **Construção incremental em blocos:** A IA atuou na geração do boilerplate e código das classes.
- **Portões de entendimento:** O avanço entre as etapas (abstração, herança, polimorfismo e integração) só ocorreu após a confirmação objetiva do entendimento de cada mecanismo pelo desenvolvedor.
- **Foco em absorção:** Economia de tempo em digitação manual com retenção cognitiva e domínio conceitual comprovados no [docs/aprendizado.md](docs/aprendizado.md).
