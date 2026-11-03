Requisitos Funcionais (RF)
RF01 - Cadastro e Autenticação de Usuários: O sistema deve permitir que usuários se cadastrem (nome, e-mail, senha, localização/bairro e telefone) e façam login na plataforma.

RF02 - Gerenciamento de Perfil: O usuário deve poder visualizar e editar suas informações de contato e ver o histórico de trocas/doações realizadas.

RF03 - Cadastro de Livro: O usuário deve poder cadastrar um livro para doação ou troca, informando: título, autor, fotos, categoria/gênero e descrição do estado de conservação (ex.: Novo, Seminovo, Marcas de uso).

RF04 - Catálogo e Busca de Livros: O aplicativo deve exibir um catálogo de livros disponíveis com filtros por título, autor, gênero e estado de conservação.

RF05 - Lista de Desejos (Wishlist): O usuário deve poder adicionar títulos à sua lista de desejos.

RF06 - Notificação de Disponibilidade: O sistema deve enviar uma notificação ao usuário assim que um livro da sua lista de desejos for cadastrado no catálogo por outro usuário.

RF07 - Conexão via WhatsApp: O sistema deve disponibilizar um botão/link direto na página do livro que redirecione para o WhatsApp do proprietário, permitindo que os usuários combinem a entrega/troca.

RF08 - Sistema de Avaliações: Após o alinhamento ou conclusão da entrega, os usuários devem poder avaliar um ao outro com uma nota (1 a 5 estrelas) e um comentário descritivo.



Requisitos Não-Funcionais (RNF)
RNF01 - Segurança: A autenticação do usuário deve ser segura (senhas criptografadas no banco de dados com hash salgado como bcrypt) e o envio do número do WhatsApp deve respeitar o consentimento prévio do usuário (LGPD).

RNF02 - Desempenho e Usabilidade: A navegação entre telas deve ser fluida (tempo de resposta inferior a 2 segundos) e otimizada para uso em dispositivos móveis (design responsivo/nativo).

RNF03 - Disponibilidade: O sistema deve ter arquitetura em nuvem que garanta alta disponibilidade (mínimo de 98% uptime durante o período de testes).

RNF04 - Portabilidade: O aplicativo deve rodar perfeitamente em sistemas operacionais Android e iOS.



Fluxo de Navegação do Usuário
[ Tela de Splash / Login ]
        │
        ├──> [ Cadastro de Usuário ]
        │
        └──> [ Tela Principal / Catálogo (Home) ]
                  │
                  ├──> [ Detalhes do Livro ] ──> [ Clique: Redireciona WhatsApp ]
                  │          │
                  │          └──> [ Perfil do Doador / Avaliações ]
                  │
                  ├──> [ Tela de Cadastro de Novo Livro ]
                  │
                  ├──> [ Lista de Desejos (Wishlist) ] ──> [ Recebe Notificação ]
                  │
                  └──> [ Perfil do Usuário / Meus Livros / Histórico de Avaliações ]


Esboço das Telas Principais (Layout Básico)
Tela 1 - Home / Catálogo: Topo com barra de pesquisa e filtros por categoria. Lista vertical/grid de cards contendo: Imagem da capa, Título, Autor e tag "Conservação".

Tela 2 - Detalhe do Livro: Foto destacada em tamanho maior, Título, Autor, Estado de conservação detalhado, Nome do Doador (com sua média de avaliação por estrelas) e botão em destaque "Combinar Troca no WhatsApp".

Tela 3 - Lista de Desejos: Campo de busca rápida para adicionar títulos desejados. Lista de itens cadastrados com chave de ativação para notificações ativas.

Tela 4 - Cadastrar Livro: Formulário com campos: Título, Autor, Descrição/Estado de conservação, upload de foto e botão "Publicar Livro".


Arquitetura de Comunicação (Visão Geral em Camadas)
┌─────────────────────────────────────────────────────────────┐
│                    CAMADA DE APRESENTAÇÃO                   │
│         App Mobile (React Native / Flutter)                 │
└──────────────┬───────────────────────────────▲──────────────┘
               │                               │
               │ Requisições HTTP/REST (JSON)  │ Notificações Push / Respostas
               ▼                               │
┌──────────────────────────────────────────────┴──────────────┐
│                    CAMADA DE APLICAÇÃO                      │
│         Servidor API REST (Node.js / Python / Java)         │
│  - Módulo de Autenticação   - Módulo de Cadastro/Busca      │
│  - Módulo de Wishlist       - Serviço de Notificação (FCM)  │
└──────────────┬──────────────────────────────────────────────┘
               │
               │ Consultas SQL / NoSQL
               ▼
┌─────────────────────────────────────────────────────────────┐
│                    CAMADA DE DADOS                          │
│         Banco de Dados Relacional / Não-Relacional          │
└─────────────────────────────────────────────────────────────┘


Estruturação das Informações (Modelagem Simplificada do Banco de Dados)
Tabela Usuarios: id, nome, email, senha_hash, telefone_whatsapp, bairro_cidade, criado_em.

Tabela Livros: id, usuario_id (FK), titulo, autor, genero, estado_conservacao, status (Disponível/Trocado), foto_url, criado_em.

Tabela Wishlist: id, usuario_id (FK), titulo_desejado, autor_desejado.

Tabela Avaliacoes: id, avaliador_id (FK), avaliado_id (FK), livro_id (FK), nota (1-5), comentario, data.
