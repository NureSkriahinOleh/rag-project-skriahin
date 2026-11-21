
# PostgreSQL RAG Assistant

## Опис проєкту

PostgreSQL RAG Assistant — навчальна RAG-система для інформаційної підтримки розробників під час роботи з СУБД PostgreSQL.

Система призначена для пошуку інформації в офіційній документації PostgreSQL та формування відповідей на запитання користувачів із посиланнями на джерела.

## Джерело даних

- Джерело: офіційна документація PostgreSQL
- Версія: PostgreSQL 17.10
- Формат: HTML
- Мова: англійська
- Ліцензія: PostgreSQL License

https://www.postgresql.org/docs/17/

## Технологічний стек

- Python
- ChromaDB
- sentence-transformers/all-MiniLM-L6-v2
- Qwen 3.5 4B (Ollama)
- Beautiful Soup 4
- rank_bm25
- Reciprocal Rank Fusion (RRF)
- pytest

## Встановлення

### Вимоги

- Python 3.11 або новіша сумісна версія
- Git
- Ollama

### Клонування репозиторію

```bash
git clone https://github.com/NureSkriahinOleh/rag-project-skriahin.git
cd rag-project-skriahin
```

### Створення віртуального середовища

```bash
python -m venv .venv
```

Активація у Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### Встановлення залежностей

```bash
pip install chromadb sentence-transformers beautifulsoup4 rank-bm25 ollama pytest
```

### Встановлення моделі генерації

Спочатку необхідно встановити Ollama:

https://ollama.com/download

Далі завантажити модель:

```bash
ollama pull qwen3.5:4b
```

## Структура проєкту

- `src/ingestion/` — завантаження та очищення документів.
- `src/embeddings/` — створення векторних представлень.
- `src/retrieval/` — пошук релевантних фрагментів.
- `src/generation/` — генерація відповідей.
- `config/` — конфігураційні файли.
- `reports/` — звіти з лабораторних робіт.

