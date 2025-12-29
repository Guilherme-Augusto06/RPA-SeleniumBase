# RPA-SeleniumBaseprojeto_rpa/
├── config/
│   ├── __init__.py
│   ├── settings.py
│   ├── logging_config.py
│   └── environment.py
│
├── core/                           # Núcleo reutilizável
│   ├── __init__.py
│   ├── interfaces/                 # Contratos/Abstrações
│   │   ├── browser_interface.py
│   │   ├── repository_interface.py
│   │   └── notification_interface.py
│   │
│   ├── browser/                    # Gerenciamento de navegador
│   │   ├── __init__.py
│   │   ├── browser_factory.py      # Factory pattern
│   │   └── playwright_browser.py   # Alternativa
│   │
│   └── exceptions/
│       ├── __init__.py
│       ├── base_exception.py
│       └── automation_exceptions.py
│
├── domain/                         # Regras de negócio
│   ├── __init__.py
│   ├── entities/                   # Modelos de dados
│   │   ├── usuario.py
│   │   ├── tarefa.py
│   │   └── resultado.py
│   │
│   └── services/                   # Lógica de negócio pura
│       ├── __init__.py
│       ├── validacao_service.py
│       └── processamento_service.py
│
├── infrastructure/                 # Implementações técnicas
│   ├── __init__.py
│   ├── repositories/               # Acesso a dados
│   │   ├── __init__.py
│   │   ├── excel_repository.py
│   │   ├── database_repository.py
│   │   └── api_repository.py
│   │
│   ├── notifications/
│   │   ├── email_notifier.py
│   │   ├── teams_notifier.py
│   │   └── slack_notifier.py
│   │
│   └── logging/
│       ├── file_logger.py
│       └── cloud_logger.py
│
├── application/                    # Casos de uso/Orquestração
│   ├── __init__.py
│   ├── use_cases/
│   │   ├── __init__.py
│   │   ├── processar_pedido_use_case.py
│   │   ├── gerar_relatorio_use_case.py
│   │   └── sincronizar_dados_use_case.py
│   │
│   └── orchestrator/              # Gerenciamento de execução
│       ├── __init__.py
│       ├── task_queue.py
│       ├── worker_pool.py
│       └── scheduler.py
│
├── presentation/                   # Interface com usuário/sistema
│   ├── __init__.py
│   ├── pages/                     # Page Objects (UI)
│   │   ├── __init__.py
│   │   ├── base/
│   │   │   ├── base_page.py
│   │   │   └── page_component.py
│   │   │
│   │   └── modules/               # Agrupado por módulo
│   │       ├── autenticacao/
│   │       │   ├── login_page.py
│   │       │   └── logout_page.py
│   │       │
│   │       └── cadastro/
│   │           ├── formulario_page.py
│   │           └── confirmacao_page.py
│   │
│   └── api/                       # API REST opcional
│       ├── __init__.py
│       ├── routes.py
│       └── controllers.py
│
├── bots/                          # Automações específicas
│   ├── __init__.py
│   ├── bot_pedidos/
│   │   ├── __init__.py
│   │   ├── config.py
│   │   └── executor.py
│   │
│   └── bot_notas_fiscais/
│       ├── __init__.py
│       ├── config.py
│       └── executor.py
│
├── shared/                        # Utilitários compartilhados
│   ├── __init__.py
│   ├── decorators/
│   │   ├── retry.py
│   │   ├── timer.py
│   │   └── error_handler.py
│   │
│   ├── helpers/
│   │   ├── date_helper.py
│   │   ├── string_helper.py
│   │   └── file_helper.py
│   │
│   └── constants/
│       ├── messages.py
│       └── status_codes.py
│
├── tests/
│   ├── unit/                      # Testes unitários
│   │   ├── domain/
│   │   ├── application/
│   │   └── infrastructure/
│   │
│   ├── integration/               # Testes de integração
│   └── e2e/                       # Testes end-to-end
│
├── data/
│   ├── input/
│   ├── output/
│   └── temp/
│
├── logs/
├── drivers/
├── scripts/                       # Scripts auxiliares
│   ├── setup.py
│   └── deploy.py
│
├── docs/                          # Documentação
│   ├── architecture.md
│   └── api.md
│
├── main.py
├── requirements.txt
├── pyproject.toml                 # Poetry
├── docker-compose.yml             # Para containerização
├── Dockerfile
└── README.md