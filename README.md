───────────────────────────────────────────────────────────────┐
│                       Jetpack Compose UI Layer                     │
│  MainMenuScreen (Solo / Wi-Fi LAN)  ──▶  GameScreen (HUD / Chat)   │
│         │                                       │                  │
│         └───────────────┬───────────────────────┘                  │
│                         ▼                                          │
│               VoxCraftViewModel (StateFlow)                        │
└────────────┬────────────────────────┬──────────────────┬───────────┘
             │                        │                  │
             ▼                        ▼                  ▼
┌─────────────────────┐  ┌──────────────────────┐  ┌─────────────────┐
│   World & Storage   │  │ OpenGL ES 3.0 Engine │  │  Wi-Fi LAN Net  │
│  - WorldEngine      │  │ - VoxelGLSurfaceView │  │ - UDP Discovery │
│  - Chunk & Noise    │  │ - VoxelRenderer      │  │ - TCP Host/Join │
│  - WorldStorage     │  │ - ChunkMesher & AO   │  │ - Chat & Sync   │
│  - PlayerController │  │ - TextureAtlas       │  │                 │
└──────────┬──────────┘  └──────────┬───────────┘  └─────────────────┘
           │                        │
           ▼                        ▼
