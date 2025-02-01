---
layout: page
title: Sports Alert Engine
description: Real-Time Game Triggers with Natural Language Processing
img: assets/img/sports_alert_ui.png
importance: 1
category: fun
related_publications: false
---

A Flutter-powered sports notification system that transforms natural language rules into real-time game alerts. Below showcases its intelligent parsing engine and cross-platform capabilities.

<div class="row justify-content-sm-center" style="display: flex; align-items: flex-start;">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/alert_rule_creator.png" title="Rule Configuration" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/alert_types.png" title="Multi-Channel Delivery" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Natural language rule builder. Right: SMS/email alert configurations.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/live_scores.png" title="Live Game Monitoring" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real-time score tracking interface with active alert indicators.
</div>

The Sports Alert Engine revolutionizes fan engagement through its **natural language processing core** built with Python/Flask and Flutter. Key features include:

### Intelligent Rule Processing
- **Natural Language Interpreter**: Converts phrases like _"WHEN Lakers lead ≤3 in last 5 minutes"_ into game logic using regex patterns and safe `eval()` execution
- **Context-Aware Parsing**: Recognizes 50+ sports-specific terms (lead, OT, quarter) through custom tokenization
- **Dynamic Variables**: Supports team names, players, and game metrics from ESPN API's live data feed

### Multi-Platform Delivery
- **Flutter Frontend**: Cross-platform app (iOS/Android/Web) with team/player dropdowns and rule templates
- **Twilio Integration**: SMS/email alerts with configurable delivery channels and timing preferences
- **React Dashboard**: Web interface for non-technical users to manage subscriptions and alert history

<div class="row justify-content-sm-center" style="display: flex; align-items: flex-start;">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/api_diagram.png" title="System Architecture" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/alert_workflow.png" title="Event Processing" style="height: 300px; width: auto;" class="rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Architecture diagram showing ESPN API integration. Right: Alert triggering workflow.
</div>

### Technical Highlights
- **Real-Time Engine**: Processes 100+ concurrent games with <5s latency using WebSocket connections
- **State Management**: Bloc pattern in Flutter for efficient UI updates during live game changes
- **Security**: Rule sanitization layer prevents code injection in custom alert conditions
- **Analytics**: Tracks alert accuracy and user engagement through Firebase integration

### Performance Metrics
- Handled 50+ concurrent users during NBA playoffs with 99.8% uptime
- Reduced manual score checking time from 30min/game to instant notifications
- Supported 15+ sports types through modular league-specific parsers

The Sports Alert Engine combines fan intuition with technical precision, transforming casual viewers into engaged analysts through accessible real-time intelligence.