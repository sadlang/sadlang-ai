# sadlang-ai

موارد جاهزة لوكلاء الذكاء الاصطناعي للعمل مع **لغة ص** البرمجية — قواعد، أمثلة، تعليمات، مخططات، وتعريفات وكلاء.

> هذا المستودع ليس كودًا تنفيذيًا، بل **حزمة معرفة منظَّمة** (knowledge pack) يستهلكها وكلاء LLM
> لتوليد كود لغة ص وشرحه وإصلاحه وترجمته بدقة.

## البنية

```
sadlang-ai/
├── skills/         # المعرفة المرجعية المكثّفة (القواعد، الأنواع، الملكية، الأخطاء، المكتبة)
│   ├── grammar.md
│   ├── ownership.md
│   ├── types.md
│   ├── errors.md
│   └── stdlib.md
├── examples/       # أمثلة كود قابلة للتشغيل مشروحة
│   ├── basic.md
│   ├── ownership.md
│   ├── types.md
│   └── errors.md
├── instructions/   # تعليمات مهام للوكلاء (اكتب، اشرح، أصلح، ترجم)
│   ├── write-code.md
│   ├── explain-code.md
│   ├── fix-errors.md
│   └── translate.md
├── schemas/        # مخططات بنيوية للغة (YAML) للاستهلاك الآلي
│   ├── grammar.yaml
│   ├── types.yaml
│   └── ownership.yaml
├── prompts/        # قوالب موجّهات جاهزة
│   ├── explain.txt
│   ├── fix.txt
│   └── translate.txt
└── agents/         # تعريفات وكلاء جاهزة (معلّم، مُدقّق، مترجم)
    ├── teacher.json
    ├── linter.json
    └── translator.json
```

## كيف تُستعمل

| الدور | الملفات المعنية |
|-------|------------------|
| **سياق نظام (system prompt)** | `skills/*.md` + `instructions/*.md` |
| **few-shot** | `examples/*.md` |
| **استدلال آلي/تحقّق** | `schemas/*.yaml` |
| **قوالب مهام** | `prompts/*.txt` |
| **وكلاء جاهزون** | `agents/*.json` |

## لغة ص — لمحة

لغة ص لغة برمجة عربية كاملة: الكلمات المفتاحية والدوال المدمجة بالعربية، كتل تُغلَق بـ`نهاية`،
نظام أنواع باستنتاج، برمجة كائنية كاملة، أعمار/ملكية (lifetimes) على نمط Rust، عقود برمجية،
ماكروز، واختبار خصائص. لها مفسّر ومترجم (`sad-build` إلى LLVM).

- المنظومة: [sadlang/s-programming-language](https://github.com/sadlang/s-programming-language)
- دليل المطوّرين: [sadlang/dev-guide](https://github.com/sadlang/dev-guide)
- مقترحات التصميم: [sadlang/rfcs](https://github.com/sadlang/rfcs)

## الترخيص

MIT
