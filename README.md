# RodaLucro

Protótipo de app para motoristas de aplicativo (Uber, 99, inDrive) acompanharem quanto ganham de verdade.

## O que já faz

- **Hoje:** lucro líquido do dia, progresso da meta e quantas corridas faltam para batê-la (com tempo estimado).
- **Combustível automático:** calculado pelos km rodados, pelo consumo do carro e pelo preço do litro.
- **Indicadores:** bruto, gastos, lucro por km e lucro por hora, além do gráfico dos últimos 7 dias.
- **Lançar:** registro rápido de ganhos (por app) e de gastos (alimentação, lavagem, pedágio…).
- **Calcular:** "vale a pena aceitar a corrida?" e "quanto preciso rodar para ganhar R$ X?".
- **Ajustes:** meta diária, mínimo por km, consumo e preço do combustível.

Funciona como PWA: abra no celular e use "Adicionar à tela inicial".

## Como rodar

São arquivos estáticos, sem instalação. Para testar localmente:

```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

Para publicar de graça, ative o **GitHub Pages** (Settings → Pages → branch principal, pasta raiz).

## Arquivos

- `index.html`: o app inteiro (telas, estilos e lógica)
- `manifest.webmanifest`, `icon.svg`, `sw.js`: instalação no celular e uso sem internet

## Próximos passos

1. Login e dados na nuvem (Supabase) para não perder nada ao trocar de celular.
2. Assinatura mensal (Asaas ou Mercado Pago, com Pix recorrente) e plano grátis × Pro.
3. Relatório mensal em PDF e comparação entre apps.

> Neste protótipo os dados ficam salvos só no navegador do aparelho.
