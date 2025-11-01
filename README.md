# Boletim do Aluno

Para clonar as duas partes simultaneamente:
- <code>git clone --recursive https://github.com/NodaEng/desafio-tecnico-caed.git</code>

Para iniciar o back end:
- <code>cd desafio-tecnico-caed-back-end</code>
- <code>./mvnw spring-boot:run</code>

Para iniciar o front end (é necessário ter o node instalado no ambiente):
- <code>cd desafio-tecnico-caed-front-end</code>
- <code>npm run start</code>

## Decisões técnicas

Apesar do prazo curto, optei por uma arquitetura robusta o suficiente para que fosse escalável, além de modular.

Como o intuito do sistema era ser um MVP, mantive o front-end bem enxuto, focando principalmente numa "melhoria futura" desse projeto bruto, ao invés de fazer algo que fosse funcionar apenas para esse caso específico.

Essa preocupação refletiu também na estrutura do banco de dados, considerando que não foi explicitado a escolaridade, presumi que deveria ser uma aplicação que pudesse vir a ser usada tanto em salas do primário quanto em faculdades.

Dado a nova feature dos signals que vem sendo desenvolvida pelo time do Angular, tentei implementar no que fosse possível, mas ainda não parece maduro o suficiente num nível de produção, principalmente a integração com os reactiveForms.

À respeito da autenticação, optaria por uma estrutura simples de no máximo três tipos de usuário, sendo administrador, professor e aluno, cada um com sua devida proporção de acesso e controle sobre o sistema. Usaria também as mecânicas do próprio Angular e Spring Boot para interceptar as chamadas.


