# 📌 Redpanda - Topic `user-activity`

This document describes the **`user-activity`** topic, which tracks user activities within an application.  

---

## 📖 Topic Description

The `user-activity` topic collects events related to user interactions, such as logins, logouts, clicks, page views, and other actions.

### 🔹 Primary Use Cases:
- Analyzing user behavior
- Real-time activity monitoring
- Generating analytical reports
- Personalizing the user experience

---

## 📑 Message Schema

Messages in the `user-activity` topic are in **JSON format** and contain the following fields:

| Field       | Type      | Description                        |
|------------|----------|------------------------------------|
| `event_id` | `string`  | Unique event ID                   |
| `user_id`  | `string`  | User ID                            |
| `timestamp`| `string`  | Event timestamp (ISO 8601)        |
| `event_type` | `string` | Type of event (`login`, `click`, etc.) |
| `metadata` | `object`  | Additional event-related data     |

### 📌 Example Message

```json
{
  "event_id": "evt_12345",
  "user_id": "user_987",
  "timestamp": "2025-03-06T12:34:56Z",
  "event_type": "click",
  "metadata": {
    "page": "/home",
    "button_id": "signup"
  }
}
