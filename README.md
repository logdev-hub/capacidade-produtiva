# 🏭 Capacidade Produtiva — Análise Interativa com Python

## 📌 Contexto da Solução
Este projeto foi desenvolvido para calcular e analisar **capacidade produtiva** de forma visual e interativa, permitindo identificar rapidamente gargalos e perdas no processo.  
A solução diferencia **perdas planejadas** (manutenções, setups, etc.) e **não planejadas** (falhas, paradas imprevistas), exibindo resultados em **cards de KPI, gráficos comparativos e tabelas detalhadas**.

💡 **Exemplo prático:**  
Imagine uma indústria com capacidade instalada de 50.000 kg/semana, mas que devido a turnos, manutenções e paradas, só consegue entregar 16.900 kg/semana.  
Com esta ferramenta, é possível simular ajustes — como aumentar turnos ou reduzir paradas — e ver o impacto imediato nos indicadores.

---

## 📚 Bibliotecas Utilizadas
- **pandas** → Manipulação de dados tabulares (ocorrências, totais, percentuais).
- **numpy** → Cálculos e tratamento de dados.
- **matplotlib** → Criação de gráficos (capacidades, índices, ocorrências).
- **IPython.display** → Exibição de tabelas e HTML no Jupyter Notebook.
- **dataclasses** → Organização dos resultados em estruturas de dados.
- **typing** → Tipagem opcional para maior segurança do código.
- **textwrap** → Formatação automática de textos longos nos gráficos.

---

## ▶️ Como Usar (passo a passo no Jupyter Notebook)
1. **Parâmetros**: Informe velocidade (kg/h), quantidade de turnos e horas por turno.
2. **Ocorrências**: Cadastre quantas quiser para cada grupo:
   - Planejadas (ex.: manutenção preventiva)
   - Não Planejadas (ex.: quebra de máquina)  
   Digite `fim` para encerrar cada grupo.
3. **Resultados**: O notebook calcula tudo e exibe:
   - 📊 **Cards KPI**
   - 📈 **Gráficos**: Capacidades × Índices e Planejadas × Não Planejadas
   - 📑 **Tabelas**: com % e TOTAL + Indicador × Valor

## 🔧 Personalizações Úteis
- **Dias considerados**: ajuste `dias_instalada=7` e `dias_disponivel=5` na função `calcular_capacidades()`
- **Formatação dos gráficos**: edite rótulos/títulos nas funções `graficos_*`
- **Ordem das ocorrências**: a função `preparar_ocorrencias()` já ordena por horas e adiciona TOTAL e Percentual (%)

---

## 🧯 Solução de Problemas
- **Gráfico não aparece** → verifique se o Jupyter está usando o backend padrão:  
  ```python
  %matplotlib inline
  ```
- **Texto sobreposto no eixo X** → aumente a largura (`width`) no `wrap_labels()`
- **Erro de codificação** → salve o notebook em UTF-8

---

## 📈 Benefícios
- **Clareza operacional** → separa perdas planejadas e não planejadas
- **Decisão rápida** → KPIs e gráficos prontos em poucos cliques
- **Simulação** → altere turnos/horas e veja o impacto imediato
- **Padronização** → metodologia replicável para diferentes linhas e equipamentos


---

## 📝 Licença
Este projeto é distribuído sob a **MIT License**.  

---

## 👤 Autor
**Leandro Pereira**  
💼 Logística • 📊 Análise de Dados • 🐍 Python
