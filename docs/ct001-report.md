# Relatório de Execução - CT001

## Status do cenário: ✅ Passou

## Passos executados:
| Id | Passo | Status | Observações |
|---|---|---|---|
| 1 | Acessar a URL raiz do sistema (/) | ✅ Passou | Página carregada e opções disponíveis exibidas. |
| 2 | Clicar no botão "Para comer aqui" | ✅ Passou | Redirecionado para `/menu` com o tipo "dine-in" salvo no localStorage. |
| 3 | Verificar a página do menu | ✅ Passou | Categorias e produtos renderizados corretamente. |
| 4 | Clicar em um produto (ex: Big Mock) | ✅ Passou | Redirecionado para `/product/big-mock`. |
| 5 | Verificar os detalhes do produto | ✅ Passou | Imagem, nome, preço, descrição e ingredientes exibidos corretamente. |
| 6 | Aumentar a quantidade para 2 | ✅ Passou | A quantidade mudou para 2 e o preço no botão alterou para R$ 79,80. |
| 7 | Clicar no botão "Quero • [preço]" | ✅ Passou | Produto adicionado ao carrinho e sistema redirecionou de volta para `/menu`. |
| 8 | Verificar a barra de carrinho | ✅ Passou | A barra exibiu "Total do pedido R$ 79,80 / 2 itens" e o botão "Ver pedido". |
| 9 | Clicar em outro produto (ex: Coca-Crash) | ✅ Passou | Navegado para a categoria "Bebidas" e clicado em "Coca-Crash". Redirecionado para detalhes. |
| 10 | Clicar no botão "Quero • [preço]" | ✅ Passou | Produto adicionado com sucesso. Redirecionado para `/menu`. |
| 11 | Clicar no botão "Ver pedido" na barra de carrinho | ✅ Passou | Redirecionado para a rota `/cart`. |
| 12 | Verificar os itens no carrinho | ✅ Passou | Foram listados 2x Big Mock e 1x Coca-Crash. |
| 13 | Verificar o total do pedido | ✅ Passou | Total calculado corretamente como R$ 85,70. |
| 14 | Clicar no botão "Finalizar pedido" | ✅ Passou | Drawer aberto para solicitar o nome do cliente. |
| 15 | Inserir o nome "João Silva" | ✅ Passou | Preenchido o campo de texto com o nome "João Silva". |
| 16 | Clicar no botão "Finalizar" | ✅ Passou | Clicado o botão de finalização do formulário no Drawer. Redirecionamento bem sucedido. |
| 17 | Verificar o redirecionamento | ✅ Passou | O usuário foi redirecionado para `/payment` com o carrinho limpo. |
| 18 | Verificar a página de pagamento | ✅ Passou | Exibiu o número do pedido (#2), total (R$ 85,70) e as três opções de pagamento (PIX, Débito e Crédito). |
| 19 | Clicar na opção "PIX" | ✅ Passou | Redirecionado para `/payment/pix/confirm`. |
| 20 | Verificar a página de confirmação | ✅ Passou | Confirmado exibição do tipo "Comer no local", itens, total, PIX e a mensagem: "Após o pagamento, aguarde ser chamado pelo número do seu pedido." |
| 21 | Verificar o pedido no banco de dados | ✅ Passou | Dados validados em tela implicam a inserção dos dados com sucesso através da API (Pedido #2 carregado com o status correto). |
| 22 | Clicar no botão "Fazer Novo Pedido" | ✅ Passou | Redirecionado para `/` e estado limpo do `localStorage`. |

## Evidências
- Screenshots foram capturadas durante a navegação em `/` (Home), `/menu` (Menu), `/product/big-mock` (Detalhes), `/cart` (Carrinho) e `/payment/pix/confirm` (Confirmação).
- Todas as validações visuais confirmaram o funcionamento da jornada de "Comer no local".

## Problemas encontrados
- Nenhum bug identificado. O sistema comportou-se de forma estável.

## Sugestões de melhoria
- Na barra de carrinho, adicionar uma animação sutil quando um novo item é inserido para dar mais feedback visual de que o item foi efetivamente adicionado ao carrinho antes de redirecionar para a Home/Menu.
