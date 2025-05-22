# pg_patchwatch

🛡️ A lightweight Bash tool to check if your PostgreSQL installation is up to date – locally or inside a Docker container.

## 🚀 Features

- ✅ Checks current PostgreSQL version (local or Docker)
- 🌐 Compares with the latest official minor version from postgresql.org
- 🐳 Supports Docker containers
- 📦 JSON output for automation
- 🧰 No dependencies beyond basic Unix tools (`psql`, `curl`, `grep`, `awk`, `docker` if needed)

---

## 📦 Installation

```bash
curl -o /usr/bin/pg_patchwatch https://raw.githubusercontent.com/Nesterovic-IT-Services-e-U/pg_patchwatch/main/pg_patchwatch
chmod +x /usr/bin/pg_patchwatch
```

🧪 Usage
Check local PostgreSQL:
```bash
pg_patchwatch
```
Check PostgreSQL in Docker container:
```bash
pg_patchwatch my_container_name
```
Output as JSON:
```bash
pg_patchwatch --json
pg_patchwatch my_container_name --json
```
Example output:
```
✅ PostgreSQL 16.9 is up to date.
```
Or:
```
⚠️ PostgreSQL 17.4 is outdated. Latest is 17.5
💡 Consider updating for security and bugfixes.
```
📄 Output in JSON mode
```
{
  "local_version": "17.4",
  "latest_version": "17.5",
  "up_to_date": false,
  "source": "local"
}
```
🔧 Requirements

   - Bash

   - psql in $PATH (or installed in Docker container)

   - curl, grep, awk, sort

   - docker (if using container mode)

📜 License

MIT License © Nesterovic IT-Services e.U.
