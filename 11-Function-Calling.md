# 🔌 Function Calling & Tool Use (AI එකක් බාහිර මෙවලම් භාවිතා කිරීම)

සාමාන්‍යයෙන් Large Language Model (LLM) එකකට සෘජුවම පරිගණකයක තියෙන Functions Run කරන්න, Database එකකට දත්ත ඇතුළත් කරන්න, හෝ බාහිර APIs සමඟ සම්බන්ධ වන්න බැහැ. 

නමුත් **Function Calling** (හෝ Tool Use) සංකල්පය මඟින් AI මොඩලයකට තමන්ට තනියම කළ නොහැකි කාර්යයක් ආ විට, ඒ සඳහා බාහිර මෙවලමක් (Tool) භාවිතා කළ යුතු බව තේරුම් ගැනීමේ හැකියාව ලැබෙනවා.

---

## 🧠 1. Function Calling වැඩ කරන්නේ කොහොමද?

1. **Developer Defines Tools:** ඩෙවලොපර් විසින් කෝඩ් එක ඇතුළත තියෙන Functions (උදා: `send_email()`, `check_weather()`) මොනවාද සහ ඒවා ක්‍රියා කරන්නේ කෙසේද යන්න විස්තර සහිතව (JSON Schema එකක් මඟින්) LLM එකට හඳුන්වා දෙනවා.
2. **AI Decides:** යූසර් ප්‍රශ්නයක් ඇසූ විට (උදා: *"අද කොළඹ කාලගුණය කොහොමද?"*), AI එක තේරුම් ගන්නවා තමන්ට Live weather මතක නැති නිසා `check_weather(location="Colombo")` කියන Function එක පාවිච්චි කළ යුතුයි කියා.
3. **AI Returns JSON:** AI එක විසින් කෙලින්ම function එක run කරන්නේ නැත. ඒ වෙනුවට එය විසින් `"function_name": "check_weather", "arguments": {"location": "Colombo"}` ලෙස JSON Output එකක් අපේ Code එකට ලබා දෙනවා.
4. **Code Executes:** අපේ Backend Code එක (Python/Next.js) මඟින් ඒ JSON එක කියවා සැබෑ API එකට කතා කර උත්තරය ලබාගෙන, එය නැවත AI එකට ලබා දෙනවා.
5. **Final Response:** AI එක ඒ දත්ත කියවා යූසර්ට සරල සිංහලෙන් හෝ ඉංග්‍රීසියෙන් පිළිතුර ලබා දෙනවා.

---

## 📊 සාමාන්‍ය Chatbot සහ Function Calling Chatbot අතර වෙනස

* **සාමාන්‍ය Chatbot:** *"මට 4839 * 2948 කීයද කියන්න"* කියා ඇසූ විට, AI එක තමන්ගේ මතකයෙන් අනුමාන කර වැරදි ගණිතමය පිළිතුරක් (Hallucination) ලබා දීමට ඉඩ ඇත.
* **Function Calling Chatbot:** ගණිත ගැටලුව දුටු වහාම, AI එක තමන් සතු `calculator()` මෙවලම තෝරාගෙන, නිවැරදිම ගණනය කිරීම සිදු කර පිළිතුර ලබා දෙයි.

---

## 🚀 සැබෑ ලෝකයේ භාවිතයන් (Real-world Use Cases)

* **AI Customer Support:** යූසර් කෙනෙක් තමන්ගේ Order එක Cancel කරන්න කිව්වාම, AI එක විසින් Backend ඩේටාබේස් එකේ Function එකක් Run කර Order එක Cancel කිරීම.
* **Smart Assistants:** වත්මන් වෙළඳපොලේ ඇති ස්මාර්ට් උපාංග (උදා: IoT Smart Home) සමඟ සම්බන්ධ වී නිවසේ විදුලි බුබුළු නිවා දැමීමට හෝ දැල්වීමට AI එකට හැකියාව ලැබීම.
