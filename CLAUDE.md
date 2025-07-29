# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 專案概述 | Project Overview

這是一個 Contains Studio AI Agents 儲存庫，包含了專為快速開發設計的專業 AI agents 集合。這些 agents 都是各自領域的專家，可在需要時呼叫使用。

This is a Contains Studio AI Agents repository, containing a comprehensive collection of professional AI agents designed for rapid development. These agents are experts in their respective domains, ready to be invoked when their expertise is needed.

## 目錄結構 | Directory Structure

agents 按部門組織以便於發現：

Agents are organized by department for easy discovery:

```
contains-studio-agents/
├── design/           # 設計部門 agents
├── engineering/      # 工程部門 agents  
├── marketing/        # 行銷部門 agents
├── product/          # 產品部門 agents
├── project-management/  # 專案管理 agents
├── studio-operations/   # 工作室營運 agents
├── testing/          # 測試與基準測試 agents
└── bonus/            # 獎勵 agents
```

## Agent 檔案結構 | Agent File Structure

每個 agent 檔案都遵循標準格式：

Each agent file follows a standard format:

1. **YAML frontmatter** 包含：
   - `name`: 唯一識別符（kebab-case）
   - `description`: 使用時機與詳細範例
   - `color`: 視覺識別（如 blue, green, purple）
   - `tools`: agent 可使用的具體工具

   **YAML frontmatter** contains:
   - `name`: Unique identifier (kebab-case)
   - `description`: When to use with detailed examples
   - `color`: Visual identification (like blue, green, purple)
   - `tools`: Specific tools the agent can use

2. **System prompt**（500+ 字）包含：
   - Agent 身份與專業領域
   - 核心職責（5-8項）
   - 領域專業知識
   - 與 6 天衝刺工作流程的整合
   - 最佳實務方法
   - 約束條件
   - 成功指標

   **System prompt** (500+ words) contains:
   - Agent identity and expertise domain
   - Core responsibilities (5-8 items)
   - Domain expertise
   - Integration with 6-day sprint workflow
   - Best practices
   - Constraints
   - Success metrics

## 核心理念：6天衝刺 | Core Philosophy: 6-Day Sprint

所有 agents 都針對 6 天開發週期進行優化：
- **第1-2天**: 專案設置，實作核心功能
- **第3-4天**: 添加次要功能，優化用戶體驗
- **第5天**: 用戶測試與迭代
- **第6天**: 發布準備與部署

All agents are optimized for a 6-day development cycle:
- **Day 1-2**: Project setup, core feature implementation
- **Day 3-4**: Add secondary features, optimize user experience
- **Day 5**: User testing and iteration
- **Day 6**: Launch preparation and deployment

## Agent 分類 | Agent Categories

### 工程部門 (engineering/) | Engineering Department
- 專注於實作速度、程式碼品質、測試
- 偏好技術棧：React/Next.js、Supabase、Tailwind CSS

Focus on implementation speed, code quality, testing
Preferred tech stack: React/Next.js, Supabase, Tailwind CSS

### 設計部門 (design/) | Design Department
- 強調用戶體驗、視覺一致性、快速迭代
- 遵循行動優先、響應式設計原則

Emphasize user experience, visual consistency, rapid iteration
Follow mobile-first, responsive design principles

### 行銷部門 (marketing/) | Marketing Department
- 目標病毒傳播潛力、平台專業知識、成長指標
- 為 TikTok/Instagram 分享優化設計

Target viral potential, platform expertise, growth metrics
Optimize designs for TikTok/Instagram sharing

### 產品部門 (product/) | Product Department
- 優先考慮用戶價值、數據驅動決策、市場適配

Prioritize user value, data-driven decisions, market fit

### 營運部門 (studio-operations/) | Operations Department
- 優化流程、減少摩擦、擴展系統

Optimize processes, reduce friction, scale systems

## 最佳實務 | Best Practices

1. **讓 agents 協同工作** - 許多任務受益於多個 agents
   **Let agents work together** - Many tasks benefit from multiple agents
2. **明確描述任務** - 清晰的任務描述幫助 agents 表現更佳
   **Be specific about tasks** - Clear task descriptions help agents perform better
3. **信任專業知識** - agents 專為其特定領域設計
   **Trust the expertise** - Agents are designed for their specific domains
4. **快速迭代** - agents 支持 6 天衝刺哲學
   **Iterate quickly** - Agents support the 6-day sprint philosophy

## 主動觸發的 Agents | Proactive Agents

某些 agents 會在特定情境下自動觸發：

Some agents trigger automatically in specific contexts:

- **studio-coach**: 複雜多 agent 任務開始時或 agents 需要指導時
  **studio-coach**: When complex multi-agent tasks begin or agents need guidance
- **test-writer-fixer**: 實作功能、修復錯誤或修改程式碼後
  **test-writer-fixer**: After implementing features, fixing bugs, or modifying code
- **whimsy-injector**: UI/UX 變更後
  **whimsy-injector**: After UI/UX changes
- **experiment-tracker**: 添加功能標誌時
  **experiment-tracker**: When feature flags are added

## Agent 效能追蹤 | Agent Performance Tracking

透過以下指標追蹤 agent 效果：

Track agent effectiveness through these metrics:

- 任務完成時間 | Task completion time
- 用戶滿意度 | User satisfaction
- 錯誤率 | Error rates
- 功能採用率 | Feature adoption
- 開發速度 | Development velocity

## 客製化指南 | Customization Guide

修改 agents 以符合特定需求時：

When modifying agents to fit specific needs:

- 調整範例以反映您的產品類型
  Adjust examples to reflect your product types
- 添加 agents 可使用的特定工具
  Add specific tools agents can use
- 修改成功指標以符合您的 KPI
  Modify success metrics to match your KPIs
- 如需要可更新部門結構
  Update department structure if needed
- 客製化 agent 顏色以符合品牌
  Customize agent colors to match your brand

## 安裝與使用 | Installation and Usage

1. 複製此儲存庫到 `~/.claude/agents/` 目錄
   Copy this repository to `~/.claude/agents/` directory
2. 重啟 Claude Code 以載入新的 agents
   Restart Claude Code to load new agents
3. 描述任務，適當的 agent 將被觸發
   Describe tasks, appropriate agents will be triggered
4. 或明確提及 agent 名稱來直接呼叫
   Or explicitly mention agent names for direct invocation

每個 agent 都經過精心設計，以在快速開發環境中提供專業協助，確保在緊迫的時程中仍能維持高品質的輸出。

Each agent is carefully designed to provide professional assistance in rapid development environments, ensuring high-quality output even under tight timelines.