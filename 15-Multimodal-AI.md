# 👁️ Multimodal AI & Vision Language Models (පින්තූර, වීඩියෝ සහ ශබ්ද තේරුම් ගන්නා AI)

ආරම්භක අවධියේ තිබූ Large Language Models (LLMs) වලට තේරුම් ගත හැකි වූයේ Text (අක්ෂර) පමණි. නමුත් වර්තමානයේ ඇති **Multimodal AI** පද්ධති වලට Text වලට අමතරව Images, Audio, සහ Video යන ඕනෑම මාධ්‍යයක් (Multiple Modalities) එකවර කියවා තේරුම් ගැනීමේ හැකියාව පවතී.

පින්තූර සහ දෘශ්‍ය මාධ්‍යයන් විශ්ලේෂණය කිරීමට විශේෂයෙන් පුහුණු කළ මොඩලයන් **Vision Language Models (VLMs)** ලෙසද හඳුන්වයි (උදා: GPT-4o, Gemini 1.5 Pro, Claude 3.5 Sonnet).

---

## 🧠 1. Multimodal AI එකක් වැඩ කරන්නේ කොහොමද?

සාමාන්‍ය Text එකක් Tokenize කර ඉලක්කම් බවට පත් කරනවා සේම, පින්තූර හෝ ශබ්ද AI එකකට තේරුම් ගැනීමට නම් ඒවාද ගණිතමය Vectors බවට පරිවර්තනය කළ යුතුය:

1. **Vision Encoders (ViT - Vision Transformers):** අපි ලබාදෙන පින්තූරය කුඩා කොටස් වලට (Patches) කඩා, ඒ සෑම කොටසක්ම ගණිතමය Embeddings බවට පත් කරයි.
2. **Audio Encoders:** Voice notes හෝ ශබ්ද තරංග වල සංඛ්‍යාතයන් (Spectrograms) කියවා ඒවා දත්ත බවට පරිවර්තනය කරයි.
3. **Shared Semantic Space:** මේ ආකාරයට පරිවර්තනය කරගත් පින්තූර, ශබ්ද සහ වචන වල Embeddings සියල්ලම එකම ගණිතමය අවකාශයකට (Space එකකට) ගෙන එයි. 
   * *උදාහරණයක් ලෙස:* "බල්ලා" කියන වචනයේ Vector එකත්, බල්ලෙකුගේ පින්තූරයක Vector එකත්, බල්ලෙකු බුරන ශබ්දයේ Vector එකත් එකිනෙකට ඉතා ආසන්නයෙන් පිහිටන පරිදි AI එක තේරුම් ගනියි.

---

## 🚀 2. Full-Stack Developers ලට මෙහි ඇති ප්‍රයෝජන

* **Automated OCR & Data Extraction:** සාමාන්‍ය OCR Tools පාවිච්චි නොකර, සංකීර්ණ Invoices, Receipts, හෝ අත් අකුරු වලින් ලියූ බිල්පත් වල පින්තූරයක් AI එකට ලබා දී, ඒවායේ ඇති දත්ත නිවැරදිව JSON Format එකකට ලබා ගැනීම.
* **UI/UX to Code Conversion:** අපි කොළයක ඇඳගත්තු Design (Wireframe) එකක හෝ Screenshot එකක පින්තූරයක් AI එකට ලබා දී, එයට අදාළ React / Tailwind CSS කෝඩ් එක ක්ෂණිකව ලියා ගැනීම.
* **Smart Content Analysis:** පැය ගණනක CCTV හෝ YouTube වීඩියෝවක් AI එකට Upload කර, "මේ වීඩියෝ එකේ රතු පාට කාර් එකක් යන්නේ කීවෙනි විනාඩියේද?" වැනි සංකීර්ණ ප්‍රශ්න ඇසීම.

---

## ⚙️ 3. Multimodal API පාවිච්චි කරද්දී සැලකිලිමත් විය යුතු කරුණු

1. **Token Consumption (අධික ටෝකන භාවිතය):** පින්තූරයක් හෝ වීඩියෝවක් API එකක් හරහා යවද්දී සාමාන්‍ය Text එකකට වඩා විශාල Tokens ප්‍රමාණයක් වැය වේ. (ඉහළ Resolution පින්තූර සඳහා වියදම වැඩිය).
2. **Prompt Placement:** පින්තූරයක් සහ Text එකක් එකවර ලබා දීමේදී, මුලින්ම පින්තූරය (Image Part) යොදා ඊට පහළින් ප්‍රශ්නය (Text Instruction) ලිවීමෙන් වඩාත් නිවැරදි පිළිතුරු ලබා ගත හැක.
