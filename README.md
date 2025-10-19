


<img width="1046" height="422" alt="image" src="https://github.com/user-attachments/assets/e3716ae2-614d-480b-ac66-2159c8a83b78" />




AI-Driven Multi-Platform Video Content Pipeline
Overview

An automated social media content creation and distribution system that generates, produces, and publishes diary-style short videos across multiple platforms.
It uses GPT-4 to write scripts, Pictory.ai to generate videos with AI voiceovers and background music, and automatically distributes the final videos to TikTok, Instagram Reels, YouTube Shorts, and Twitter/X — all managed via Telegram and Google Sheets.

Workflow Summary
1. Scheduled Execution

Runs automatically every day at predefined times using n8n’s Schedule Trigger.

Reads video topics and publishing status from a connected Google Sheet.

2. Script Generation

Uses GPT-4o-mini to write 80–120 word diary-style video scripts in the Quantum White tone — soft, reflective, and poetic.

Scripts focus on simple daily moments, nature metaphors, and emotional calm.

If rejected, an improved version is auto-regenerated with better emotional tone.

3. Telegram Approval Workflow

Draft scripts are sent to a Telegram bot for manual approval or rejection.

Approved scripts proceed to video production; rejected ones are rewritten automatically.

4. Video Generation (Pictory.ai)

Calls the Pictory.ai API to create videos with:

AI voiceovers

Auto background music

Dynamic text overlays

1080x1920 portrait format (ideal for Reels & Shorts)

Waits for job completion, retrieves the rendered video link, and stores it.

5. Metadata Creation

Generates:

Social media titles optimized for engagement

Video descriptions with 2–3 relevant hashtags

Both are created using GPT-4o-mini and stored in Google Sheets.

6. Multi-Platform Upload

Uploads completed videos automatically via Upload-Post API to:

TikTok

Instagram Reels

YouTube Shorts

Twitter/X

Marks each upload as done in the sheet.

7. Status Tracking & Automation

Tracks every video’s progress and upload status in Google Sheets.

Includes auto-updating workflows for daily content management.

Technology Stack

n8n – Workflow automation & orchestration

GPT-4o-mini (OpenAI) – Script, title, and description generation

Pictory.ai API – AI video generation with auto voice and music

Telegram Bot API – Human review and approval interface

Google Sheets – Input, tracking, and publishing log

Upload-Post API – Multi-platform publishing automation

Summary

This workflow fully automates the social media short-video lifecycle — from idea to published post.
It enables daily, human-reviewed, AI-generated video publishing at scale, combining creative writing, video production, and multi-platform distribution into a single intelligent pipeline.
