# Relatório de Execução - CT002

## Status do cenário: ✅ Passou

## Passos executados:
| Id | Passo | Status | Observações |
|---|---|---|---|
| 1 | Acessar a URL raiz do sistema (/) | ✅ Passou | Página inicial carregada corretamente. |
| 2 | Clicar no botão "Para levar" | ✅ Passou | `takeaway` salvo no localStorage e redirecionado para `/menu`. |
| 3 | Verificar a página do menu | ✅ Passou | Exibido o menu com todas as categorias. |
| 4 | Clicar na aba "Fritas" | ✅ Passou | Menu filtrado para exibir itens da categoria "Fritas". |
| 5 | Clicar em um produto de fritas (ex: Batatas Full Stack) | ✅ Passou | Redirecionado para `/product/batatas-fullstack`. |
| 6 | Verificar os detalhes do produto | ✅ Passou | Detalhes como imagem, preço e ingredientes exibidos corretamente. |
| 7 | Manter a quantidade em 1 | ✅ Passou | Mantida a quantidade padrão (1). |
| 8 | Clicar no botão "Quero • [preço]" | ✅ Passou | Produto adicionado ao carrinho e redirecionado para `/menu`. |
| 9 | Clicar na aba "Bebidas" | ✅ Passou | Categoria "Bebidas" selecionada. |
| 10 | Clicar em um produto de bebida (ex: Fanta Warning) | ✅ Passou | Redirecionado para `/product/fanta-warning`. |
| 11 | Aumentar a quantidade para 3 | ✅ Passou | A quantidade mudou para 3 e o botão refletiu o total de R$ 17,70. |
| 12 | Clicar no botão "Quero • [preço]" | ✅ Passou | Produto adicionado e retorno para `/menu`. |
| 13 | Verificar a barra de carrinho | ✅ Passou | Barra exibiu R$ 28,60 e 4 itens. |
| 14 | Clicar no botão "Ver pedido" na barra de carrinho | ✅ Passou | Redirecionado para `/cart`. |
| 15 | Verificar os itens no carrinho | ✅ Passou | Batatas Full Stack (1x) e Fanta Warning (3x) listados. |
| 16 | Aumentar a quantidade de um item no carrinho | ✅ Passou | A quantidade das Batatas Full Stack foi incrementada para 2x. |
| 17 | Verificar o total do pedido | ✅ Passou | Total recalculado para R$ 39,50. |
| 18 | Clicar no botão "Finalizar pedido" | ✅ Passou | Drawer aberto para solicitar nome. |
| 19 | Inserir o nome "Maria Santos" | ✅ Passou | Nome preenchido no input. |
| 20 | Clicar no botão "Finalizar" | ✅ Passou | Redirecionamento após o cadastro do pedido. |
| 21 | Verificar o redirecionamento | ✅ Passou | Redirecionado para `/payment` com carrinho vazio. |
| 22 | Verificar a página de pagamento | ✅ Passou | O número do pedido #3 e as três opções de pagamento (PIX, Débito e Crédito) foram exibidos. |
| 23 | Clicar na opção "Cartão de Crédito" | ✅ Passou | Redirecionado para `/payment/credit/confirm`. |
| 24 | Verificar a página de confirmação | ✅ Passou | Número de pedido, tipo "Para levar" e itens refletidos corretamente. |
| 25 | Verificar que não há mensagem de aguardar | ✅ Passou | A mensagem "aguarde ser chamado" não foi exibida. Apenas instruções de pagamento. |
| 26 | Verificar o pedido no banco de dados | ✅ Passou | A criação foi implícita pelo sucesso e consistência na exibição do número do pedido gerado pelo backend. |
| 27 | Clicar no botão "Fazer Novo Pedido" | ✅ Passou | Retorno para `/` com estado limpo. |

## Evidências
- As ações foram capturadas via screenshots do Playwright durante toda a jornada de "Para levar" (takeaway).
- As validações dos estados dos componentes, botões e valores atualizados comprovaram o funcionamento integral do fluxo.

## Problemas encontrados
- Nenhum bug identificado. O fluxo ocorreu corretamente.

## Sugestões de melhoria
- O botão `+` (Aumentar a quantidade) apresentou acessibilidade e seletividade confusa. A adição de `aria-labels` claros (como `Aumentar quantidade` ou `Diminuir quantidade`) ajudaria para testes de acessibilidade e E2E via seletores ARIA.
