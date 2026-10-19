# RodaLucro

Protótipo de app para motoristas de aplicativo (Uber, 99, inDrive) acompanharem quanto ganham de verdade.

## O que já faz

- **Planejar o dia:** ao abrir, escolhe os apps, o dia, a meta e os gastos (café, combustível, almoço…) e vê quanto precisa fazer: meta + gastos, em reais e em corridas.
- **Hoje:** lucro líquido do dia, progresso da meta e quantas corridas faltam para batê-la (com tempo estimado).
- **+ Corrida:** registra cada corrida em 2 toques (valor e app).
- **Jornada:** botão "Iniciar dia / Encerrar dia" que conta as horas sozinho (e os km, se informar o painel).
- **Gastos:** vários gastos de uma vez (combustível, lavagem, alimentação…), com total.
- **Combustível:** escolha do tipo (gasolina, aditivada, etanol, diesel S500/S10, GNV) com preço médio de referência; consumo real medido pelos abastecimentos; conta pelo valor pago no posto ou pelos km rodados.
- **Metas:** do dia, da semana e do mês.
- **Calcular:** "vale a pena aceitar a corrida?", "etanol ou gasolina?" e "quanto preciso rodar para ganhar R$ X?".
- **Relatório mensal:** lucro, dias rodados, melhor dia, qual app rendeu mais e para onde foi o dinheiro.
- **Aparência:** tema claro/escuro e letra grande.
- **Primeiro acesso guiado:** configura combustível, consumo e meta em 30 segundos (ou mostra um exemplo).
- **Histórico e correção:** navegue pelos dias e toque num lançamento para corrigir ou apagar.
- **Manutenção:** reserva por km para óleo, pneu e revisão, e aviso da próxima troca de óleo.
- **Resumo para WhatsApp:** do dia e do mês, para enviar ou copiar.
- **Backup:** baixar ou copiar os dados e restaurar em outro celular.
- **Página de vendas:** `planos.html`, com planos Grátis e Pro.

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
- `planos.html`: página de vendas. Para o botão "Quero o Pro" abrir o seu WhatsApp, preencha `const WHATSAPP = ''` no fim do arquivo (ex.: `'5511999999999'`)
- `manifest.webmanifest`, `icon.svg`, `sw.js`: instalação no celular e uso sem internet

## Próximos passos

1. Login e dados na nuvem (Supabase) para não perder nada ao trocar de celular.
2. Assinatura mensal (Asaas ou Mercado Pago, com Pix recorrente) e plano grátis × Pro.
3. Exportar o relatório mensal em PDF.

> Neste protótipo os dados ficam salvos só no navegador do aparelho.
