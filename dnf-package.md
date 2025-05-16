--

### ✅ **Installing a Package with `dnf`**

To install any package (e.g., MySQL, MongoDB, or others):

```bash
sudo dnf install <package-name>
```

Example:

```bash
sudo dnf install mysql-server
```

---

### ✅ **Steps Before Installing**

1. **Check if the package is available:**

```bash
dnf search <package-name>
```

2. **View details of the package:**

```bash
dnf info <package-name>
```

---

### ✅ **Example: Install MySQL 8**

1. **Enable MySQL 8 module:**

```bash
sudo dnf module reset mysql
sudo dnf module enable mysql:8.0
```

2. **Install MySQL:**

```bash
sudo dnf install mysql-server
```

3. **Start & enable service:**

```bash
sudo systemctl enable --now mysqld
```

---

### ✅ **Example: Install MongoDB**

MongoDB is not in the default AppStream repos, so you need to manually add its repo:

```bash
cat <<EOF | sudo tee /etc/yum.repos.d/mongodb-org-6.0.repo
[mongodb-org-6.0]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/\$releasever/mongodb-org/6.0/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-6.0.asc
EOF
```

Then install:

```bash
sudo dnf install -y mongodb-org
```

---

### ✅ **Bonus: Useful `dnf` Commands**

| Command              | Description                    |
| -------------------- | ------------------------------ |
| `dnf list installed` | Show all installed packages    |
| `dnf list available` | Show all available packages    |
| `dnf repolist`       | Show enabled repositories      |
| `dnf module list`    | Show AppStream module packages |
| `dnf clean all`      | Clean cached metadata          |
| `dnf check-update`   | Check for updates              |
| `dnf update`         | Update all packages            |

---
