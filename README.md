# CS2Radar

Um aplicativo móvel para monitorar itens do CS2 (Counter-Strike 2) no Mercado Steam.

# About

Este projeto é feito para jogadores de CS2 que gostam de investir no Mercado Steam e desejam uma solução para monitorar itens desejáveis para comprar ou vender a preços específicos.

O **backend** será desenvolvido usando Supabase (Banco de Dados PostgreSQL) para armazenar a lista completa de itens do CS2 do Mercado Steam, uma lista de itens populares e os itens selecionados pelos usuários para análise e monitoramento mais precisos.

O **frontend** usará Flutter com Dart para criar a UI e armazenar em cache a lista de itens do usuário, oferecendo uma experiência de usuário melhor e mais rápida.

# Principais Funcionalidades

- Alertas de Preço Personalizados: Os usuários podem adicionar até 10 itens à sua lista de observação pessoal (atualizada de hora em hora) e definir alertas personalizados de preço mínimo (compra) e máximo (venda).

- Cache Híbrido de Preços: O aplicativo fornece preços instantâneos para as caixas do jogo, que são atualizados de hora em hora pelo backend.

- Verificação de Preço Sob Demanda: Para itens raros (que não são caixas do jogo), os usuários podem realizar um número limitado de verificações sob demanda por dia. Isso invoca uma Edge Function que busca os preços ao vivo com segurança, sem usar o endereço IP do usuário.

- Cache Local-First: A lista de observação do usuário é salva em um banco de dados local (possivelmente Hive) no dispositivo. Isso garante tempos de carregamento instantâneos e acesso offline aos últimos preços conhecidos.

- Busca Inteligente: Um sistema robusto de busca e paginação (com um limite mínimo de caracteres) para consultar eficientemente o banco de dados de mais de 19.000 itens.
