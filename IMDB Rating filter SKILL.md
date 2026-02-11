

## Implementation Approach

### Step 1: Gmail Search Strategy
Search for emails containing subscription indicators:
- Keywords: "trial", "subscription", "free trial", "cancel anytime", "billing", "recurring", "membership"
- Sender patterns: "noreply@", "billing@", "subscriptions@"
- Date range: Last 90 days for trials, last 12 months for active subscriptions

### Step 2: Email Parsing
Extract key information from each email:
- Service name
- Trial start date
- Trial end date / billing date
- Cancellation instructions
- Subscription cost (if mentioned)
- Account email used

### Step 3: Analysis & Categorization
Group subscriptions into:
1. **Active Trials** - Currently in trial period
2. **Ending Soon** - Trial ends within 7 days
3. **Recently Billed** - Converted from trial in last 30 days
4. **Active Subscriptions** - Ongoing paid subscriptions

### Step 4: Recommendations
For each subscription:
- **Urgent** (< 3 days): Cancel immediately if unused
- **Action Needed** (3-7 days): Review usage and decide
- **Monitor** (> 7 days): Set reminder to review later
- Provide direct cancellation links when available

## Output Format

### Summary View
Present findings in structured format:

**⚠️ Urgent Action Required**
- [Service Name] - Trial ends [Date] ([X days])
  - Cost after trial: $XX/month
  - Cancellation: [Link or instructions]

**📋 Active Trials**
- [Service Name] - [Days remaining]

**💳 Active Subscriptions**
- [Service Name] - $XX/month (billed [frequency])

### Detailed Analysis
For each subscription provide:
- Service name and category
- Current status (trial/active/ending)
- Key dates (start, end, next billing)
- Cost breakdown
- Usage recommendation
- Cancellation difficulty (easy/moderate/hard)
- Direct action links

## Best Practices

1. **Privacy First**: Only analyze emails user has access to, never store sensitive data
2. **Actionable Insights**: Focus on subscriptions requiring immediate action
3. **Clear Communication**: Use simple language and visual indicators (emoji, formatting)
4. **Time Sensitivity**: Prioritize by urgency (days until billing)
5. **Verification**: Encourage users to verify details before cancelling

## Error Handling

- If Gmail access fails: Guide user through authentication
- If no subscriptions found: Confirm search parameters and date range
- If parsing fails: Report which emails couldn't be analyzed
- If links unavailable: Provide manual cancellation steps

## Integration Points

This skill works best when integrated with:
- Gmail API for email analysis
- Calendar for billing reminders
- Task management for follow-up actions
- Budget tracking tools for cost analysis

## Example Usage

**User**: "What trials do I have that are ending soon?"

**Claude Response**:
```
I'll search your Gmail for active trials and expiration dates.

[After analysis]

⚠️ **Action Required This Week**

1. **Streaming Service X** - Trial ends Feb 14 (4 days)
   - Will charge $19.99/month
   - Cancel: [Direct link]
   
2. **Fitness App Y** - Trial ends Feb 16 (6 days)
   - Will charge $9.99/month  
   - Cancel: Settings → Subscriptions

📊 **Summary**: 2 trials ending soon, potential savings: $29.98/month

Would you like me to set reminders or help you cancel any of these?
```

## Continuous Improvement

Track common patterns:
- Which services most often convert to unwanted charges
- Typical trial lengths by category
- Cancellation difficulty by service
- User action rates on recommendations

Use insights to improve detection accuracy and recommendation quality over time.
