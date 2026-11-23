# antiburn-missing-kids · 公益找孩子数据

供 [antiburn 防烧屏模块](https://github.com/Xposed-Modules-Repo/io.github.wumisc.antiburn)「公益找孩子」板块读取的规范化 JSON。

- 数据源：宝贝回家寻子网 baobeihuijia.com「家寻宝贝」栏目（排除送养类）。
- 更新：每 2 天一次定时抓取，按注册日期倒序（最新发布优先）。
- 通道：`raw.githubusercontent.com/wumisc/antiburn-missing-kids/main/kids.json`，
  备用 `cdn.jsdelivr.net/gh/wumisc/antiburn-missing-kids@main/kids.json`；App 内另内置兜底快照。
- 抓取脚本：antiburn 工程 `tools/fetch_missing_kids.py`；合格条目不足 3 条时不覆盖旧数据。

## kids.json 结构

```json
{
  "schema": 1,
  "updated": "2026-11-23T12:00:00Z",
  "source": "宝贝回家寻子网 baobeihuijia.com · 家寻宝贝",
  "source_url": "https://baobeihuijia.com/bbhj/",
  "notice": "…仅供公益传播线索；发现线索请拨 110 或联系官方。",
  "contact": { "tel": "…", "mobile": "…", "email": "…", "qq_group": "…", "service_time": "…", "address": "…" },
  "items": [
    { "id": 748652, "name": "…", "gender": "男", "birth": "…", "height": "…",
      "type": "被拐", "lost_time": "…", "lost_place": "…", "feature": "…",
      "reg_date": "2026-08-09", "url": "https://baobeihuijia.com/bbhj/contents/3/….html",
      "photo": "https://baobeihuijia.com/bbhj/special/….jpg" }
  ]
}
```

信息版权归宝贝回家志愿者协会与登记人所有，此处仅作公益传播。发现线索请拨 110。
