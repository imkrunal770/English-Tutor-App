# English Tutor App — Setup Steps (mobile se)

## Step 1: API key lo (free)
1. Phone browser mein jao: https://aistudio.google.com/app/apikey
2. Google account se login karo
3. "Create API key" par click karo, key copy kar lo (kisi ko share mat karna)

## Step 2: Key ko code mein daalo
1. Is zip ko extract karo (koi bhi file manager app se — "Extract" option)
2. File open karo: `app/src/main/java/com/krunal/englishtutor/MainActivity.kt`
3. Line dhundo: `const val GEMINI_API_KEY = "PASTE_YOUR_API_KEY_HERE"`
4. `PASTE_YOUR_API_KEY_HERE` ki jagah apni copied key paste karo, save karo

## Step 3: GitHub par upload karo
1. https://github.com par jao, account banao (agar nahi hai)
2. "New repository" par click karo — naam do jaise `english-tutor` — Public rakho — Create karo
3. Us repo ke andar "uploading an existing file" link par click karo
4. Extract ki hui poori `EnglishTutor` folder ke andar ka saara content (sab files/folders) select karo aur upload karo
   - Zaroori: folder structure preserve rehni chahiye (`.github/workflows/build.yml`, `app/...` waisa hi)
5. "Commit changes" par click karo

## Step 4: Build automatically start ho jaayega
1. Repo ke andar "Actions" tab par jao
2. "Build APK" workflow chal raha dikhega (2-4 minute lagenge)
3. Green tick aane ke baad, us run par click karo
4. Neeche "Artifacts" section mein "EnglishTutor-app" dikhega — usse download karo (ye ek zip hai jisme APK hai)

## Step 5: Phone pe install karo
1. Downloaded zip ko extract karo — `app-debug.apk` milega
2. Us file par tap karo install karne ke liye
3. Agar "Install blocked" dikhe: Settings → "Install unknown apps" → apne browser/file manager ko allow karo
4. Install ho jaayega — app kholo aur English practice shuru karo!

## Notes
- Ye APK Google's free Gemini API use karta hai — free tier mein daily limited requests milti hain (personal use ke liye kaafi hai)
- API key seedhe app ke andar hai — isliye ye APK kabhi bhi Play Store ya public log ke saath share mat karna, sirf apne phone ke liye hai
- Har naye "push" (upload/commit) par naya build automatically ban jaayega — future changes ke liye bhi yehi process
