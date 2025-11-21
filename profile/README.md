# Ludiscan

**Game Analytics Platform** - ゲームプレイデータの収集・分析プラットフォーム

## Overview

Ludiscanは、ゲーム内のプレイヤー行動データを収集・可視化・分析するためのツールセットです。
プレイヤーの位置情報、イベント、スクリーンショットなどを記録し、ゲーム開発の改善に活用できます。

## Repositories

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| [ludiscan-webapp](https://github.com/ludiscan/ludiscan-webapp) | Analytics dashboard & management UI | Next.js, TypeScript, Three.js |
| [ludiscan-unity-api-client](https://github.com/ludiscan/ludiscan-unity-api-client) | Unity SDK for game integration | C#, Unity 2022.2+ |
| [ludiscan-api-v0](https://github.com/ludiscan/ludiscan-api-v0) | Backend API server | - |

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
            │
            ▼
┌─────────────────────────┐
│     Backend API         │
│   (ludiscan-api-v0)     │
│                         │
│  - Session Management   │
│  - Data Storage         │
│  - Analytics Processing │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│      Web Dashboard      │
│   (ludiscan-webapp)     │
│                         │
│  - 3D Visualization     │
│  - Analytics Reports    │
│  - Server Management    │
└─────────────────────────┘
```

## Features

- **Position Tracking** - プレイヤーの移動経路をリアルタイムで記録
- **Event Logging** - 死亡、勝利などのカスタムイベントを記録
- **Screenshot Capture** - 重要な瞬間のスクリーンショットを自動保存
- **3D Visualization** - Three.jsによるプレイデータの3D可視化

## Author

yuhi yamane
