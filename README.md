# Dashboard de Vendas Xbox Game Pass

## Visão Geral

Este projeto apresenta um dashboard desenvolvido no Microsoft Excel para análise de vendas de assinaturas do Xbox Game Pass.

O objetivo do painel é acompanhar o faturamento das assinaturas, avaliar o impacto da renovação automática e mensurar o desempenho das vendas adicionais dos serviços EA Play e Minecraft Season Pass.

O dashboard permite filtrar os resultados por tipo de assinatura (Mensal, Trimestral ou Anual) por meio de um segmentador de dados (Slicer) conectado às tabelas dinâmicas.

---

## Objetivos da Análise

- Monitorar o faturamento total das assinaturas.
- Comparar receitas com e sem renovação automática.
- Avaliar vendas adicionais de EA Play.
- Avaliar vendas adicionais de Minecraft Season Pass.
- Permitir análises por periodicidade de assinatura.

---

## Dados Utilizados

A base de dados contém **295 assinaturas** registradas entre **01/01/2024 e 16/12/2024**.

### Estrutura da Base

A tabela possui 13 campos:

| Campo | Descrição |
|---------|---------|
| Subscriber ID | Identificação do assinante |
| Subscriber Name | Nome do assinante |
| Plan | Plano contratado (Core, Standard ou Ultimate) |
| Start Date | Data de início da assinatura |
| Auto Renewal | Renovação automática |
| Subscription Price | Valor da assinatura |
| Subscription Type | Periodicidade (Monthly, Quarterly ou Annual) |
| EA Play Season Pass | Contratação do EA Play |
| EA Play Season Pass Price | Valor do EA Play |
| Minecraft Season Pass | Contratação do Minecraft Pass |
| Minecraft Season Pass Price | Valor do Minecraft Pass |
| Coupon Value | Valor do desconto aplicado |
| Total Value | Valor total da venda |

### Regra de Negócio

O valor total da venda é calculado pela seguinte fórmula:

```excel
=[@[Subscription Price]]
+[@[EA Play Season Pass Price]]
+[@[Minecraft Season Pass Price]]
-[@[Coupon Value]]