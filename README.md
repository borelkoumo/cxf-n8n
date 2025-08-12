# Quick Start: Run Your n8n Node Locally

**1️⃣ Install n8n globally**

```bash
npm install -g n8n
```

**2️⃣ Create a custom extensions directory**

```bash
mkdir -p ~/.n8n/custom
cd ~/.n8n/custom
npm init -y
```

**3️⃣ Build and link your node** (replace `cxf-kafka-node` with your project folder)

```bash
cd ~/cxf-kafka-node
npm run build
npm link
```

**4️⃣ Link your node to your local n8n**

```bash
cd ~/.n8n/custom
npm link cxf-kafka-node
```

**5️⃣ Start n8n**

```bash
n8n start
```

**6️⃣ Test in the browser**

* Open n8n in your browser
* Search for the **node name** (e.g., `Cxf Kafka`, `Cxf Kafka Trigger`), *not* the package name (`n8n-nodes-cxf-kafka`)

---

Note:
- By default, the custom directory location is `~/.n8n/custom`.  You can change the location by setting the N8N_CUSTOM_EXTENSIONS environment variable.
- You must create the custom directory manually
