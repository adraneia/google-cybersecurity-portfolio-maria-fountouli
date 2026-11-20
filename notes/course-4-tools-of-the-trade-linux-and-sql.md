# Course 4: Tools of the Trade, Linux and SQL

## Module 1: Operating systems
- **OS** = interface between hardware and user. Windows, macOS (closed source), Linux (open source), ChromeOS, Android, iOS.
- **Boot process:** BIOS/UEFI → bootloader → OS.
- **Virtual machines** = virtual computers inside a physical one. Useful for testing malware safely (sandbox).
- **GUI** vs **CLI**. The CLI is faster and keeps a history of commands.
- Legacy OS = old OS still in use. A security risk because it doesn't get updates.

## Module 2: The Linux OS
- Architecture: **user → applications → shell → FHS → kernel → hardware**.
- **Kernel** = core of the OS, manages processes and memory.
- **Shell** = command line interpreter. Bash is the default in most distributions.
- **Distributions:** Kali Linux (penetration testing, digital forensics), Ubuntu, Parrot, Red Hat (RHEL), AlmaLinux.
- **Package managers:** apt / dpkg (Debian, Ubuntu, Kali), yum / rpm (Red Hat).
- Linux standard input → **stdin**, output → **stdout**, errors → **stderr**.

## Module 3: Linux commands in Bash
**Navigation:**

| Command | What it does |
|---|---|
| `pwd` | shows current directory |
| `ls` / `ls -la` | lists files, including hidden, with permissions |
| `cd` | changes directory |
| `cat`, `head`, `tail`, `less` | read file content |

**Filtering:**
- `grep` searches for a string in a file. `grep error log.txt`
- `|` (pipe) sends the output of one command to the next. `ls /home | grep analyst`
- `find /home -name "*.log"`, `find -mtime -3` (changed in the last 3 days)

**File management:** `mkdir`, `rmdir`, `touch`, `rm`, `mv`, `cp`, `nano` (text editor), `>` overwrite, `>>` append.

**Permissions:**
- `-rwxrw-r--` → type, **user**, **group**, **other**. r = read, w = write, x = execute.
- `chmod` changes permissions. `chmod g-w file.txt`, `chmod u+x script.sh`
- Hidden files start with `.`
- **Principle of least privilege** applies to files too.

**Users:** `sudo` (run as root, only for users in the sudoers file), `useradd`, `userdel`, `usermod`, `chown`.

**Help:** `man`, `whatis`, `apropos`.

## Module 4: Databases and SQL
- **Relational database** = tables with rows (records) and columns (fields).
- **Primary key** = unique per row. **Foreign key** = links to a primary key in another table.
- **SQL** queries:
```sql
SELECT username, login_date FROM log_in_attempts
WHERE success = FALSE AND login_time > '18:00';
```
- Operators: `=`, `<>`, `>`, `<`, `BETWEEN`, `LIKE` with `%` (any characters) and `_` (one character), `AND`, `OR`, `NOT`.
- `ORDER BY` (ASC/DESC)
- **Joins:**
  - **INNER JOIN**: only matching rows
  - **LEFT JOIN** / **RIGHT JOIN**: all rows from one side
  - **FULL OUTER JOIN**: everything
- Aggregate functions: `COUNT`, `AVG`, `SUM`.
- Used in security for: failed logins after hours, logins from certain countries, finding machines that need updates.
