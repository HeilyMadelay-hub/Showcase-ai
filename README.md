# Legal Intelligence Assistant

**Legal Intelligence Assistant** is an **AI-powered legal assistant system** that combines:

- 🔍 **Semantic search of court rulings**  
- ✍️ **Contract drafting and refinement**  
- 📄 **Legal contextualization based on case law**

The goal is to demonstrate how artificial intelligence can **support legal practice** by automating repetitive processes and offering legal insights, without replacing the professional.

---

## 🎯 Key Features

### 1️⃣ Semantic search of court rulings

- Enter a query in natural language.
- The system retrieves relevant rulings based on context and content.
- Displays:
  - Court  
  - Year  
  - Legal summary  
  - Key legal basis  

### 2️⃣ Contract generation

- Automatically creates contracts using retrieved case law.
- Clauses drafted with formal legal language.
- Contracts adaptable to different legal scenarios.

### 3️⃣ Guided refinement

- Easily modify contracts:
  - "Make it more conservative"
  - "Add indemnification clause"
  - "Strengthen company position"

---

## 🏗️ Architecture

**Clean Architecture (.NET 8)**:

```
User
  ↓
LegalIntelligence.Api (Web API)
  ↓
LegalIntelligence.Application (Business logic)
  ↓
LegalIntelligence.Domain (Legal entities)
  ↓
LegalIntelligence.Infrastructure (Azure / LLM integrations)
```

- **API**: exposes REST endpoints to clients.
- **Application**: use cases and business rules.
- **Domain**: entities such as `Ruling` and `Contract`.
- **Infrastructure**: integrations with Azure, OpenAI/Gemini, and document storage.

---

## ☁️ Services and Technologies

- **Backend:** ASP.NET Core 8 Web API
- **AI:** LLM (OpenAI / Gemini / Azure OpenAI)
- **RAG:** Embeddings + Vector DB (FAISS or Azure AI Search)
- **Cloud:** Azure App Service, Azure Blob Storage
- **Version control and CI/CD:** GitHub + GitHub Actions

---

## 📂 Project Structure

```
LegalIntelligence.Api/
LegalIntelligence.Application/
LegalIntelligence.Domain/
LegalIntelligence.Infrastructure/
README.md
diagrams/
  architecture.png
```

---

## ⚠️ Legal Disclaimer

This system **does not substitute professional legal advice**.  

The AI functions as a support assistant, providing information and contract drafts based on case law.

---

## 🚀 Usage / Quick Demo

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/legal-intelligence-assistant.git
cd legal-intelligence-assistant
```

### 2. Open the solution

Open the solution in Visual Studio / VS Code.

### 3. Restore packages and build

```bash
dotnet restore
dotnet build
```

### 4. Run the API

```bash
dotnet run --project LegalIntelligence.Api
```

### 5. Test endpoint

Test the `POST /contracts/generate` endpoint by sending JSON with:

```json
{
  "contractType": "Labor dismissal",
  "rulings": [
    {
      "id": "...",
      "court": "...",
      "year": 2021,
      "summary": "...",
      "fullText": "..."
    }
  ]
}
```

---

## 📈 Professional Positioning

This demo showcases:

- ✅ AI integration in legal processes
- ✅ Professional and scalable backend architecture
- ✅ Azure usage for deployment and storage
- ✅ Capability to design high-value legaltech products

---

## 🔮 Roadmap / Future Improvements

- [ ] Integration with Azure AI Search for advanced semantic search
- [ ] Multi-language and international adaptation
- [ ] Authentication and permissions with Azure AD B2C
- [ ] Contract storage and version control

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ for the legal community

⭐ Star this repo if you find it useful!

</div>
