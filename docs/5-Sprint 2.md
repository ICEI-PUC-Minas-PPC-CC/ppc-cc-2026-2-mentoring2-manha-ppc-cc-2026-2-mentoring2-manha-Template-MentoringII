# Sprint 2

1.Pesquisa de soluções existentes no mesmo domínio do problema identificado, destacando características, pontos positivos, limitações e diferenciais; 

Dois desperdícios recorrentes e conectados livros de literatura que ficam parados nas estantes depois de lidos, e também material didático de escolas particulares e cursinhos pré-vestibular, descartado todo fim de ano, enquanto isso, alunos bolsistas e estudantes de baixa renda não têm condições de comprar o mesmo material, a proposta é um app, de atuação inicial municipal, que conectará:
●Leitores que querem trocar livros de literatura entre si.
●Famílias de escolas particulares/cursinhos com material didático disponível para doação.
O mercado atual não possui concorrentes diretos que combinem a troca de livros de literatura geral com a doação direcionada de material didático para estudantes. As soluções existentes se dividem em três grandes categorias:
●Plataformas de Troca de Livros (Gerais): Apps e sites como Troca de Livros, Seebo, Swappy Books, EscamBook e LivraLivro focam em literatura geral e facilitam a troca presencial ou por pontos. Destacam-se pela facilidade de uso (como leitura de ISBN) e foco em sustentabilidade, mas pecam pela falta de recorte social, ausência de doações estruturadas e falhas de usabilidade e retenção.
●Soluções Didáticas: O Yzye é o concorrente que mais se aproxima do modelo, unindo venda, troca e doação de livros didáticos. No entanto, possui baixo alcance (cerca de 100 usuários) e carece de curadoria específica para bolsistas ou parcerias com instituições de ensino.
●Iniciativas Sociais (ONGs): Projetos como Passarte e Leitura para Todos SP realizam o trabalho social de triagem e distribuição de materiais para alunos vulneráveis com forte impacto real. A limitação está no modelo 100% físico e manual, sem uma tecnologia digital que conecte diretamente doadores e alunos, projetos como esse também comprovam a necessidade do App.

2.realização de entrevistas com potenciais usuários ou pessoas relacionadas ao contexto do problema, quando possível. Caso não tenham sido realizadas entrevistas, a equipe deverá apresentar como foi feita a análise do público e quais informações ou evidências foram utilizadas; 

Iniciativas que promovam estímulo e acesso à leitura são urgentes em nosso país, considerando inclusive os dados apresentados pela análise do PISA 2025 (Programa Internacional de Avaliação de Estudantes), no último dia 08.09.2026, que oferece informações sobre o desempenho dos estudantes na faixa etária dos 15 anos, de vários países, e avalia os conhecimentos e as habilidades desses jovens.
Um dos principais pontos destacados está a desigualdade de aprendizagem, fortemente revelado pelo nível socioeconômico, que no Brasil, entre os estudantes mais pobres, representa que 67% têm baixo desempenho em Leitura.
Nesse sentido, é muito importante que a universidade fomente pesquisas e projetos que possam apresentar respostas às principais questões que a sociedade enfrenta no dia a dia, sejam de acesso à leitura, de repertório cultural e leituras que possam abrir horizontes, nesse caso específico, levando à emancipação acadêmica e pessoal.
Como todos nós sabemos, o livro impresso e algumas obras digitais são produtos caros em nosso país, impactando principalmente os menos favorecidos financeiramente, que muitas vezes não têm acesso a esse acervo intelectual. Mas também sabemos que é a leitura que eleva o potencial de interpretação do mundo e coloca os jovens, no caso, em outro patamar de ação enquanto sujeitos da própria história.
As leituras obrigatórias apresentadas pelos grandes vestibulares do país, buscam fazer esse movimento de repertório tão necessário, por isso, seria imprescindível promover a acessibilidade desses livros a todos jovens, diminuindo o abismo que há, inclusive, de acesso às universidades de qualidade.

Juliana Cristina Costa - Assessora da Anglo
O descarte massivo de apostilas no fim do ano letivo e o acúmulo de livros parados nas estantes escancaram um problema clássico de alocação de recursos: de um lado, materiais valiosos perdem a utilidade; do outro, alunos bolsistas e de baixa renda enfrentam gargalos financeiros para ter acesso a conteúdos didáticos e obras de vestibulares.
Analisando o ecossistema atual de software, identificamos um gap claro. As aplicações existentes tratam trocas literárias gerais e doações de forma totalmente desacoplada, sem uma arquitetura que conecte a ponta doadora diretamente ao estudante vulnerável. Em validação de campo com uma professora, ela reforçou como essa assimetria no acesso ao material impacta no desempenho dos alunos e perpetua a desigualdade no ingresso ao ensino superior.
Para modelar uma solução eficiente e orientada às dores reais, estruturamos um roteiro de entrevistas rápidas segmentado em três perfis: leitores, famílias doadoras e alunos beneficiários. A meta é mapear padrões de uso, identificar gargalos de UX e logística, e validar os requisitos de segurança e 
confiança necessários para o desenvolvimento da plataforma.

3.construção ou refinamento das personas, representando os principais perfis do público-alvo; 

Persona 1 — Leitor trocador
Nome fictício: Bianca, 22 anos, estudante universitária Objetivo: renovar a estante sem gastar, sem acumular livros já lidos Frustrações: livrarias caras; sites de troca genéricos (ex.: Troca de Livros, Seebo) exigem esperar alguém interessado no mesmo título; medo de golpe em combinações via WhatsApp O que o app resolve: troca local, dentro do município, com histórico de reputação

Persona 2 — Família doadora
Nome fictício: Marcos, 45 anos, pai de aluno de cursinho pré-vestibular Objetivo: dar um destino útil ao material do filho ao final do ano, sem esforço logístico Frustrações: não sabe para onde doar; acha ONGs distantes ou burocráticas (como percebido em iniciativas tipo Passarte); joga fora por comodidade O que o app resolve: doação direcionada e simples, dentro da própria cidade, com destino visível (sabe que ajudou um aluno específico)

Persona 3 — Aluno bolsista/baixa renda
Nome fictício: Kauê, 17 anos, bolsista em escola particular, cursando o 3º ano do ensino médio Objetivo: ter acesso ao mesmo material didático dos colegas, sem custo Frustrações: vergonha de pedir; falta de canal claro para conseguir apostilas/livros de anos anteriores O que o app resolve: acesso discreto e direto a doações de material didático compatível com seu curso/série

4.revisão da proposta de solução com base nas informações obtidas durante o benchmark, nas entrevistas, quando realizadas, e nas demais análises desenvolvidas pela equipe; 

Ajustes recomendados a partir do que o benchmark revelou:
Separar claramente os dois fluxos dentro do app (troca ponto-a-ponto de literatura vs. doação direcionada de material didático) — nenhum concorrente faz essa separação, e ela evita que o app vire "mais um marketplace genérico" como Troca de Livros/Seebo/EscamBook.
Adotar verificação/curadoria leve para o fluxo de doação (ex.: cadastro como aluno bolsista, ou parceria com a coordenação da escola/cursinho), resolvendo o problema de confiança que aparece nas reviews negativas de apps como Swappy Books e Seebo.
Manter escopo municipal no MVP — isso é o principal diferencial frente a ONGs como Passarte/Leitura para Todos SP, que operam fisicamente e têm dificuldade de escalar por causa da logística de entrega; um app local resolve o "last mile" com o próprio usuário combinando a entrega.
Evitar dependência de canais externos (WhatsApp) para fechar a negociação, diferente do EscamBook — manter chat e combinação de entrega dentro do próprio app aumenta segurança e retenção.
Parcerias institucionais diretas com escolas/cursinhos para o fluxo de doação (em vez de depender só de doações espontâneas de famílias), inspirado no modelo que a Passarte já validou com escolas parceiras — mas trazendo esse relacionamento para dentro do app.

5.Registro de contribuições da equipe
André Luiz:
- Realização de entrevistas com potenciais usuários ou pessoas relacionadas ao contexto do problema.
Diana Vitória:
- Realização de alterações e atualizações no repositório do GitHub, incluindo o preenchimento e a organização das atividades referentes ao Sprint 1.
- Criação e preenchimento do Lean Canvas.
- Atualização do GitHub para refletir as mudanças realizadas na ideia e no direcionamento do projeto.
- Revisão e atualização do Lean Canvas de acordo com as alterações na proposta do projeto.
- Revisão e adequação das atividades e informações do Sprint 1, garantindo que estivessem alinhadas à nova definição da ideia do projeto.
Gabriel de Paula Lima:
- Formatação do documento para ABNT.
Matheus Felizardo:
- Registro de contribuições da equipe.
Pedro Luz:
- Efetuado pesquisa de campo / criação de arquivo word contendo respostas das entrevistas com público misto, para levantamento de base inicial sobre a ideia da aplicação.
Samuel Amaral Jacinto:
- Respostas do Sprint 2.
