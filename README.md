<div dir="rtl">

# Build Along | افهم الشغل وإنت ماشي

سكيل من إسلام الوزير لأي حد بيتعلّم وهو بيركّب مشروع أو بيربط خدمة. بتخلّي المساعد يشرح بالبلدي هو عمل إيه، ليه، إزاي تتأكد إن الخطوة نجحت، وإيه الخطر الفعلي لو فيها صلاحيات أو تغيير في بيانات. جواها مثال تطبيقي على ClinicDesk.

## الاستخدام

فك ضغط الحزمة وانسخ فولدر `build-along` كامل للمكان المناسب في مشروعك.

| الأداة | مكان فولدر السكيل جوه مشروعك | مثال للتشغيل |
|---|---|---|
| Codex | `.agents/skills/build-along/` | `$build-along اشرح لي تركيب المشروع خطوة بخطوة.` |
| Claude Code | `.claude/skills/build-along/` | `/build-along اشرح لي تركيب المشروع خطوة بخطوة.` |
| Google Antigravity | `.agents/skills/build-along/` | `/build-along اشرح لي تركيب المشروع خطوة بخطوة.` |

لو المساعد بتاعك بيقرا ملفات ومفيهوش قائمة سكيلز، افتح فولدر المشروع معاه وقل له «اقرأ ملف `build-along/SKILL.md` واتبع أسلوبه في شرح الخطوة اللي أنا فيها». حط الفولدر في مكان يقدر المساعد يقراه.

## مثالين تبدأ بيهم

- «بص على ملفات ClinicDesk، وامشي معايا في ربط الشيت. قولّي أعمل إيه وأتأكد من النتيجة إزاي.»
- «اقرأ دليل مشروعي وفهّمني الاعتماد ده بيدي أنهي صلاحية. أنا اللي هنفّذ، فاديني أول خطوة أعملها.»

طريقة التركيب طالعة من توثيق الأدوات ومواصفة Agent Skills. [Codex](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills) · [Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load) · [Antigravity](https://antigravity.google/docs/skills) · [المواصفة](https://agentskills.io/specification)

</div>
