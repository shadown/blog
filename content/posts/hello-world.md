---
title: "Hello World"
date: 2026-05-31
description: "Welcome to the blog — a first post showing off text, images, and Mermaid diagrams."
tags: ["hello", "meta", "mermaid"]
ShowToc: true
---

Welcome to the blog! This is the first post, and it doubles as a demo of what Hugo + PaperMod can do.

## Text

Write your thoughts in clean Markdown. Everything you'd expect works: **bold**, *italic*, `inline code`, [links](https://gohugo.io), blockquotes, lists, and more.

> The best time to start a blog was 10 years ago. The second best time is today.

## Code Blocks

```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

print(list(fibonacci(10)))
# Output: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

## Images

Hugo handles images natively with image processing. Drop an image in the page bundle and reference it:

```markdown
![Alt text](image.png)
```

## Mermaid Diagrams

Mermaid diagrams are supported via a custom render hook. Write standard Mermaid syntax inside a fenced code block with the `mermaid` language:

### Flowchart

```mermaid
graph TD
    A[Write in Markdown] --> B[Hugo builds site]
    B --> C[GitHub Pages serves it]
    C --> D{Readers}
    D --> E[Enjoy content]
    D --> F[Share feedback]
    style A fill:#4a9eff,color:#fff
    style B fill:#4a9eff,color:#fff
    style C fill:#4a9eff,color:#fff
```

### Sequence Diagram

```mermaid
sequenceDiagram
    participant You
    participant Hugo
    participant GitHub
    You->>Hugo: hugo new post my-post.md
    You->>Hugo: Write content...
    You->>Hugo: hugo
    Hugo->>public/: Generate static files
    You->>GitHub: git push
    GitHub->>GitHub Pages: Deploy site
    Note right of GitHub: All automatic via Actions
```

### Gantt Chart

```mermaid
gantt
    title Blog Setup Timeline
    dateFormat  YYYY-MM-DD
    section Setup
    Install Hugo           :done, 2026-05-31, 1d
    Choose theme           :done, 2026-05-31, 1d
    Configure site         :done, 2026-05-31, 1d
    section Content
    Write first post       :active, 2026-05-31, 1d
    Write about page       :2026-06-01, 1d
    Regular posts          :2026-06-01, 30d
```

### Class Diagram

```mermaid
classDiagram
    class Blog {
        +String title
        +String author
        +publish()
        +share()
    }
    class Post {
        +String title
        +Date date
        +String[] tags
        +render()
    }
    class Tag {
        +String name
        +getPosts()
    }
    Blog "1" --> "*" Post
    Post "*" --> "*" Tag
```

---

That's it! More posts coming soon. 🚀
