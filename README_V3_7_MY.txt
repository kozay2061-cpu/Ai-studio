AI Music Studio V3.7 — Chord Timeline + Online AI

ပါဝင်သည့်အရာ
- AI_Music_Studio_V3_7_Chord_Timeline_Online_AI.html
- Chord Timeline: Chord block ကိုနှိပ်လျှင် player သည် အချိန်သို့ရွှေ့နိုင်သည်
- BPM, Key, Duration, estimated bars
- Section markers (Intro/Verse/Chorus စသည်) — အစပိုင်းတွင် ခန့်မှန်းခွဲခြားထားခြင်းဖြစ်ပြီး ကိုယ်တိုင်ပြင်နိုင်သည်
- Cloudflare Worker API ချိတ်ဆက်မှုစမ်းသပ်ခြင်း၊ AI transcription၊ Lyrics အတွက် chord suggestion

အသုံးပြုနည်း (Android)
1. HTML ဖိုင်ကို ဖုန်းထဲ Download လုပ်ပါ။
2. Online AI ကို သုံးရန် HTML ကို file:// မှ တိုက်ရိုက်ဖွင့်ခြင်းထက် HTTPS website အဖြစ် host လုပ်ပါ (ဥပမာ Cloudflare Pages သို့မဟုတ် GitHub Pages)။
3. Website ထဲ MP3/WAV ဖိုင်ရွေးပါ။
4. “အသံကို ခွဲခြမ်းစိတ်ဖြာမယ်” ကိုနှိပ်ပါ။ Chord Timeline နှင့် BPM/Key ရလဒ်ကိုကြည့်ပါ။
5. Online AI Backend ချိတ်ဆက်မှု စမ်းမယ် ကိုနှိပ်ပါ။ Default Worker URL သည် https://late-star-ef0a.sback0065.workers.dev/ ဖြစ်သည်။

Cloudflare Worker ပြင်ဆင်မှု
- Worker Settings > Variables and Secrets တွင် HF_TOKEN ကို Secret အဖြစ် ထည့်ရန်လိုသည်။
- HF_TOKEN မရှိပါက health check တွင် AI token မထည့်ရသေးဟု ပြမည်၊ AI endpoint များ အလုပ်မလုပ်နိုင်ပါ။
- Token ကို HTML ဖိုင်ထဲ မထည့်ပါနှင့်။ Backend ထဲတွင်သာ သိမ်းပါ။
- Worker သည် /api/health, /api/transcribe, /api/chords endpoint များကို ပံ့ပိုးပေးရမည်။

အရေးကြီးသော ကန့်သတ်ချက်များ
- Browser-side BPM/Key/Chord များသည် အခြေခံ signal-processing ခန့်မှန်းချက်များဖြစ်ပြီး အတည်ပြုထားသော transcription မဟုတ်ပါ။
- Section markers များသည် အစပိုင်းတွင် သီချင်းကြာချိန်အလိုက် ခန့်မှန်းထားခြင်းဖြစ်သည်။ အလိုအလျောက်တိကျသော Intro/Verse/Chorus detection ဟု မယူဆပါနှင့်။
- Online AI transcription/chord suggestion အလုပ်လုပ်မှုသည် Worker endpoint နှင့် Hugging Face model/token အခြေအနေပေါ် မူတည်သည်။
- Script syntax ကို စစ်ဆေးပြီးဖြစ်သော်လည်း Android ဖုန်း/Live Worker ပေါ်တွင် အပြည့်အဝ စမ်းသပ်အတည်ပြုထားခြင်း မဟုတ်ပါ။
