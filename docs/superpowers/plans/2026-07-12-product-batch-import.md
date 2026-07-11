# Product Batch Import Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add the remaining Excel product image-and-text records after image 81 using the approved 2:1 image treatment.

**Architecture:** Keep the existing single-file static app. Preserve image-only records 1-81 and append product records 82+ with `note` fields so the existing product-mode CSS renders image plus text.

**Tech Stack:** Static HTML/CSS/JavaScript, embedded base64 data URLs, Python scripts for one-time Excel/image transformation, Playwright for verification.

## Global Constraints

- Do not change the legacy 1-81 single-image UI.
- Product images use 2:1 crop at 1800x900.
- Product text remains large, bold, and fully visible when possible.
- Keep output usable on iPad browsers through GitHub Pages or local HTTP.

---

## Tasks

- [x] Inspect Excel rows, image media files, and row-to-image mapping.
- [x] Generate normalized product records starting at 82.
- [x] Replace the existing sample product block in `index.html` with the full product list.
- [x] Verify in iPad viewport that legacy and product modes both work.
- [ ] Commit and push the finished update if the remote is available.
