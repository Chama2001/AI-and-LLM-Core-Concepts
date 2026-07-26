# ⚡ LLM Caching (Prompt Caching & Semantic Caching)

Large Language Models (LLMs) මඟින් ක්‍රියාත්මක වන Applications වලදී හැම ප්‍රශ්නයකටම LLM එකට කතා කිරීම (API Call එකක් යැවීම) අධික පිරිවැයක් (High Cost) සහ ප්‍රමාදයක් (High Latency) ඇති කරයි.

පරිශීලකයින් නිරන්තරයෙන් අසන සමාන ප්‍රශ්න වලට AI එක නැවත නැවත ගණනය කිරීමකින් තොරව ක්ෂණිකව පිළිතුරු ලබාදීම සඳහා පාවිච්චි කරන තාක්ෂණය **LLM Caching** ලෙස හඳුන්වයි.

---

## 🧠 1. Caching ක්‍රමවේද 2

* **Exact Match Caching (සමාන ප්‍රශ්න):**
  යූසර් කෙනෙක් අහපු ප්‍රශ්නයම (උදා: *"What is your return policy?"*) වෙනත් යූසර් කෙනෙක් ඇහුවොත්, AI එකට නොයවා කලින් Database/Redis එකේ save වුණු පිළිතුර ලබා දීම.
* **Semantic Caching (තේරුම සමාන ප්‍රශ්න):**
  වචන වෙනස් වුණත් අදහස සමාන නම් (උදා: *"How to return an item?"* සහ *"What is the return process?"*), Vector DB එකක් හරහා ඒ ප්‍රශ්න දෙකේ අදහස සමාන බව (Similarity > 95%) තේරුම් ගෙන කලින් දුන්නු පිළිතුරම ලබා දීම.

---

## 🚀 2. Prompt Caching (Prefix Caching)

ලොකු Context එකක් (උදා: පිටු 100ක Document එකක් හෝ System Prompt එකක්) දිගටම AI එකට යවද්දී, AI Provider (Gemini/Anthropic) විසින් ඒ පරණ Document කොටස **Cache** කර තබා ගනියි.
* **වාසිය:** ඊළඟ ප්‍රශ්න අහද්දී ඒ Document එක නැවත කියවීමට යන පිරිවැය (Cost) 50%-90% ප්‍රමාණයකින් අඩු වන අතර උත්තරය ලැබෙන වේගය (Speed) ඉතාමත් වැඩි වේ.

---

## 📊 LLM Caching වල වාසි

1. **පිරිවැය අඩුවීම (Cost Reduction):** API Tokens පාවිච්චිය 80% දක්වා අඩු කරගත හැක.
2. **වේගවත් වීම (Low Latency):** AI එක උත්තරයක් හදන්න තත්පර 3-5ක් ගන්නවා වෙනුවට milliseconds 50ක් ඇතුළත Cache එකෙන් උත්තරය පෙන්විය හැක.
3. **Rate Limits වලින් බේරීම:** API එකට යන Request ප්‍රමාණය අඩුවන බැවින් Server Overload වීම වැළකේ.
