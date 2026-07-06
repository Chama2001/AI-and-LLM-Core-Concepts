# 🛠️ AI Frameworks (LangChain vs LlamaIndex)

අපි කලින් කතා කරපු RAG Systems, AI Agents, සහ Embeddings වැනි සංකල්ප මුල සිටම (from scratch) කෝඩ් කරන්න ගියොත් විශාල කාලයක් ගත වෙනවා වගේම කෝඩ් එක ගොඩක් සංකීර්ණ වෙනවා. 

AI Applications ඉතාමත් ඉක්මනින් සහ පහසුවෙන් නිර්මාණය කරගැනීම සඳහා ලෝකයේ බහුලවම පාවිච්චි කරන ප්‍රධාන මෙවලම් (Frameworks) 2ක් තියෙනවා. ඒ තමයි **LangChain** සහ **LlamaIndex**.

---

## 🦜 1. LangChain කියන්නේ මොකක්ද?

LangChain කියන්නේ AI Models (LLMs) වෙනත් බාහිර මෙවලම් (Tools, APIs, Databases) සමඟ සම්බන්ධ කරමින් සංකීර්ණ සහ බහු-පියවර (Multi-step) කාර්යයන් කළ හැකි Applications සෑදීමට පාවිච්චි කරන Framework එකකි.

* **විශේෂත්වය (Chains & Agents):** මෙහි ප්‍රධානම සංකල්පය තමයි "Chains". එනම් එක පියවරක Output එක ඊළඟ පියවරේ Input එක විදිහට සම්බන්ධ කරමින් දිගු ක්‍රියාවලියක් (Workflow) සැකසීමට ඇති හැකියාවයි. AI Agents හැදීමට මෙය ඉතාමත් ප්‍රසිද්ධයි.
* **හොඳම භාවිතය:** AI Agents, Context-aware Chatbots, සහ විවිධ බාහිර මෙවලම් එකපාර පාවිච්චි කරන සංකීර්ණ AI Apps සඳහා.

---

## 🦙 2. LlamaIndex කියන්නේ මොකක්ද?

LlamaIndex (කලින් GPT Index) කියන්නේ ප්‍රධාන වශයෙන්ම **ලොකු දත්ත ප්‍රමාණයක් (Data Sources) LLM එකක් සමඟ සම්බන්ධ කිරීමට** සහ **RAG Systems** ඉතාමත් කාර්යක්ෂමව නිර්මාණය කිරීමට නිපදවා ඇති Framework එකකි.

* **විශේෂත්වය (Data Ingestion):** අප සතු PDFs, Word Documents, Notion, හෝ SQL Databases වැනි ඕනෑම ආකාරයක දත්ත ඉතාමත් පහසුවෙන් කියවා, ඒවා Chunk කර, Vector Embeddings බවට පත් කර Vector DB එකකට සම්බන්ධ කිරීමේ (Data Ingestion & Indexing) උපරිම හැකියාව මේ Framework එක සතුයි.
* **හොඳම භාවිතය:** Search Engines, Document Q&A Applications, සහ උසස් මට්ටමේ RAG Systems සඳහා.

---

## 📊 LangChain සහ LlamaIndex අතර ප්‍රධාන වෙනස

| ලක්ෂණය | 🦜 LangChain | 🦙 LlamaIndex |
| :--- | :--- | :--- |
| **ප්‍රධාන අවධානය** | AI මොඩලයේ ක්‍රියාකාරීත්වය සහ බාහිර වැඩ (Actions/Agents). | දත්ත හැසිරවීම, Index කිරීම, සහ සෙවීම (Data/RAG). |
| **භාවිතය ලේසි කාටද?** | Generic AI workflows සහ Agents හදන්න. | තමන්ගේම ඩේටා මත Search කරන Apps හදන්න. |
| **ශක්තිමත් පැත්ත** | Multi-Agent Systems සහ Tool Use. | Advanced RAG (Querying, Chunking, Retrieving). |

---

## 💡 සාරාංශය: මම තෝරාගත යුත්තේ කුමක්ද?

* ඔයා හදන්න යන්නේ ඔයා සතු විශාල පොත් පත් හෝ ලිපිගොනු (Documents) කියවලා උත්තර දෙන **ලස්සන RAG Chatbot කෙනෙක් නම් ➡️ LlamaIndex** තෝරාගන්න.
* ඔයා හදන්න යන්නේ තනියම තීරණ අරන්, වෙබ් එක සර්ච් කරලා, Email යවන්න පුළුවන් **ස්වාධීන AI Agent කෙනෙක් නම් ➡️ LangChain** තෝරාගන්න.
