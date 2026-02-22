# PortFlow v7.2 – Simulação de Terminais Portuários



**PortFlow** é uma ferramenta computacional de simulação de eventos discretos desenvolvida como Trabalho de Conclusão de Curso (TCC) da **Pós-Graduação em Engenharia Naval e Oceânica da Universidade Católica de Petrópolis (UCP)**. O sistema permite modelar terminais de contêineres, identificar gargalos operacionais e avaliar cenários de melhoria por meio de indicadores de desempenho (KPIs) e análises probabilísticas.

---

## 📚 Racional Teórico

O PortFlow fundamenta-se nos seguintes pilares da engenharia de operações portuárias:

- **Teoria das Filas (Queueing Theory)**  
  O terminal é modelado como um sistema **M/M/c** (notação de Kendall):
  - Chegada de navios: processo de Poisson (taxa λ)
  - Tempo de atracação: distribuição exponencial (taxa μ)
  - Número de servidores: berços disponíveis (c)
  - Equação de Little: `L = λW` relaciona o número médio de navios no sistema com o tempo médio de espera.

- **Simulação de Eventos Discretos (DES)**  
  O estado do sistema evolui por meio de eventos discretos (chegada de navio, início/fim de operação). Cada evento altera variáveis como ocupação de berços, filas e utilização de equipamentos.

- **Análise de Gargalos**  
  Indicadores como tempo de espera, taxa de ocupação e throughput são calculados para identificar pontos de estrangulamento (ex.: número insuficiente de guindastes STS).

- **Simulação Monte Carlo**  
  Introduz variabilidade nos parâmetros de entrada (taxa de chegada, desempenho de guindastes) para estimar distribuições de probabilidade dos resultados e avaliar riscos.

- **Retorno sobre Investimento (ROI)**  
  Compara cenários com diferentes configurações de equipamentos e horários, calculando payback e ganhos anuais.

---

## ✨ Funcionalidades

- **Dashboard interativo** com KPIs e gráficos em tempo real.
- **Cadastro completo** de navios, guindastes, caminhões e berços.
- **Simulação de cenários** configurando número de berços, guindastes STS/RTG, dias e taxa de chegada.
- **Comparação lado a lado** de múltiplos cenários com gráficos radares e tabelas comparativas.
- **Simulação Monte Carlo** para análise probabilística de espera e throughput.
- **Cálculo de ROI** com análise de sensibilidade.
- **Importação de dados** via Excel/CSV e download de templates.
- **Exportação de relatórios** em PDF, Excel e CSV.
- **Histórico de ações** com opção de desfazer/refazer.
- **Tema claro/escuro** e atalhos de teclado.
- **Sistema de alertas** automáticos baseados em limites operacionais.

---

## 🛠️ Tecnologias Utilizadas

- HTML5, CSS3 e JavaScript (ES6)
- [Chart.js](https://www.chartjs.org/) – visualização de dados
- [SheetJS (XLSX)](https://sheetjs.com/) – importação/exportação de planilhas
- [jsPDF](https://github.com/parallax/jsPDF) + [jspdf-autotable](https://github.com/simonbengtsson/jsPDF-AutoTable) – geração de PDF
- [Font Awesome](https://fontawesome.com/) – ícones
- LocalStorage – persistência de dados no navegador

---

## 🚀 Como Executar

1. **Clone o repositório**  
   ```bash
   git clone https://github.com/seu-usuario/portflow.git
   cd portflow
