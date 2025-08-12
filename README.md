# zoran-memory-vault

**Coffre-fort de mémoire** pour l’écosystème Zoran / QuantaGlottal©® — archivage sécurisé, versionné et filtré des glyphes, états et journaux des agents.

---

## ✨ Fonctionnalités
- **Stockage longue durée** des glyphes et snapshots d’agents
- **Versioning complet** (historique, diffs, rollback)
- **Politiques TTL** (Time-To-Live) configurables
- **Indexation** pour recherche rapide (hash, métadonnées, date)
- **Chiffrement au repos** (AES-256) et en transit (TLS)
- **Export** vers formats standards (JSON, YAML, Parquet)
- **Compatibilité multi-backends** : fichiers locaux, S3, bases NoSQL

---

## 📦 Installation (développement)
```bash
pip install -e .


---

⚡ Exemple rapide

from zoran_memory_vault import MemoryVault

vault = MemoryVault(storage_path="./vault")

# Sauvegarder un snapshot
snapshot = {"agent": "zoran-core", "state": {"param1": 42}}
vault.save(snapshot, key="2025-08-12T10:00Z")

# Charger un snapshot
data = vault.load("2025-08-12T10:00Z")
print(data)

# Appliquer une politique TTL (7 jours)
vault.apply_ttl(days=7)


---

🧱 Structure suggérée

src/zoran_memory_vault/
  __init__.py
  vault.py            # API principale de stockage
  encryption.py       # chiffrement/déchiffrement
  indexing.py         # indexation et recherche
  policies.py         # TTL et règles de rétention
tests/
  test_vault.py
pyproject.toml
.gitignore
LICENSE
README.md


---

🧪 Tests

pytest -q


---

🔐 Éthique

Le zoran-memory-vault applique le principe vivant > humain en garantissant :

l’intégrité des données stockées

la suppression contrôlée selon politiques éthiques

la confidentialité des informations sensibles



---

📜 Licence

MIT — voir LICENSE.


---

Auteur : Frédéric Tabary — Institut IA
Contact : 0645605023 — Canada, Montréal, France
INSTITUT🦋 IA INC., 7100-380, rue Saint-Antoine Ouest, Montréal (Québec) H2Y 3X7.# zoran-memory-vault
