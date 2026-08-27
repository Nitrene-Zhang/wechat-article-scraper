# WeChat Article Scraper

[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md) | [日本語](README.ja.md) | [한국어](README.ko.md)

A Codex skill for extracting visible content from a WeChat Official Account article already open in the user's browser, when the user is authorized to access it. Results can be exported as editable text documents.

## Features

- Extracts the title, account name, author, publication time, and body
- Preserves headings, paragraphs, lists, tables, phonetic annotations, formulas, and examples
- Records image captions and visible attachment information
- Supports editable Markdown, DOCX, and TXT output
- Performs limited scrolling and expansion for lazy-loaded content
- Reports complete or partial extraction and the reason

## Usage

1. Open the target article in Chrome or another supported browser.
2. Confirm that the current account is authorized to access it and keep the page open.
3. Invoke in Codex:

~~~text
Use $wechat-article-scraper to extract the complete body of the currently open WeChat article and export it as an editable text document.
~~~

## Output formats

| Format | Best for | Notes |
| --- | --- | --- |
| Markdown | Editing, version control, and publishing | Preserves document structure |
| DOCX | Word editing, delivery, and printing | Suitable for comments and layout |
| TXT | Plain-text use | Does not preserve complex formatting |

## Workflow

1. Identify the open article page.  2. Confirm its metadata and body region.  3. Extract visible text while preserving structure.  4. Collect captions and visible attachments.  5. Generate the requested file and report scope.

## Limitations

- Only processes pages the user has opened and is authorized to access.
- Does not bypass login, CAPTCHA, paywalls, copyright restrictions, or access controls.
- Does not like, follow, comment, repost, or download paid attachments.
- Partial access is reported with missing content and its reason.
- Users are responsible for content rights and compliance with applicable laws.

## Repository structure

~~~text
wechat-article-scraper/
├── SKILL.md                 # Skill scope and workflow
├── agents/openai.yaml       # Codex skill metadata
├── README.md                # Simplified Chinese documentation
├── README.zh-TW.md          # Traditional Chinese documentation
├── README.en.md             # English documentation
├── README.ja.md             # Japanese documentation
└── README.ko.md             # Korean documentation
~~~

## Content responsibility

This project documents an extraction workflow. It does not change source copyright or grant permission to reproduce articles. Users must verify the source, access rights, and intended use.
