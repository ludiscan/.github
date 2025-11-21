# Ludiscan

**Game Analysis Tool Project** - ゲーム解析ツールプロジェクト

## Overview

Ludiscanは、ゲームプレイデータを収集・分析するためのツールセットです。

## Repositories

| Repository | Description |
|------------|-------------|
| [ludiscan-api-v0](https://github.com/ludiscan/ludiscan-api-v0) | Backend API server |
| [ludiscan-webapp](https://github.com/ludiscan/ludiscan-webapp) | Web application frontend |
| [ludiscan-unity-api-client](https://github.com/ludiscan/ludiscan-unity-api-client) | Unity SDK for game integration |

## Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Unity Game    │────▶│   Backend API   │◀────│    Web App      │
│   (SDK Client)  │     │   (ludiscan-api)│     │   (Dashboard)   │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

## Author

yuhi yamane
