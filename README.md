# Claude Household Budget Management Workspace

[![Claude Code](https://img.shields.io/badge/Claude%20Code-Project-8A2BE2?logo=anthropic)](https://github.com/anthropics/claude-code)

A comprehensive workspace template for managing household budgets using Claude Code CLI with AI-assisted analysis, reporting, and financial planning.

## Overview

This template provides a complete system for household budget management including transaction processing, budget creation, expense analysis, financial goal tracking, and comprehensive reporting—all powered by Claude Code's AI agents and slash commands.

## Features

- **AI-Assisted Budget Creation**: Generate realistic monthly budgets based on income, historical spending, and financial goals
- **Automated Transaction Processing**: Import and categorize bank transactions with intelligent categorization
- **Comprehensive Financial Reports**: Monthly, quarterly, and annual reports with insights and trends
- **Goal Tracking**: Set and monitor progress toward savings goals, debt payoff, and major purchases
- **Spending Analysis**: Deep-dive analyses identifying patterns and optimization opportunities
- **Scenario Planning**: Model financial decisions and life events
- **Privacy-First**: All data stays local on your machine

## Quick Start

### 1. Clone or Fork This Repository

```bash
cd ~/repos/github
git clone [this-repo-url] my-household-budget
cd my-household-budget
```

### 2. Initial Setup

Open Claude Code in this directory and run the setup wizard:

```bash
/setup-workspace
```

This interactive setup will configure:
- Household profile and preferences
- Income sources and amounts
- Expense categories and budgets
- Financial goals and savings targets
- Bill due dates and payment schedules

### 3. Create Your First Budget

```bash
/create-monthly-budget
```

### 4. Import Transactions (Optional)

Place transaction exports from your bank/credit card in `transactions/import/`, then:

```bash
/process-transactions
```

### 5. Generate Monthly Report

```bash
/monthly-report
```

## Directory Structure

```
.
├── .claude/
│   ├── agents/              # Specialized AI agents for budget tasks
│   │   ├── budget-architect.md
│   │   ├── expense-analyst.md
│   │   ├── goal-tracker.md
│   │   ├── transaction-processor.md
│   │   ├── report-generator.md
│   │   └── financial-advisor.md
│   └── commands/            # Slash commands for common operations
│       ├── setup-workspace.md
│       ├── create-monthly-budget.md
│       ├── process-transactions.md
│       ├── monthly-report.md
│       ├── analyze-spending.md
│       ├── set-financial-goal.md
│       └── review-goals.md
├── context/
│   ├── household/          # Household-specific context
│   ├── financial/          # Financial account details
│   └── goals/              # Detailed goal documentation
├── prompts/                # Reusable prompts for budget tasks
├── outputs/
│   ├── budgets/           # Generated budget documents
│   ├── reports/           # Financial reports and analyses
│   ├── analyses/          # Deep-dive spending analyses
│   └── visualizations/    # Charts and graphs (if generated)
├── transactions/
│   ├── import/            # Place bank/CC exports here
│   └── processed/         # Categorized transaction data
├── budgets/
│   ├── templates/         # Budget templates
│   ├── monthly/           # Monthly budgets
│   └── annual/            # Annual budgets
├── reports/
│   ├── templates/         # Report templates
│   ├── monthly/           # Monthly financial reports
│   ├── quarterly/         # Quarterly reports
│   └── annual/            # Annual reports
├── financial-goals/
│   ├── templates/         # Goal tracking templates
│   ├── active/            # Active financial goals
│   └── archived/          # Completed goals
├── context.md             # Main household configuration
├── CLAUDE.md             # Workspace operation instructions
├── mcp.md                # MCP integration guidance
└── README.md             # This file
```

## Available Agents

### budget-architect
Creates comprehensive monthly and annual budgets based on income, spending history, and goals.

**Use when:** Creating or modifying budgets

**Example:** "I need to create my December budget"

### expense-analyst
Analyzes spending patterns, identifies trends, and finds savings opportunities.

**Use when:** Understanding where money goes or finding ways to save

**Example:** "I went over budget last month. What happened?"

### goal-tracker
Manages financial goals including savings targets and debt payoff plans.

**Use when:** Setting new goals or checking progress

**Example:** "How am I doing on my emergency fund goal?"

### transaction-processor
Imports and categorizes transaction data from banks and credit cards.

**Use when:** Processing downloaded transactions

**Example:** "I downloaded my bank transactions for November"

### report-generator
Creates comprehensive financial reports with insights and recommendations.

**Use when:** Need monthly summaries or annual reviews

**Example:** "Can you create my November financial report?"

### financial-advisor
Provides strategic financial guidance and scenario planning.

**Use when:** Making major financial decisions

**Example:** "Should I pay off student loans or invest?"

## Available Slash Commands

### Setup & Configuration
- `/setup-workspace` - Initial workspace configuration wizard
- `/update-context` - Update household information

### Budget Management
- `/create-monthly-budget` - Generate monthly budget
- `/create-annual-budget` - Generate annual budget
- `/adjust-budget` - Modify existing budget

### Transaction Processing
- `/process-transactions` - Import and categorize transactions
- `/reconcile-accounts` - Match transactions to statements

### Analysis & Reporting
- `/monthly-report` - Comprehensive monthly report
- `/analyze-spending` - Deep spending analysis
- `/budget-vs-actual` - Compare budget to actuals

### Goal Management
- `/set-financial-goal` - Define new financial goal
- `/review-goals` - Check progress on all goals
- `/update-goal` - Modify existing goal

### Financial Planning
- `/debt-payoff-plan` - Strategic debt reduction
- `/savings-plan` - Optimize savings allocation
- `/financial-scenario` - Model what-if scenarios

## Typical Workflows

### Monthly Budget Cycle

1. **Beginning of Month**: Create next month's budget
   ```bash
   /create-monthly-budget
   ```

2. **Throughout Month**: Import and process transactions weekly
   ```bash
   # Place transactions in transactions/import/
   /process-transactions
   ```

3. **End of Month**: Generate comprehensive report
   ```bash
   /monthly-report
   ```

4. **Review**: Analyze spending and adjust next budget
   ```bash
   /analyze-spending
   ```

### Setting Up a New Financial Goal

1. Define the goal
   ```bash
   /set-financial-goal
   ```

2. Ensure it's funded in your budget
   ```bash
   /create-monthly-budget
   ```

3. Track progress monthly
   ```bash
   /review-goals
   ```

### Major Financial Decision

1. Gather all context
   ```bash
   /monthly-report
   /review-goals
   ```

2. Model the scenario
   ```bash
   # Ask: "What if I...?" and use financial-advisor agent
   ```

3. Make informed decision with full financial picture

## Best Practices

### Regular Cadence

**Weekly**:
- Import transactions
- Check spending vs. budget
- Note any unusual expenses

**Monthly**:
- Generate comprehensive report
- Review goal progress
- Create next month's budget
- Analyze spending patterns

**Quarterly**:
- Deep-dive financial review
- Adjust goals if needed
- Optimize budget allocations

**Annually**:
- Year-end comprehensive review
- Tax preparation
- Set new year goals
- Annual budget planning

### Data Management

**Transaction Imports**:
- Import regularly (weekly minimum)
- Categorize promptly
- Review automated categorization for errors
- Keep raw files as backup

**Version Control**:
- Commit budgets when created
- Commit monthly reports
- Add transaction files to .gitignore
- Regular commits for audit trail

**Privacy**:
- Never commit files with full account numbers
- Use 1Password for credentials
- Review .gitignore before pushing
- Consider private repo for this workspace

### Financial Discipline

**Budget Realism**:
- Base on actual spending, not wishes
- Include 5-10% buffer for unexpected
- Adjust as you learn your patterns
- Don't be too restrictive

**Goal Setting**:
- Use SMART criteria
- Prioritize properly (emergency fund first)
- Track consistently
- Celebrate milestones

**Spending Awareness**:
- Review transactions regularly
- Understand your triggers
- Plan for irregular expenses
- Build sinking funds

## Customization

### Adding Custom Categories

1. Edit `context.md` to add category
2. Update budget templates if needed
3. Recategorize past transactions if desired

### Creating Custom Reports

1. Define report structure in `reports/templates/`
2. Create slash command in `.claude/commands/`
3. Document in this README

### Modifying Agents

Edit agent files in `.claude/agents/` to adjust:
- Analysis methodology
- Report formats
- Recommendation logic
- Processing rules

## MCP Integration

This workspace can be enhanced with MCP (Model Context Protocol) servers for:
- Direct bank/credit card data access
- Spreadsheet integration
- Calendar reminders
- Chart generation
- Tax preparation exports

See `mcp.md` for detailed integration guidance.

## Troubleshooting

### Categorization Issues
**Problem**: Transactions categorized incorrectly
**Solution**: Manually correct them - the system learns from your corrections

### Budget Too Tight
**Problem**: Consistently exceeding budget
**Solution**: Increase allocations based on actual spending patterns. Budget should be realistic, not aspirational.

### Goals Not Tracking
**Problem**: Goal progress not updating
**Solution**: Ensure goal account is linked properly in context.md

### Missing Transactions
**Problem**: Imported file incomplete
**Solution**: Check export settings from bank, ensure all accounts included

## Privacy & Security

**Local Data**:
- All financial data stays on your machine
- No cloud synchronization of sensitive data
- Complete control over your information

**Version Control**:
- Use private repository if pushing to remote
- Sensitive files listed in .gitignore
- Never commit full account numbers

**Credentials**:
- Store API keys in 1Password
- Use environment variables for sensitive data
- Review MCP configurations for security

## License

MIT License - Feel free to fork and customize for your needs

## Support & Contributing

- **Issues**: Report bugs or request features via GitHub issues
- **Documentation**: Claude Code docs at [docs.claude.com](https://docs.claude.com)
- **Community**: Share your customizations and improvements

## Acknowledgments

Built for Claude Code CLI by Anthropic. Inspired by household budget management best practices and structured workspace organization principles.

---

**Ready to take control of your household finances?**

Start with `/setup-workspace` and build your path to financial clarity!
