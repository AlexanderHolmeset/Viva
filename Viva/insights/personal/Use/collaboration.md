---

title: Collaboration page for Viva Insights
description: Learn how to use Microsoft Viva Insights to improve your collaboration at work
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-personal 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: user

---

# Collaboration

The Collaboration page on your personal insights [Dashboard](dashboard-2.md) helps you reflect on how effectively you spend your time in meetings, email, chats, and calls.

  ![Collaboration page.](../../Images/mya/use/collaboration.png)

## Weekly average

The Weekly average section shows an estimate of how much time you spent in meetings, email, chats, and calls in the past four weeks. This estimate is measured as a percentage of your work week, which is based on activity within your set working hours as configured in [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance).

   ![Collaboration Weekly Average.](../../Images/mya/use/collab-weekly-average.png)

## Meeting habits

The **Meeting habits** section highlights what your habits or practices are in meetings you organized and accepted. You can switch between the Habits view and the **Meetings** view:

* The **Habits** view shows data about your meeting habits based on the meetings on your calendar over the past four weeks. It helps you understand the number of times each of these meeting types occur out of the total number of meetings you organized or accepted to attend.

    ![Collaboration Meeting Habits View.](../../Images/mya/use/collab-habits-2.png)

* The **Meetings view** shows details about all the meetings on your calendar over the past four weeks.

    ![Collaboration Meeting List View.](../../Images/mya/use/collab-meeting-list.png)

   |Icon |Description |
   |---|---|
   |![recur icon.](../../Images/mya/use/recur-icon.png) |Represents a recurring meeting on your calendar. |
   |![person meeting icon.](../../Images/mya/use/person-meeting-icon.png) | Represents a meeting organized by you. |
   |![recurring meeting by you icon.](../../Images/mya/use/recur-byu-icon.png) | Represents a recurring meeting organized by you. |
   |![check mark icon.](../../Images/mya/use/checkmark.png) | If a meeting has a check mark in a column, it met that specified meeting’s metric. For example, the meeting started on time. |
   |![X icon.](../../Images/mya/use/x-icon.png) | If a meeting has an X in a column, it did not meet that specified meeting’s metric. For example, the meeting did not start on time. |
   |![dash icon.](../../Images/mya/use/dash-icon.png) | If a meeting has a dash in a column, the specified meeting metric was not applicable for that meeting. For example, the meeting was canceled, so starting on time was not applicable. |
   |![sort up icon.](../../Images/mya/use/sort-up-icon.png)![sort down icon](../../Images/mya/use/sort-icon.png)  | Select a column name in the Meetings list to sort the list by that column in ascending or descending order. The sort icon will show up next to the column name that the list is sorted by. |

For a list of meetings that are excluded from the Meetings list and metrics, see [Meeting exclusions](#meeting-exclusions).

## Communication habits

The Communication habits section shows the total number of chats (instant messages) and emails sent and read during each hour of the day in the past four weeks.

   ![Communication habits.](../../Images/mya/use/collab-comm-habits.png)

## Productivity insights

The Collaboration page's productivity insights are based on your recent collaboration activity at work. Select **View suggestions** to get ideas about how you might change your current collaboration patterns.

## About the metrics

This section describes the metrics that the Collaboration page shows. It also describes how those metrics are calculated by Viva Insights.

### Meetings

Meeting metrics include any meetings that you organized or accepted to attend that have at least one other person attending. Meeting time includes meetings that take place during and outside of your set working hours. After-hours meeting time also affects your [Wellbeing metrics](../use/wellbeing.md#about-the-metrics).

#### Meeting habit metrics

The following meeting-habit metrics are included on the Collaboration page. You can select the question mark icon next to **Meeting habits** to see similar details about them.

* **High attendance** includes meetings you organized or accepted that had greater than a 50 percent response rate.
* **Invitations sent with a days' notice** includes meetings where you sent invitations with more than 24 hours notice before the meeting's scheduled start time.
* **Added Teams link** includes meetings you organized and included a Teams link for remote attendance.
* **No overlap with other meetings** includes meetings that you organized or accepted that did not overlap with other meetings.
* **No emails or chats during the meeting** includes meetings during which you did not send a significant number of emails or chats.
* **Online meetings joined on time** includes Teams meetings that you joined or started on time (or within five minutes of their schedule start time).
* **During working hours** includes meetings you organized or accepted to attend during your working hours.

#### Meeting exclusions

The following meeting types are excluded from meeting metrics:

* Meetings whose length is equal to or greater than 24 hours. Notably, this also excludes **All day** meetings:
![All-day meeting checkbox.](../../Images/mya/use/all-day-mtgs.png)

* Meetings that are marked as **Private**

* Meetings with no other participants than yourself, for example when you block focus time in your calendar or set reminders

* Meetings for which **Show As** is set to any of the following values:

  * Free
  * Working Elsewhere
  * Tentative
  * Out of Office

> [!Note]
> Viva Insights counts double-booked meetings only one time for metric calculations. For example, if you have two meetings scheduled for 10:00 AM to 11:00 AM on the same day, Viva Insights counts this as only one hour of meeting time.

### Email

Email metrics estimate how much time you spent sending and reading emails, across all devices, such as laptops and mobile phones. Only emails that have your name, or a group you’re a member of, on the **To** line or on the **Cc** line are included. Emails that you delete without opening are not included.

Each email you send is assigned 5 minutes. Each email you open is assigned 2.5 minutes. However, shorter times are assigned for the following scenarios:

* If you send one email and then open or send another one within 5 minutes, the time between the two actions gets assigned to the first email.
* If you open one email and then open or send another one within 2.5 minutes, the time between the two actions gets assigned to the first email.

Also, the time you spend sending or reading email outside your set work hours (as defined by your [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance)) will affect your [Wellbeing metrics](../use/wellbeing.md#about-the-metrics).

### Chats and calls

Viva Insights counts your audio calls, video calls, and chats (instant messages) that occur in Teams as collaboration activities, which are calculated as follows:

* Each chat or instant message that *you send* counts the time as 30 seconds.
* Each chat that *you receive* counts as zero seconds in time because empirically, time spent on sent messages is a good predictor of the total duration of Teams sessions.
* Each chat or instant message within a 15-minute window of time is counted as one chat.
* For each impromptu call, Viva Insights uses the actual duration of the call. An impromptu or ad hoc call is an unscheduled call that’s not included in your calendar.
* For calls that are scheduled as meetings in your calendar, the time counts as zero seconds because these calls are already being counted as meeting time.

  >[!Note]
  > Chats from Teams channels are excluded from the metrics. 

### Documents

Viva Insights also shows information for OneDrive and SharePoint documents that you have worked on. As a Viva Insights participant, you'll see the following insights:

* The number of cloud documents that you worked on (read, edited, or reviewed).
* The number of cloud documents that you worked on outside of working hours.

To see these insights, you must have worked on at least three OneDrive or SharePoint cloud documents during the past week.

## Collaboration tips

You might miss out on valuable collaboration time if you're spending too much time on email or impromptu calls or in meetings or chats. Research shows that typically doing just four to five things differently can enable you to increase your collaboration time by 18 to 24 percent.

* **Batch email time**: To reduce distraction, try checking your inbox once an hour. If that works well, try checking email every two hours and so on. Discover how much time you can get back.

* **Group your meetings together on your calendar**: If your calendar is fragmented with meetings, try grouping your meetings on your calendar, so you have longer free blocks available for team collaboration.

* **Reduce the meetings you attend and schedule**:

  * Fewer meetings enables more time for collaboration. Review your recurring meetings to make sure they're a good use of time each week.
  * Check the attendee lists for meetings you organize. Try condensing meetings with identical attendees.
  * In an office culture where meetings fill the day, make the most of yours. By setting expectations and making goals clear ahead of time, meetings can become more efficient, giving you and your colleagues some time back.

* **Keep meeting size under control**: Small and short meetings are more conducive to decision making, as it prompts attendees to communicate faster and focus on getting the work done. Research shows that every person added to the meeting group over seven reduces decision effectiveness by 10 percent. Consider making your meeting size small to avoid decision making overhead.

* **Respond to meetings on time**: Respond to meeting invites on time so your team knows what to expect. Coworkers can better prepare for meetings when they have a good sense of who plans to attend.

* **Give people time to prepare for meetings**: Last-minute invitations are sometimes necessary, but your meetings might be more effective if you give attendees some time to prepare.

* **Include Teams link for remote attendees**: Consider adding a Teams links to your meetings to accommodate remote attendees.

* **Include meeting agendas and action items in your invites**: Add agendas and action items to get the most out of your meetings. Consider adding clarity for what you’d like participants to do with attached files in your meeting invitations.

* **Start and end meetings on time**:

  * When meetings start on time, they are more likely to finish on time and meet the objectives of the meeting. Consider blocking time for preparation before the start of meetings to avoid late starts.
  * Better meeting practices can improve productivity, information sharing, innovation, decision making, and team collaboration.

* **Cancel meetings a day ahead**: If possible, send cancellations to attendees the day before. Do your best to plan ahead so that attendees can optimally re-purpose that time.

* **Take long email threads offline**: For long email threads that increase over the course of a few weeks, consider taking the email offline and scheduling a meeting to sync up.

* **Schedule meeting during work hours**: For non-urgent meetings, scheduling them during attendees' set working hours is a good practice that respects people’s wellbeing.

* **Avoid multitasking during meetings**: Research shows that merely having your smartphone nearby impairs cognitive capacity on par with the effects of lacking sleep. Consider putting away your phone while in meetings to dedicate full attention to them.
