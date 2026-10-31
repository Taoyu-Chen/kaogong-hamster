# kaogong-hamster

考公陪跑 · 仓鼠打卡：上传学习截图，识别结果确认后，仓鼠按当日状态变化并说话。

## 运行

```bash
npm install
npm run dev      # http://127.0.0.1:5173
npm run build    # 产物在 dist/
```

## 结构

- `src/api.js`：全项目唯一碰网络的地方。`USE_MOCK = true` 走本地假数据，`false` 走真识别链路
- `public/recognize.js`：截图识别 SDK，挂 `window.recognizeScreenshot`
- `src/components/`：上传卡、确认卡、兜底手填、今日屏
- `src/bridge.js`：识别结果到仓鼠参数的映射
