🤖 RAG (Retrieval-Augmented Generation) කියන්නේ මොකක්ද?

ChatGPT හෝ Gemini වැනි Large Language Model (LLM) එකකට සාමාන්‍යයෙන් උත්තර දිය හැක්කේ උන්ව Train කරපු Data වලට විතරයි. උදාහරණයක් විදිහට ඔයාගේ සමාගමක රහස් PDF එකක් දුන්නොත් ඒක ගැන උත්තර දෙන්න AI එකට බැහැ.

මෙන්න මේ ප්‍රශ්නය විසඳන්න පාවිච්චි කරන සුපිරිම ක්‍රමවේදයක් තමයි **RAG (Retrieval-Augmented Generation)** කියන්නේ. මේකෙන් කරන්නේ AI Model එකට තමන්ගේම බාහිර ඩේටා (Custom PDFs, Websites, Databases) කියවලා නිවැරදිව උත්තර දීමේ හැකියාව ලබා දීමයි.

🛠️ RAG එකක් ඇතුළතින්ම වැඩ කරන්නේ කොහොමද? (Step-by-Step)

RAG ක්‍රියාවලිය ප්‍රධාන කොටස් 3කට බෙදන්න පුළුවන්,

  1. Data Ingestion & Chunking (දත්ත කැබලි කිරීම)
     මුලින්ම අපි දෙන ලොකු PDF එකක් හෝ Document එකක් කෙලින්ම AI එකට කියවන්න බෑ. ඒ නිසා ඒ Documents පොඩි පොඩි කැබලි වලට (Chunks) කඩා ගන්නවා (උදාහරණයක් ලෙස වචන 500 බැගින් කැබලි කිරීම).

  2. Vector Embeddings (ගණිතමය අගයන් බවට පත් කිරීම)
     මේ කඩාගත්තු හැම Text කැබැල්ලක්ම **Embedding Model** එකක් (උදා: OpenAI Embedding API) හරහා යවලා, ඒ වචන වල තේරුම නිරූපණය වන පරිදි ගණිතමය අංක සමූහයක් (Numbers/Vectors) බවට පත් කරනවා. වචන වල තේරුම අනුව සමාන දේවල් එක        ළඟ පිහිටන විදිහට තමයි මේ Vectors හැදෙන්නේ.

  3. Vector Database
  මේ පරිවර්තනය කරගත්තු Vectors (ගණිතමය අගයන්) ටික අපි **Vector Database** එකක (උදා: Pinecone, ChromaDB, Milvus) Store කරගන්නවා. සාමාන්‍ය SQL DB එකක වගේ නැතුව මෙතනදී ඩේටා Search කරන්නේ "තේරුම" (Semantic Meaning) මත         පදනම්වයි.

🔄 User කෙනෙක් ප්‍රශ්නයක් ඇහුවාම වෙන්නේ මොකක්ද?

1. Query Embedding - User ප්‍රශ්නයක් ඇහුවාම (උදා: "අපේ Company එකේ නිවාඩු ලබාගැනීමේ නීති මොනවාද?"), ඒ ප්‍රශ්නයත් Vector එකක් බවට පත් කරනවා.
2. Vector Search - ඒ ප්‍රශ්නයේ Vector එක Vector Database එකට යවලා, ඒකට වඩාත්ම සමාන තේරුමක් තියෙන Text Chunks (කැබලි) ටික හොයාගන්නවා (Similarity Search).
3. Augmented Generation - දැන් අර හොයාගත්තු අදාළම තොරතුරු ටික සහ Userගේ ප්‍රශ්නය එකතු කරලා (Prompt එකක් හදලා) LLM (ChatGPT/Gemini) එකට යවනවා.
4. Answer - LLM එක ඒ තොරතුරු කියවලා බලලා, ඉතාමත් නිවැරදි උත්තරයක් Userට ලබා දෙනවා.

💡 RAG වල තියෙන වාසි මොනවාද?
* No Hallucinations - AI එක හිතෙන් මවාගෙන බොරු උත්තර දෙන එක ගොඩක් අඩු වෙනවා.
* Cost-Effective - AI Model එකක් මුල ඉඳන් ලොකු මුදලක් දීලා Fine-tune/Train කරන්න ඕන වෙන්නේ නැහැ.
* Up-to-date Data - Live ඩේටා වුණත් ඉක්මනින් Update කරලා AI එකට කියවන්න දෙන්න පුළුවන්.
