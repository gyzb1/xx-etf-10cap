# 512890 红利低波ETF回测系统

基于市值加权的ETF持仓回测系统，支持静态和动态两种回测模式。

## 快速开始

```bash
# 1. 安装依赖
npm install

# 2. 配置环境变量（创建 .env 文件）
TUSHARE_TOKEN=your_token_here

# 3. 启动服务
npm start

# 4. 访问系统
# 浏览器打开 http://localhost:3001
```

## 功能说明

### 静态回测
使用最新披露的持仓，回测历史表现。

### 动态回测
跟随ETF每次持仓披露，动态调整组合。

## 权重策略

**市值加权**：按股票市值比例分配权重

```
股票权重 = 该股票市值 / 所有股票市值之和
```

- 市值大的股票权重高
- 市值小的股票权重低
- 符合主流指数编制方法

## 数据来源

- **持仓数据**：Tushare `fund_portfolio` 接口
- **价格数据**：Tushare `daily` 接口
- **市值数据**：Tushare `daily_basic` 接口

## 技术栈

- **后端**：Node.js + Express
- **前端**：原生JavaScript + Chart.js
- **数据源**：Tushare Pro API

## 注意事项

1. 需要有效的Tushare Token
2. 建议积分≥2000以获取完整数据
3. 历史回测不代表未来收益
4. 仅供学习研究使用

## 许可证

MIT License
