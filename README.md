# SmokeLine 2.0

**Um guia de utilitários táticos para Counter-Strike 2.**

O SmokeLine é um aplicativo Android desenvolvido para facilitar o aprendizado e a consulta de granadas táticas no Counter-Strike 2 (CS2), reunindo tutoriais de smokes, flashes e outros recursos estratégicos em uma interface intuitiva e organizada.

A versão 2.0 está sendo reconstruída do zero com foco em arquitetura de software, manutenibilidade, qualidade de código e uma experiência moderna utilizando Jetpack Compose.

> **Status:** Em desenvolvimento.

## Sobre o projeto

O SmokeLine nasceu com a proposta de tornar o aprendizado de utilitários no CS2 mais acessível, permitindo que os jogadores encontrem referências para melhorar suas estratégias durante as partidas.

A versão 2.0 representa uma reestruturação completa do aplicativo, adotando uma arquitetura organizada em camadas e tecnologias modernas do ecossistema Android.

### Objetivos

- Organizar tutoriais de utilitários por mapa e categoria.
- Facilitar o acesso a referências estratégicas durante o aprendizado.
- Permitir que usuários salvem tutoriais para consultar posteriormente.
- Oferecer autenticação e gerenciamento de conta.
- Construir uma base de código escalável, testável e de fácil manutenção.

## Funcionalidades planejadas

- Autenticação com e-mail e senha.
- Cadastro de usuários.
- Recuperação de senha.
- Página inicial com acesso às funcionalidades.
- Catálogo de mapas do CS2.
- Tutoriais de smokes e flashes.
- Sistema de favoritos e conteúdos salvos.
- Configurações e gerenciamento de conta.
- Suporte a português e inglês.
- Autenticação com Google.

*As funcionalidades serão implementadas progressivamente ao longo do desenvolvimento.*

## Tecnologias e ferramentas

| Tecnologia | Aplicação |
|---|---|
| Kotlin | Linguagem principal |
| Jetpack Compose | Construção das interfaces |
| MVVM | Organização da camada de apresentação |
| Clean Architecture | Separação de responsabilidades |
| Firebase Authentication | Autenticação de usuários |
| Navigation Compose | Navegação entre telas |
| Hilt | Injeção de dependências |
| Git e GitHub | Versionamento e colaboração |

*As tecnologias e integrações serão configuradas conforme a evolução do projeto.*

## Arquitetura

O projeto utiliza uma organização por funcionalidades (*feature-based*), com separação de responsabilidades entre as camadas da Clean Architecture.

```text
com.thiagocastagnoli.smokeline/
├── core/
│   ├── common/
│   ├── designsystem/
│   └── navigation/
│
├── features/
│   ├── login/
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   ├── register/
│   ├── forgotPassword/
│   ├── homePage/
│   ├── maps/
│   ├── flashes/
│   ├── saved/
│   └── settings/
│
└── MainActivity.kt
```

A estrutura representa a organização proposta para o projeto e poderá evoluir conforme as necessidades de cada funcionalidade.

### Responsabilidades das camadas

**Presentation**
- Telas construídas com Jetpack Compose.
- ViewModels responsáveis pelo estado e pelas ações da interface.
- Estados de UI e tratamento de eventos.

**Domain**
- Entidades e regras de negócio.
- Interfaces dos repositórios.
- Casos de uso que representam operações específicas da aplicação.

**Data**
- Implementações dos repositórios.
- Fontes de dados remotas ou locais.
- Integração com serviços externos, incluindo Firebase quando aplicável.
- Conversão entre modelos de dados e modelos de domínio.

A proposta é manter as regras de negócio independentes dos detalhes da interface e das fontes de dados, facilitando testes, manutenção e evolução.

## Interface e experiência do usuário

O aplicativo busca oferecer uma experiência visual moderna, consistente e intuitiva, com atenção à legibilidade, à navegação e à organização dos conteúdos.

As interfaces serão desenvolvidas com Jetpack Compose, priorizando componentes reutilizáveis e uma identidade visual coerente com o tema do projeto.

### Screenshots

As capturas de tela serão adicionadas conforme as funcionalidades e as interfaces forem concluídas.

## Requisitos de desenvolvimento

- Android Studio compatível com a versão do Android Gradle Plugin utilizada pelo projeto.
- JDK compatível com a configuração do Gradle.
- SDK Android correspondente às versões configuradas no projeto.
- Conta e projeto Firebase para os serviços de autenticação.

## Desenvolvimento e versionamento

O projeto é desenvolvido com Git e GitHub, buscando manter um histórico de alterações organizado e facilitar a evolução incremental da aplicação.

A organização do desenvolvimento prioriza:

- Commits claros e descritivos.
- Separação de funcionalidades por responsabilidade.
- Código legível e de fácil manutenção.
- Evolução incremental da arquitetura.
- Testes e validação das funcionalidades à medida que forem implementadas.

## Autor

**Thiago Murilo Castagnoli Alves**

Desenvolvedor Android com foco em Kotlin, desenvolvimento de interfaces modernas e arquitetura de aplicações móveis.

- GitHub: [@ThiagoCastagnoli](https://github.com/ThiagoCastagnoli)
- LinkedIn: [Thiago Castagnoli](https://linkedin.com/in/thiago-castagnoli-200210306/)

---

O SmokeLine 2.0 é um projeto de portfólio desenvolvido com o objetivo de aprofundar conhecimentos em desenvolvimento Android e boas práticas de engenharia de software.

*Counter-Strike 2 e seus respectivos elementos são propriedade de seus titulares. SmokeLine é um projeto independente, sem afiliação oficial com a Valve.*
