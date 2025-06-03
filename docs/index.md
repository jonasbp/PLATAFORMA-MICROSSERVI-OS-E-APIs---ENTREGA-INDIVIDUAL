# PLATAFORMA MICROSSERVIÇOS E APIs - ENTREGA INDIVIDUAL
JONAS BONFÁ PELEGRINA 2025.1

PROJETO EM GRUPO REALIZADO COM A GIULIA GOMES VALENTE
LINK DO PROJETO EM GRUPO

EXCHANGE

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_exchange

ACCOUNT

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_account

AUTH

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_auth

ORDER

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_order

PRODUCT

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_product

PRODUCT SERVICE

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_product-service

ORDER SERVICE

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_order-service

AUTH SERVICE

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_auth-service

ACCOUNT SERVICE

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_account-service

GATEWAY SERVICE

https://github.com/jonasbp/plataformas_microservicoes_apis_individual_gateway-service

# BOTTLENECKS

# Observabilidade no EKS com AWS CloudWatch

![Descrição da imagem](assets/images/eks.png)

Para garantir a observabilidade e o monitoramento da nossa aplicação executada no Amazon EKS, utilizamos o serviço AWS CloudWatch, que é a ferramenta nativa da AWS para coleta de métricas, logs e eventos.

Realizamos toda a configuração de integração entre o EKS e o CloudWatch, o que nos permitiu:
	•	Monitorar o desempenho dos pods e containers em tempo real;
	•	Visualizar métricas como uso de CPU, memória e status dos serviços;
	•	Configurar alertas automáticos para falhas ou comportamentos fora do esperado;
	•	Analisar logs centralizados para facilitar a identificação e resolução de problemas.

Com isso, conseguimos ter visibilidade completa do ambiente e maior segurança na operação da nossa aplicação em produção.

FOTOFOTO

# Uso de Load Balancer com EKS na AWS

![Descrição da imagem](assets/images/load.png)


Em nossa arquitetura com Amazon EKS, utilizamos um Load Balancer (balanceador de carga) para distribuir o tráfego de forma eficiente entre os pods da aplicação. Essa configuração foi essencial para garantir alta disponibilidade, resiliência e escalabilidade no acesso ao sistema.

A integração foi feita da seguinte forma:
	•	Criamos um Load Balancer externo (ELB ou ALB) automaticamente por meio de um Ingress Controller (como o AWS Load Balancer Controller).
	•	Configuramos as rotas e serviços no Kubernetes para direcionar o tráfego corretamente.
	•	Com isso, o Load Balancer distribui as requisições entre os pods ativos, garantindo que nenhum nó fique sobrecarregado.
	•	Também foi possível configurar SSL/TLS, regras de roteamento e verificações de saúde (health checks) para manter a aplicação segura e estável.

Essa abordagem nos permitiu escalar horizontalmente com facilidade e oferecer uma experiência de acesso confiável para os usuários finais.

# Análise de Vulnerabilidades com SonarQube

![Descrição da imagem](assets/images/sonar.png)


Para reforçar a segurança e a qualidade do nosso código, integrarmos nosso repositório ao SonarQube, uma ferramenta amplamente utilizada para análise estática de código. Com isso, conseguimos realizar vulnerability scanning e identificar problemas de segurança, bugs e más práticas logo nas primeiras etapas do desenvolvimento.

Os principais benefícios dessa integração foram:
	•	Detecção automática de vulnerabilidades e códigos inseguros;
	•	Análise contínua a cada push no repositório, integrando com nosso fluxo de CI/CD;
	•	Relatórios claros e detalhados, com sugestões de correção;
	•	Monitoramento de cobertura de testes, duplicações, complexidade e padrões de código.

Essa prática garantiu maior confiabilidade e segurança ao nosso software, além de facilitar a manutenção e evolução do sistema ao longo do tempo.

