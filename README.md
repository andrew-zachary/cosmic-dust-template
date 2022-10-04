# Cosmic Dust Template.

Astro.build multilingual template for building websites quickly with a translated UI and Content.
## 🚀 Folders
### `src/components`
Break down a single page into parts each with its own translated content.
<pre>
const content = {
    'en': {
        'title': 'welcome',
        'p': 'Astro.build multilingual template for building websites quickly with a translated UI and Content.'
    },
    'ar': {
        'title': 'أهلاً',
        'p': 'قالب Astro.build متعدد اللغات لإنشاء مواقع الويب بسرعة باستخدام واجهة مستخدم ومحتوى مترجمين.'
    }
};
</pre>
### `src/data`
MDX data files each file contains translated content for a nested singular page.
### `src/images`
Project images to import within code.
### `src/layouts`
Main layouts and reusable components used globally.
### `src/locals`
- First file `meta.json` is to produce targeted languages attributes.
<pre>
{
    "1": {"name": "en", "target": "en", "dir": "ltr"},
    "2": {"name": "ar", "target": "العربية", "dir": "rtl"}
}
</pre>
- Second file `nav.json` is to produce translated slugs and urls for all destinations.
<pre>
{
    "1": {
        "en": {"name": "home", "slug": "", "url": ""},
        "ar": {"name": "إبدأ", "slug": "", "url": ""}
    },
    "2": {
        "en": {"name": "articles", "slug": "articles", "url": "articles/1"},
        "ar": {"name": "مقالات", "slug": "articles", "url": "articles/1"}
    },
    "3": {
        "en": {"name": "test page", "slug": "test-page", "url": "test-page"},
        "ar": {"name": "صفحة إختبار", "slug": "test-page", "url": "test-page"}
    }
}
</pre>
- For example `cats.json` is an entity to be translated and used.
<pre>
{
    "1": {
        "en": {"name": "cat 1", "slug": "cat-1"},
        "ar": {"name": "نوع 1", "slug": "نوع-1"}
    },
    "2": {
        "en": {"name": "cat 2", "slug": "cat-2"},
        "ar": {"name": "نوع 2", "slug": "نوع-2"}
    }
}
</pre>
### `src/pages` and `src/styles`
Normally used to build necessary pages and style them.