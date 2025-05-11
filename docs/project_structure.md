your-project/
├── cmd/                  # 主程序入口
│   └── app/             # 可执行程序1（例如主服务）
│       └── main.go
│   └── cli/             # 可执行程序2（例如命令行工具）
│       └── main.go
├── internal/            # 私有代码（禁止外部项目导入）
│   ├── app/            # 应用层（业务逻辑入口）
│   ├── domain/         # 领域层（核心业务模型）
│   ├── repository/     # 数据访问层（数据库操作）
│   └── service/        # 服务层（业务逻辑实现）
├── pkg/                # 公共库（允许外部项目导入）
│   ├── utils/         # 通用工具函数
│   └── logger/        # 日志模块
├── configs/            # 配置文件（YAML/TOML/JSON等）
│   └── config.yaml
├── scripts/            # 辅助脚本（部署、代码生成等）
├── test/               # 测试相关（Mock数据、集成测试）
├── web/                # 前端相关（静态资源、模板）
├── api/                # API定义（Protobuf/OpenAPI等）
├── docs/               # 文档（设计文档、Swagger）
├── go.mod              # 模块依赖
├── go.sum
├── Makefile            # 常用命令封装
├── README.md           # 项目说明
└── .gitignore


应用程序依赖项(手动管理或使用你喜欢的依赖项管理工具，如新的内置 Go Modules 功能)。
go mod vendor 命令将为你创建 /vendor 目录。

请注意，如果未使用默认情况下处于启用状态的 Go 1.14，则可能需要在 go build 命令中添加 -mod=vendor 标志。
