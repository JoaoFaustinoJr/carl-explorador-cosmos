# Auditoria técnica e curadoria — CARL

Data: 10/11/2026. Escopo: inspeção estática do código publicado no repositório, do manifesto PWA, do service worker, da documentação e das referências locais de mídia. **Não equivale a testes funcionais em navegadores ou aparelhos reais.**

## Resultado

**Situação: apto a piloto acompanhado; homologação final condicionada a testes práticos.**

### Pontos verificados

- O aplicativo mantém estrutura de observatório em português, com seções de corpos celestes, luz e distâncias, Sistema Solar, céu noturno, Via Láctea, história e exploração espacial.
- Há manifesto PWA, ícone, registro de service worker e estratégia de cache para navegação.
- A abertura dispõe de botão de pular e encerramento temporizado; reprodução automática de áudio não é garantida pelos navegadores.
- O seletor de tradução funcional foi retirado após relato de travamento; bandeiras são apenas indicadores visuais.
- O código contém atributos de acessibilidade e estilos para redução de movimento, mas isso não substitui testes com teclado e leitor de tela.
- O rodapé declara autoria, vínculo ao Tangram e diferencia licença MIT do código dos direitos sobre mídias.
- O script do GA4 com ID G-KXDY9J9N3V está presente; recebimento de eventos deve ser confirmado no relatório Tempo real da propriedade.
- As referências relativas explícitas de mídia encontradas em atributos src/href apontam para arquivos do repositório; o prefixo `assets/carl/` isolado não representa arquivo e não é falha. URLs remotas e URLs construídas por JavaScript requerem verificação adicional.

### Correções realizadas nesta rodada

- Tradução residual em inglês do botão de narração corrigida para português.
- Aviso de licença e direitos de terceiros acrescentado ao rodapé.
- Documento de auditoria e critérios de validação registrado no próprio repositório.

## Pendências de prioridade alta

1. **Teste de estabilidade**: abrir, navegar por todas as seções, trocar astros, usar laboratórios e voltar ao portal em Android, Chromebook e desktop; registrar console e eventuais travamentos.
2. **Abertura e áudio**: verificar comportamento com som permitido, bloqueado e sem rede; hospedar uma cópia autorizada e durável da narração no repositório ou em armazenamento estável. O URL atual usa um endereço de pré-visualização externa e não é garantia de permanência.
3. **Curadoria científica**: verificar individualmente valores numéricos, unidades, época das observações, créditos e links das fotografias (inclusive a foto atribuída ao cometa Halley); distinguir fotografia, simulação e arte.
4. **Acessibilidade**: verificar foco visível, contraste, navegação apenas por teclado, leitores de tela e preferência por movimento reduzido.
5. **Privacidade**: documentar GA4, consentimento e finalidade de geolocalização facultativa; avaliar requisitos da LGPD e regras da escola antes do uso com estudantes.

## Melhorias estruturais posteriores

- Separar progressivamente dados científicos, CSS e JavaScript do HTML principal, com testes de regressão antes de cada alteração.
- Criar roteiro pedagógico e instrumentos simples de avaliação da aprendizagem, sem prejudicar a exploração livre.
- Retomar tradução apenas por dicionários de conteúdo e interfaces testados; não usar observadores que reescrevam continuamente os textos da página.
- Validar PWA em primeira instalação, atualização de versão e uso sem internet.

## Critério para declarar versão final homologada

A homologação exige: ausência de erros bloqueantes em dispositivos-alvo, fontes científicas verificadas, áudio e navegação com comportamento previsível, acessibilidade mínima testada e política de privacidade adequada ao contexto escolar.

## Continuação da auditoria — revisão 2 (10/11/2026)

- Corrigido o foco inicial da abertura e o retorno do foco ao botão de rever a apresentação quando o usuário a pula por teclado.
- Atualizada a identificação do cache PWA de v4 para v5, forçando renovação do conjunto básico de arquivos na ativação do service worker.
- Inspecionadas constantes científicas do código: unidade astronômica `149597870.7 km`, velocidade da luz no vácuo `299792.458 km/s`, ano-luz `9.4607304725808e12 km` e constante gravitacional `6.67430e-11` em SI. Os valores são compatíveis com referências usuais; isso **não** valida automaticamente todos os resultados ou modelos.
- Pendente verificar URL, origem e licença da fotografia atribuída ao cometa Halley, além de outras imagens externas. Não substituir arquivos sem referência verificada.
- Pendente validar comportamento do áudio externo quando o navegador bloqueia autoplay ou a URL deixa de funcionar.
- Pendente teste manual em Android/Chromebook/desktop e validação com leitores de tela; não declarar testes concluídos sem execução.
