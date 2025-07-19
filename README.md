from pathlib import Path

# محتوى ملف RSS بصيغة XML
rss_content = '''<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
  <channel>
    <title>خدمات الإعلام الآلي</title>
    <link>https://example.com/university-feed</link>
    <description>أخبار وتفاصيل التسجيلات الجامعية 2026/2025</description>
    <language>ar-dz</language>
    <item>
      <title>تفاصيل التسجيلات الجامعية 2026/2025</title>
      <link>https://example.com/university-feed/2026</link>
      <description>
        <![CDATA[
        تفاصيل حول التسجيلات الجامعية للسنة الجديدة 2026/2025:<br/>
        - حقوق التسجيل: 330.00 دج<br/>
        - حقوق النقل: 280.00 دج<br/>
        - حقوق الإيواء: 5300.00 دج<br/>
        - جامعة التكوين المتواصل: 5200.00 دج
        ]]>
      </description>
      <pubDate>Fri, 19 Jul 2025 12:00:00 +0000</pubDate>
      <guid>https://example.com/university-feed/2026</guid>
    </item>
  </channel>
</rss>
'''

# حفظ الملف
file_path = Path("/mnt/data/university-feed.xml")
file_path.write_text(rss_content, encoding="utf-8")

file_path.name
