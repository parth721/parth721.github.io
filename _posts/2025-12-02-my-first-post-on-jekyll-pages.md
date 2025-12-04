---
layout: post
title: My First Post on Jekyll/Minima
date: 2025-12-02 10:00:00 +0530
categories: experience
---

This is the content of my very first blog post!

I recently started experimenting with Jekyll, choosing the Minima theme because it looked simple. Instead, I spent several hours solving issues I didn’t expect. Here’s a concise record of what I learned.

### Dark Mode Setup

Enabling light/dark mode was harder than anticipated. LLM-generated instructions were inconsistent and often incorrect. The solution came only after carefully reading the official Minima README.

### File Structure Confusion

Understanding where files belong (_layouts, _includes, _sass, etc.) was initially confusing. Here, LLM tools helped clarify the structure, and the issue was resolved quickly.

### LaTeX Support

There was almost no reliable information on enabling LaTeX in Minima. I spent 2–3 hours trying different LLM suggestions and online posts, none successful. Switching tp alfolio theme felt costly after already investing effort.

Eventually, checking GitHub Issues in Minima repo helped. I found someone who solved the same problem, but their explanation wasn’t immediately clear due to my lack of experience. I asked an LLM to interpret the thread in simple terms, followed the steps, and finally got LaTeX working.

---

### Key Takeaways

- Real fixes usually come from official docs and GitHub Issues, not random search or LLM suggestions

- You don’t always need deep understanding of tools like Jekyll for occasional tasks.

- LLMs are useful for simplify concepts if you have the most of the context, but unreliable for exact implementation steps. because of these LLM I lost 2-3 hrs, it gives instructions like : Do step A then B then C then Rollback to A then do D 😵‍💫

---

## Links :

- [issue828](https://github.com/jekyll/minima/issues/828)
- [readme](https://github.com/jekyll/minima/blob/master/README.md)
- [add logos](https://lucaf.eu/2025/08/14/minima-custom-icons.html)