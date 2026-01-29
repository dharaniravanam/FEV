# FEV - Feature Evaluation & Analysis Tool

Java-based data analysis framework with MySQL, GUI, and AI-powered question generation via [OpenRouter.ai](https://openrouter.ai/).

## Features

- **Data Ingestion**: XML processing
- **Analysis**: Line and map-based questions
- **AI Generation**: Auto-generate questions using LLM
- **Database**: MySQL persistence
- **GUI**: User interface
- **Evaluation**: Benchmarking tools

## Requirements

- Java 8+
- MySQL 5.7+
- OpenRouter.ai API key

## Quick Start

### 1. Database Setup
```bash
mysql -u root -p < src/mysql-init/schema.sql
```

### 2. Configure
Edit `config.properties`:
```properties
db.host=localhost
db.user=root
db.password=your_password
openrouter.api.key=your_api_key
```

### 3. Compile
```bash
javac -d bin -sourcepath src src/**/*.java
```

### 4. Run
```bash
java -cp bin GUI.input
```

## Project Structure

```
src/
├── DataAnalysis/       # Analysis & AI question generation
├── DataInload/         # XML loading
├── DataObject/         # Data models
├── DBConnection/       # Database ops
├── evaluation/         # Evaluation tools
├── GUI/                # Interface
└── mysql-init/         # Schema
```

## Docker

```bash
docker-compose up -d
```

## Troubleshooting

- **DB**: Check MySQL and credentials
- **GUI**: Verify Java version and classpath
- **LLM**: Verify OpenRouter.ai API key and connectivity

---

**Built with**: Java | MySQL | OpenRouter.ai LLM
