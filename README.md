# Subscription Analyzer Skill

An AI-powered skill for Claude that analyzes Gmail to detect trial subscriptions and recurring charges, helping you prevent unwanted billing.

## Overview

This skill enables Claude to:
- Search your Gmail for subscription-related emails
- Identify active trial periods and expiration dates
- Track recurring subscriptions and billing cycles
- Provide actionable recommendations to cancel before charges
- Maintain an inventory of all your subscriptions

## Use Cases

- **Trial Management**: Find all active free trials before they convert to paid
- **Billing Prevention**: Get alerts for trials ending soon
- **Subscription Audit**: Comprehensive view of all recurring charges
- **Cost Optimization**: Identify unused subscriptions to cancel
- **Reminder System**: Track when trials expire and subscriptions renew

## How to Use

### Installation

1. Go to Claude.ai settings
2. Navigate to "Skills" or "Capabilities"
3. Click "Upload Custom Skill"
4. Upload the `SKILL.md` file

### Basic Commands

Ask Claude things like:
- "What subscriptions do I have?"
- "Show me trials ending this week"
- "Which services will bill me soon?"
- "Help me find subscriptions to cancel"
- "What's my total monthly subscription cost?"

### Example Interaction

**You**: "What trials are ending soon?"

**Claude**: 
```
I'll search your Gmail for active trials...

⚠️ Action Required This Week:

1. Streaming Service X - Ends Feb 14 (4 days)
   Cost: $19.99/month after trial
   Cancel: [link]

2. Fitness App Y - Ends Feb 16 (6 days)  
   Cost: $9.99/month after trial
   Cancel: Settings → Subscriptions

Total potential savings: $29.98/month
```

## Features

### Smart Detection
- Identifies subscription emails using multiple signals
- Recognizes trial period language patterns
- Extracts cancellation instructions automatically
- Tracks billing dates and renewal cycles

### Priority-Based Recommendations
- **Urgent** (< 3 days): Immediate action required
- **Action Needed** (3-7 days): Review and decide
- **Monitor** (> 7 days): Set reminder for later

### Comprehensive Analysis
- Service categorization (streaming, software, fitness, etc.)
- Cost breakdown and projection
- Cancellation difficulty rating
- Direct action links when available

## Requirements

- Gmail account with subscription-related emails
- Claude Pro or Team account (for Gmail integration)
- Permission to access Gmail via Claude

## Privacy & Security

- No subscription data is stored permanently
- Analysis happens in real-time during conversation
- Only accesses emails you have permission to view
- No data shared with third parties

## Configuration

The skill works out of the box, but you can customize:

### Search Parameters
- Date range for analysis (default: 90 days for trials)
- Subscription categories to include/exclude
- Minimum cost threshold for alerts

### Notification Preferences
- Lead time for trial ending alerts (default: 7 days)
- Frequency of subscription reviews
- Cost threshold for urgent alerts

## Troubleshooting

### "No subscriptions found"
- Extend the search date range
- Check if subscription emails are in spam/promotions
- Verify Gmail access permissions

### "Can't access Gmail"
- Re-authenticate Claude's Gmail connection
- Check account permissions
- Ensure Gmail integration is enabled

### "Missing cancellation links"
- Skill will provide manual cancellation steps
- Search service name + "cancel subscription" for help
- Check service's account settings page

## Best Practices

1. **Weekly Reviews**: Check trials ending in the next 7 days
2. **Monthly Audits**: Review all active subscriptions monthly
3. **Immediate Action**: Cancel trials you won't use right away
4. **Set Reminders**: Use calendar alerts for important dates
5. **Track Decisions**: Note which services you actively use

## Limitations

- Requires Gmail access (other email providers not supported yet)
- Some services may not send clear trial notification emails
- Cancellation complexity varies by service
- Historical data limited to email retention period

## Roadmap

Future enhancements planned:
- Support for Outlook and other email providers
- Integration with calendar for automatic reminders
- Spending analytics and trends
- One-click cancellation for supported services
- Subscription sharing detection (family plans)
- Price change alerts

## Support

For issues or questions:
- Review the SKILL.md file for detailed implementation guide
- Check Claude's documentation on custom skills
- Provide feedback via Claude's thumbs up/down buttons

## Version History

### v1.0.0 (Current)
- Initial release
- Gmail subscription detection
- Trial expiration tracking
- Basic recommendations engine
- Cost analysis

## Contributing

To improve this skill:
1. Test with various subscription services
2. Note any missed subscriptions or false positives
3. Share feedback on recommendation accuracy
4. Suggest additional features or improvements

## License

This skill is provided as-is for personal use with Claude.

---

**Built for preventing unwanted subscription charges and maintaining control over your recurring expenses.**
