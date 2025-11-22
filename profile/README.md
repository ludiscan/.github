# Ludiscan

**Game Analytics Platform** - ゲームプレイデータの収集・分析プラットフォーム

## Overview

Ludiscanは、ゲーム内のプレイヤー行動データを収集・可視化・分析するためのツールセットです。
プレイヤーの位置情報、イベント、ヒートマップ生成、AIによるルートコーチングなどの機能を提供します。

## Repositories

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| [ludiscan-api-v0](https://github.com/ludiscan/ludiscan-api-v0) | Backend API server (Private) | NestJS, TypeScript, PostgreSQL, Redis |
| [ludiscan-webapp](https://github.com/ludiscan/ludiscan-webapp) | Analytics dashboard | Next.js, TypeScript, Three.js |
| [ludiscan-unity-api-client](https://github.com/ludiscan/ludiscan-unity-api-client) | Unity SDK | C#, Unity 2022.2+ |

## Architecture

```
┌─────────────────────────┐
│      Unity Game         │
│  (ludiscan-unity-api)   │
│                         │
│  - Position Tracking    │
│  - Event Logging        │
│  - Screenshot Capture   │
└───────────┬─────────────┘
            │ REST API
            ▼
┌─────────────────────────┐     ┌─────────────┐
│     Backend API         │────▶│ PostgreSQL  │
│   (ludiscan-api-v0)     │     │ + Redis     │
│                         │     └─────────────┘
│  - Session Management   │
│  - Heatmap Generation   │
│  - AI Route Coaching    │
│  - Google OAuth         │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│      Web Dashboard      │
│   (ludiscan-webapp)     │
│                         │
│  - 3D Visualization     │
│  - Heatmap Viewer       │
│  - Project Management   │
└─────────────────────────┘
```

## Features

- **Position Tracking** - 2D/3D対応のプレイヤー位置記録
- **Heatmap Generation** - 非同期ヒートマップ生成（Bull queue）
- **AI Route Coaching** - OpenAIによるルート最適化提案
- **Event Logging** - カスタムイベント・スクリーンショット記録
- **3D Visualization** - Three.jsによるデータ可視化
- **Multi-Auth** - JWT, Google OAuth, Game API Key対応

## Author

yuhi yamane
