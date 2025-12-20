# Financial Analysis Toolkit Knowledge Base

**For use with:** Financial Analyst GPT
**Created by:** Latentti.fi / Ari Hietamäki
**Version:** 1.0

---

## Financial Metrics Reference

### Profitability Metrics

| Metric | Formula | Interpretation | Healthy Range |
|--------|---------|----------------|---------------|
| **Gross Profit Margin** | (Revenue - COGS) / Revenue × 100% | Direct cost efficiency | Industry dependent |
| **Operating Profit Margin** | Operating Income / Revenue × 100% | Operational efficiency | 10-25% |
| **Net Profit Margin** | Net Income / Revenue × 100% | Bottom-line profitability | 5-20% |
| **EBITDA Margin** | EBITDA / Revenue × 100% | Cash profitability | 15-30% |
| **Contribution Margin** | (Revenue - Variable Costs) / Revenue × 100% | Per-unit profitability | 40-70% |
| **Return on Sales (ROS)** | Net Income / Revenue × 100% | Sales efficiency | 5-15% |

### Liquidity Metrics

| Metric | Formula | Interpretation | Healthy Range |
|--------|---------|----------------|---------------|
| **Current Ratio** | Current Assets / Current Liabilities | Short-term solvency | 1.5-3.0 |
| **Quick Ratio** | (Current Assets - Inventory) / Current Liabilities | Immediate liquidity | 1.0-2.0 |
| **Cash Ratio** | Cash / Current Liabilities | Cash coverage | 0.5-1.0 |
| **Operating Cash Flow Ratio** | Operating Cash Flow / Current Liabilities | Cash-based liquidity | > 1.0 |

### Efficiency Metrics

| Metric | Formula | Interpretation | Target |
|--------|---------|----------------|--------|
| **Days Sales Outstanding (DSO)** | (Accounts Receivable / Revenue) × 365 | Collection speed | 30-45 days |
| **Days Inventory Outstanding (DIO)** | (Inventory / COGS) × 365 | Inventory turnover | 30-60 days |
| **Days Payables Outstanding (DPO)** | (Accounts Payable / COGS) × 365 | Payment timing | 30-60 days |
| **Cash Conversion Cycle (CCC)** | DSO + DIO - DPO | Working capital efficiency | Lower is better |
| **Asset Turnover** | Revenue / Average Total Assets | Asset utilization | 0.5-2.0× |
| **Inventory Turnover** | COGS / Average Inventory | Inventory efficiency | 4-12× |
| **Receivables Turnover** | Revenue / Average Receivables | Collection efficiency | 8-15× |

### Return Metrics

| Metric | Formula | Interpretation | Healthy Range |
|--------|---------|----------------|---------------|
| **Return on Assets (ROA)** | Net Income / Average Total Assets × 100% | Asset returns | 5-15% |
| **Return on Equity (ROE)** | Net Income / Average Shareholders' Equity × 100% | Shareholder returns | 15-25% |
| **Return on Invested Capital (ROIC)** | NOPAT / Invested Capital × 100% | Capital efficiency | > WACC |
| **Return on Capital Employed (ROCE)** | EBIT / Capital Employed × 100% | Capital utilization | 15-25% |

### Leverage Metrics

| Metric | Formula | Interpretation | Healthy Range |
|--------|---------|----------------|---------------|
| **Debt-to-Equity** | Total Debt / Total Equity | Financial leverage | 0.5-1.5 |
| **Debt-to-Assets** | Total Debt / Total Assets | Asset financing | 30-50% |
| **Interest Coverage** | EBIT / Interest Expense | Debt service ability | > 3× |
| **Debt Service Coverage (DSCR)** | Operating Cash Flow / Total Debt Service | Loan repayment ability | > 1.25× |
| **Equity Multiplier** | Total Assets / Shareholders' Equity | Leverage factor | 1.5-3.0× |

---

## Unit Economics & SaaS Metrics

### Customer Acquisition

| Metric | Formula | Interpretation | Target |
|--------|---------|----------------|--------|
| **Customer Acquisition Cost (CAC)** | (Sales + Marketing Spend) / New Customers | Cost to acquire customer | Varies by industry |
| **CAC Payback Period** | CAC / (Monthly Revenue × Gross Margin) | Months to recover CAC | < 12 months |
| **Blended CAC** | Total S&M / Total New Customers | Average across channels | Track trends |
| **CAC by Channel** | Channel S&M / Channel New Customers | Channel efficiency | Compare channels |

### Customer Value

| Metric | Formula | Interpretation | Target |
|--------|---------|----------------|--------|
| **Customer Lifetime Value (CLV/LTV)** | (ARPU × Gross Margin) / Churn Rate | Total customer value | ≥ 3× CAC |
| **Average Revenue Per User (ARPU)** | Total Revenue / Total Customers | Revenue per customer | Track growth |
| **Monthly Recurring Revenue (MRR)** | Sum of monthly subscription revenue | Predictable revenue | Track growth |
| **Annual Recurring Revenue (ARR)** | MRR × 12 | Annual subscription base | Track growth |
| **Average Contract Value (ACV)** | Total Contract Value / Number of Contracts | Deal size | Track trends |

### Retention & Churn

| Metric | Formula | Interpretation | Target |
|--------|---------|----------------|--------|
| **Customer Churn Rate** | Lost Customers / Starting Customers × 100% | Customer loss rate | < 5% monthly |
| **Revenue Churn Rate** | Lost MRR / Starting MRR × 100% | Revenue loss rate | < 3% monthly |
| **Net Revenue Retention (NRR)** | (Starting MRR - Churn + Expansion) / Starting MRR × 100% | Revenue growth from existing | > 100% |
| **Gross Revenue Retention (GRR)** | (Starting MRR - Churn) / Starting MRR × 100% | Revenue retention | > 90% |
| **Logo Retention Rate** | (Starting Customers - Lost) / Starting Customers × 100% | Customer retention | > 90% |

### Growth Metrics

| Metric | Formula | Interpretation | Target |
|--------|---------|----------------|--------|
| **MRR Growth Rate** | (Current MRR - Previous MRR) / Previous MRR × 100% | Revenue growth | 10-20% MoM |
| **Net New MRR** | New MRR + Expansion MRR - Churned MRR | Net revenue change | Positive |
| **Quick Ratio (SaaS)** | (New MRR + Expansion MRR) / Churned MRR | Growth efficiency | > 4× |
| **Magic Number** | Net New ARR / Previous Quarter S&M Spend | Sales efficiency | > 0.75 |
| **LTV:CAC Ratio** | LTV / CAC | Unit economics health | ≥ 3:1 |

---

## Valuation Methodologies

### Discounted Cash Flow (DCF)

**Step-by-Step Process:**

1. **Project Free Cash Flow (5-10 years)**
   ```
   Free Cash Flow (FCF) = EBIT × (1 - Tax Rate) + D&A - CapEx - ΔWorking Capital
   ```

2. **Calculate Weighted Average Cost of Capital (WACC)**
   ```
   WACC = (E/V × Re) + (D/V × Rd × (1 - T))

   Where:
   E = Market value of equity
   D = Market value of debt
   V = E + D
   Re = Cost of equity (CAPM: Rf + β × (Rm - Rf))
   Rd = Cost of debt
   T = Tax rate
   ```

3. **Calculate Terminal Value**
   ```
   Gordon Growth: TV = FCF(n+1) / (WACC - g)
   Exit Multiple: TV = EBITDA(n) × Exit Multiple
   ```

4. **Discount to Present Value**
   ```
   Enterprise Value = Σ (FCF(t) / (1+WACC)^t) + TV / (1+WACC)^n
   ```

5. **Calculate Equity Value**
   ```
   Equity Value = Enterprise Value - Net Debt + Non-Operating Assets
   ```

### Comparable Company Analysis

| Multiple | Formula | Best For |
|----------|---------|----------|
| **EV/Revenue** | Enterprise Value / Revenue | High-growth, pre-profit |
| **EV/EBITDA** | Enterprise Value / EBITDA | Mature, profitable |
| **EV/EBIT** | Enterprise Value / EBIT | Capital-intensive |
| **P/E** | Share Price / EPS | Profitable, stable |
| **P/B** | Share Price / Book Value | Asset-heavy |
| **EV/FCF** | Enterprise Value / Free Cash Flow | Cash generative |

**Steps:**
1. Identify 5-10 comparable companies
2. Calculate relevant multiples
3. Determine median/mean multiples
4. Apply to target company metrics
5. Triangulate valuation range

### Precedent Transactions

**Steps:**
1. Research comparable M&A transactions (last 3-5 years)
2. Calculate transaction multiples (EV/Revenue, EV/EBITDA)
3. Adjust for:
   - Market conditions (bull/bear)
   - Control premium (typically 20-40%)
   - Synergies
4. Apply adjusted multiples to target

---

## Industry Benchmarks

### SaaS / Software

| Metric | Seed | Series A | Series B+ | Public |
|--------|------|----------|-----------|--------|
| ARR | < €1M | €1-5M | €5-20M | > €50M |
| ARR Growth | > 100% | 80-100% | 50-80% | 20-40% |
| Gross Margin | 60-70% | 70-80% | 75-85% | 80-90% |
| Net Retention | 90-100% | 100-110% | 110-130% | 110-140% |
| CAC Payback | 18-24 mo | 12-18 mo | 12-15 mo | < 12 mo |
| LTV:CAC | 2:1 | 3:1 | 4:1+ | 5:1+ |
| Rule of 40 | N/A | > 40% | > 40% | > 40% |

**Rule of 40:** Revenue Growth Rate + Profit Margin ≥ 40%

### E-commerce

| Metric | Small | Medium | Large |
|--------|-------|--------|-------|
| Revenue | < €5M | €5-50M | > €50M |
| Gross Margin | 25-35% | 30-45% | 35-50% |
| Operating Margin | -5-5% | 5-10% | 10-15% |
| CAC | €20-50 | €30-80 | €50-150 |
| LTV:CAC | 1.5:1 | 2:1 | 2.5:1+ |
| AOV | €50-100 | €80-200 | €100-500 |
| Repeat Rate | 20-30% | 30-40% | 40-60% |

### B2B Services

| Metric | Small | Medium | Large |
|--------|-------|--------|-------|
| Revenue | < €5M | €5-50M | > €50M |
| Gross Margin | 40-50% | 50-60% | 55-70% |
| Operating Margin | 10-15% | 15-20% | 20-30% |
| Revenue/Employee | €80-120K | €100-150K | €150-250K |
| Utilization Rate | 60-70% | 70-80% | 75-85% |

### Manufacturing

| Metric | Low | Average | High |
|--------|-----|---------|------|
| Gross Margin | 20-25% | 25-35% | 35-45% |
| Operating Margin | 5-8% | 8-12% | 12-18% |
| Asset Turnover | 0.5-1.0× | 1.0-1.5× | 1.5-2.5× |
| Inventory Turnover | 4-6× | 6-10× | 10-15× |
| ROIC | 8-12% | 12-18% | 18-25% |

---

## Financial Modeling Templates

### 3-Statement Model Structure

**Income Statement:**
- Revenue (by segment/product)
- Cost of Goods Sold
- Gross Profit
- Operating Expenses (S&M, R&D, G&A)
- Operating Income (EBIT)
- Interest Expense
- Pre-Tax Income
- Taxes
- Net Income

**Balance Sheet:**
- Assets: Cash, Receivables, Inventory, PP&E, Intangibles
- Liabilities: Payables, Accrued Expenses, Debt
- Equity: Share Capital, Retained Earnings

**Cash Flow Statement:**
- Operating: Net Income + Non-cash + Working Capital Changes
- Investing: CapEx, Acquisitions
- Financing: Debt, Equity, Dividends

### Key Assumptions to Document

| Category | Assumptions |
|----------|-------------|
| Revenue | Growth rate, pricing, volume, mix |
| COGS | Unit costs, labor, materials |
| OpEx | Headcount, salaries, marketing spend |
| Working Capital | DSO, DIO, DPO |
| CapEx | Maintenance, growth investments |
| Financing | Interest rates, debt schedule |
| Tax | Effective rate, NOLs |

---

## Scenario Analysis Framework

| Scenario | Revenue Growth | Margin | Key Assumptions |
|----------|---------------|--------|-----------------|
| **Base Case** | Expected | Current | Management guidance, historical trends |
| **Upside Case** | Base + 20-30% | Improved | Optimistic market, successful initiatives |
| **Downside Case** | Base - 20-30% | Compressed | Market challenges, execution issues |

**Sensitivity Analysis:**
- Identify 3-5 key drivers
- Test ±10%, ±20%, ±30% changes
- Document impact on valuation/returns

---

*Source: BMad-METHOD by Latentti.fi*
