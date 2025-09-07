# Guia de Governança, Conformidade e Melhores Práticas no Azure

## Projeto Governança e Conformidade - Bootcamp AZ900

A governança na nuvem Azure é uma disciplina fundamental que visa estabelecer um equilíbrio entre a agilidade para inovar e a necessidade de manter o controle, a segurança e a conformidade organizacional. Não se trata de criar barreiras, mas sim de construir "guard-rails" inteligentes que permitem às equipes trabalhar de forma autônoma e segura.

## A Base da Confiança: Service Trust Portal

A base de toda essa estratégia começa com a confiança na própria plataforma. É aqui que entra o **Portal de Confiança do Serviço (Service Trust Portal)**. Este portal é o repositório centralizado da Microsoft onde a empresa demonstra sua postura de conformidade. Nele, você encontra:
* Uma vasta biblioteca de relatórios de auditoria de terceiros (como SOC 1, 2, 3 e ISO/IEC 27001).
* Documentação detalhada sobre as práticas de segurança e privacidade da Microsoft.
* Guias que mapeiam os controles da Azure com centenas de **certificações, regulamentos e padrões** globais e setoriais (GDPR, PCI DSS, HIPAA, etc.).

Ele é a prova documental de que a Microsoft cumpre sua parte no modelo de responsabilidade compartilhada.

## Organização e Proteção: Grupos de Recursos e Bloqueios

Com a confiança na plataforma estabelecida, a responsabilidade se volta para como você organiza e protege seus próprios recursos.

* **Grupos de Recursos (Resource Groups):** São o alicerce da governança. Um grupo de recursos é um contêiner lógico que agrupa recursos relacionados de uma solução (VMs, armazenamento, redes) para gerenciar seu ciclo de vida, permissões (RBAC) e custos de forma unificada.

* **Bloqueios (Locks):** Para proteger recursos críticos contra modificações ou exclusões acidentais, mesmo por administradores, o Azure oferece os bloqueios. Existem dois tipos:
    * `ReadOnly`: Impede qualquer alteração no recurso.
    * `CanNotDelete`: Permite modificações, mas impede a exclusão.

## Automação da Conformidade: Azure Policy

Subindo um nível, as **Políticas do Azure (Azure Policy)** permitem a automação e a aplicação de regras em escala. Se o RBAC define *quem* pode fazer *o quê*, a política define *o que* pode ser feito.

As políticas avaliam continuamente os recursos para garantir a **conformidade** com os padrões corporativos. Por exemplo, você pode criar políticas para:
* Obrigar o uso de tags específicas para alocação de custos.
* Restringir a criação de recursos a determinadas regiões geográficas.
* Permitir apenas tamanhos específicos de máquinas virtuais.
* Exigir que o tráfego HTTPS seja habilitado em contas de armazenamento.

O Azure oferece "Iniciativas" (conjuntos de políticas) que mapeiam controles a regulamentos como NIST ou ISO 27001, fornecendo um painel de conformidade em tempo real.

## Governança de Dados: Microsoft Purview

A governança moderna vai além da infraestrutura e foca nos dados. É aqui que o **Microsoft Purview** se torna essencial. O Purview é um serviço de governança de dados unificado para gerenciar seus dados on-premises, no Azure e em outras nuvens.

Seu processo envolve:
1. **Descoberta e Varredura:** O Purview se conecta às suas fontes de dados (Banco de Dados SQL, Data Lake, Power BI) e as varre.
2. **Classificação:** Durante a varredura, ele descobre metadados e identifica automaticamente informações confidenciais (PII), como números de cartão de crédito ou CPFs.

O resultado é um mapa holístico dos seus **dados de governança**, mostrando a linhagem dos dados e onde residem as informações mais sensíveis. Do ponto de vista da **segurança**, essa visibilidade é inestimável para aplicar os controles de acesso e proteção corretos.

## Conclusão: Governança em Camadas

Uma estratégia de governança e conformidade robusta no Azure é construída em camadas:
- Começa com a **confiança** na plataforma (Portal de Confiança).
- Organiza-se com **controles** fundamentais (Grupos de Recursos e Bloqueios).
- É dimensionada e automatizada com **regras** (Políticas do Azure).
- Alcança a profundidade necessária ao governar o **próprio dado** (Microsoft Purview).

Essa abordagem garante uma operação segura, compatível e alinhada às melhores práticas da indústria.
