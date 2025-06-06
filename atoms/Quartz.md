The built-in explorer doesn't play well with my {上,中,下} way of ordering things, so I disabled it on the main page and replaced it with a "latest journal entries things" which I shamelessly copy-pasted from Jacky's blog.

```
Component.DesktopOnly(
Component.RecentNotes({
title: "最近の日記",
limit: 4,
filter: (f) =>
f.slug!.startsWith("journal/") && f.slug! !== "journal/index" && !f.frontmatter?.noindex,
linkToMore: "journal/" as SimpleSlug,
}),
),
```
