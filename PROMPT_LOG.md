Prompt Log - BillKeeper

Date: November 25, 2026

Project
BillKeeper: A Household Bill Tracker

Purpose
This file records the prompts used with GitHub Copilot Agent Mode during the development of the project.

Prompt History

Prompt 1 – Initial BillKeeper Application

Date: November 25, 2026

Prompt:
[You are a helpful senior web developer. Build a complete, beginner-friendly, single-page household bill tracking web application called **BillKeeper: A Household Bill Tracker**.

**Tagline:** "Keep Bills in Line, Pay Right on Time."

Follow all the requirements below carefully. Do not skip any feature.

1. Project Purpose

BillKeeper is designed for our household/family. Its purpose is to help parents and the family member responsible for paying household bills remember due dates and monitor paid and unpaid bills.

The application should provide a centralized place to record household bills, monitor payment statuses, and display due date reminders.

2. Technology Requirements

- HTML for the application structure.
- CSS for styling and responsive layout.
- Vanilla JavaScript for functionality.
- localStorage for saving bill records.
- Use only one HTML file containing HTML, CSS, and JavaScript.
- Do not use external libraries, frameworks, databases, or backend services.

3. Bill Information and Categories

Each bill must contain:
- Bill Category
- Amount
- Due Date
- Payment Status (Paid or Unpaid)

Provide these predefined categories:
1. Electricity
2. Water
3. Internet
4. Phone
5. Rent
6. Other

When the user selects "Other", display an input field where they can enter a custom category.

All bill amounts must use Philippine Pesos (₱), not US Dollars ($). Display amounts using the format, such as ₱1,500.00.

4. Dashboard Features

Create an organized dashboard displaying:
- Total Bills
- Unpaid Bills
- Paid Bills
- Due Soon
- Total Unpaid Amount
- Upcoming Bills
- Overdue Bills
- Recent Bills
- Add New Bill button

Make the dashboard easy to understand and navigate.

5. Bill Management

Implement the following features:
- Add Bill
- View Bills
- Edit Bill
- Update Payment Status
- Archive Bill
- View Archived Bills

Do not include a permanent Delete feature. Archived bills must remain saved and accessible in the archive section.

6. Input Validation

- Require all necessary bill information.
- Reject bills with missing required fields.
- Reject amounts that are zero or less.
- Display clear and understandable validation messages.
- Prevent invalid bill records from being saved.

7. Due Date Reminder System

Only unpaid bills should receive active reminders.

Display the following reminders:
- 3 days before the due date: "Due in 3 days"
- 1 day before the due date: "Due tomorrow"
- On the due date: "Due today"
- After the due date: "Overdue"

Requirements:
- Display reminders on the dashboard.
- Keep reminders visible without repeated pop-up notifications.
- Stop reminders when a bill is marked as Paid or archived.
- Calculate reminders based on the current date.
- Reminders should only be visible when the application is open. Do not implement browser notifications while the application is closed.

8. Household PIN Protection

- Anyone in the household can view the dashboard and bill records.
- Require a shared household PIN before adding, editing, or archiving bills.
- Only parents and the household member responsible for paying bills should manage records.
- Do not create individual accounts, registration, or login systems.
- Provide a clearly marked configurable PIN value so the household can change it.
- Explain that this is basic PIN protection, not strong security.

9. Data Persistence

Use localStorage to save all bill records.

Requirements:
- Bills must remain saved after refreshing or reopening the browser.
- Editing and updating payment status must update the saved records.
- Archived bills must remain accessible.
- Dashboard totals and reminders must update automatically when records change.

10. Design and Theme

Use a modern, clean, minimalist, and professional green-and-white theme.

Design preferences:
- Dark green for the header and primary buttons.
- Light green accents for highlights and reminders.
- White or very light gray background.
- Rounded cards with subtle shadows.
- Clean typography and consistent spacing.
- Clear visual distinction between Paid, Unpaid, Due Soon, and Overdue statuses.
- Simple navigation and user-friendly forms.
- Avoid cluttered layouts and unnecessary decorations.

11. Responsive Web Design

Make the application fully responsive for:
- Desktop computers
- Laptops
- Tablets
- Mobile phones

Requirements:
- Automatically adapt the layout to different screen sizes.
- Display dashboard cards in organized columns on larger screens.
- Stack dashboard cards vertically on smaller screens.
- Make forms, buttons, text, and input fields fit mobile screens.
- Make bill lists or tables mobile-friendly.
- Prevent horizontal scrolling on mobile devices.
- Keep all features accessible and easy to use on every device.

Use CSS media queries, flexible layouts, and responsive sizing.

12. Important Limitations

- Store records only in the browser's localStorage.
- Do not implement automatic syncing between devices.
- Do not claim that records are shared across different devices.
- Do not implement notifications while the browser is closed.
- Use fictional sample data only if sample records are needed.

13. Final Instructions

- Create a complete and functional application, not just a visual mockup.
- Keep all HTML, CSS, and JavaScript in one file.
- Add short comments to explain important sections.
- Make sure all buttons and forms work correctly.
- Test the main features and check for JavaScript errors.
- Preserve all the requirements above.
- Save the completed application as **billkeeper.html** in the current project folder.
- After creating the application, explain how to open and test it.
- Summarize the implemented features and mention any limitations.

Do not remove or ignore any of the specified requirements.]

Prompt 2 – Design and Functionality Improvements

Date: November 25, 2026

Prompt:

Improve the existing BillKeeper application based on the following requirements. Keep all existing working features unless they are specifically requested to be changed. Do not rebuild the application from scratch. Preserve the existing HTML, CSS, JavaScript, and localStorage functionality.

1. Add a Logo
- Create a simple, professional, and recognizable logo for BillKeeper.
- Use a bill, receipt, or wallet-inspired icon.
- Display the logo beside the BillKeeper name in the header.
- Make sure the logo matches the green-and-white theme.

2. Improve the Overall Design
- Make the application look more modern, polished, clean, and professional.
- Improve the layout, spacing, typography, colors, buttons, cards, and navigation.
- Use a consistent green-and-white color palette.
- Add subtle hover effects and smooth transitions.
- Make the design visually appealing but keep it simple and easy to use.
- Maintain full responsiveness on desktop, laptop, tablet, and mobile.

3. Add a Delete Button
- Add a Delete button for bill records.
- Allow authorized household members to delete bills after entering the correct PIN.
- Show a confirmation dialog before permanently deleting a bill.
- If the user cancels, keep the bill unchanged.
- If confirmed, remove the selected bill from localStorage and update the dashboard and bill list.
- Keep the existing Archive feature separate from Delete.

4. Change the PIN Behavior
- Use **1004** as the household PIN.
- When the user clicks the Add New Bill button, immediately display a PIN input modal before opening the bill form.
- Require the correct PIN before allowing the user to add a bill.
- Also require the PIN when editing or deleting a bill.
- Do not require a PIN just to view the dashboard, All Bills, or Archived Bills.
- Do not show the PIN modal when viewing bill records.
- Do not require a PIN when marking a bill as Paid or Unpaid unless the action is part of editing.
- Display a clear error message when the PIN is incorrect.
- Make sure the PIN modal is properly designed and easy to use.

5. Dashboard Summary
- Keep all summary cards and overall bill statistics exclusively on the Dashboard.
- The Dashboard should display:
  - Total Bills
  - Unpaid Bills
  - Paid Bills
  - Due Soon
  - Total Unpaid Amount
- The All Bills page should only display the bill records and their relevant information.
- The Archived Bills page should only display archived records.
- Do not display dashboard summary cards or overall statistics on the All Bills and Archived Bills pages.
- Keep the navigation between Dashboard, All Bills, and Archived Bills working properly.

6. Add a Notification and Reminder Area
- Add a dedicated notification or reminder section on the Dashboard.
- Display reminders for unpaid bills:
  - Due in 3 days
  - Due tomorrow
  - Due today
  - Overdue
- Make reminders easy to notice and understand.
- Show the bill category, amount, due date, and reminder status.
- Do not show active reminders for Paid or Archived bills.
- Keep reminders visible while the application is open without repeatedly showing pop-up messages.
- Do not implement browser notifications when the application is closed.

7. Remove the PIN and Data Privacy Instructions at the Bottom
- Remove the explanatory PIN protection and data privacy information displayed at the bottom of the application.
- Do not remove the actual PIN functionality or localStorage functionality.
- Keep the application interface clean and focused on the main features.

8. Important Instructions
- Preserve all existing working features.
- Do not remove or break Add, View, Edit, Archive, payment status updates, reminders, or localStorage persistence.
- Make sure the new Delete feature works correctly.
- Ensure the PIN is required at the correct times.
- Make sure dashboard summaries appear only on the Dashboard.
- Check all navigation links, buttons, forms, and modals.
- Test the application for JavaScript errors.
- Update the existing `billkeeper.html` file instead of creating another application file.

After completing the changes, summarize what was improved and identify any remaining issues.

Prompt 3 – Notification Bell and Reminder System Changes

Date: November 25, 2026

Prompt:

Improve the existing BillKeeper application by replacing the separate Payment Reminders dashboard card with a notification bell system.

Follow these requirements:

1. Remove the existing Payment Reminders card from the Dashboard. Do not remove the dashboard's other summary cards.

2. Add a notification bell icon in the upper header, beside the text "Household bills saved on this device".

3. Display a small red notification badge on the bell whenever there are unread notifications. Show the unread notification count when applicable.

4. When the user clicks the notification bell, open a clean, modern notification dropdown or panel.

5. Automatically generate notifications for unpaid bills based on their due dates:
   - 3 days before: Due in 3 days
   - 1 day before: Due tomorrow
   - On the due date: Due today
   - After the due date: Overdue

6. Each notification must display:
   - Bill category
   - Bill amount
   - Due date
   - Reminder status

7. Add a "Mark as Read" action for each notification. Also provide a convenient option to mark all notifications as read.

8. Unread notifications must have a visible highlight or indicator. Read notifications should remain accessible in the notification panel but should no longer appear as unread.

9. Save notification read/unread status using localStorage so the status remains after refreshing or reopening the application.

10. Automatically update notifications when a bill is marked as Paid or Archived. Remove inactive reminders for Paid or Archived bills.

11. Prevent duplicate notifications for the same bill and reminder stage. Do not create repeated unread notifications every time the dashboard is refreshed or reopened.

12. When a bill's reminder stage changes, update or generate the appropriate notification without creating unnecessary duplicates.

13. Make the notification panel responsive and ensure it works on desktop, tablet, and mobile screens.

14. Keep the notification bell design consistent with the existing BillKeeper green-and-white theme.

Important:
- Do not use browser push notifications.
- Notifications should work inside the application only.
- Preserve all existing working features, including Add, View, Edit, Delete, Archive, PIN protection, dashboard summaries, and localStorage persistence.
- Do not recreate the application from scratch.
- Update the existing billkeeper.html file.

Prompt 4 – Dashboard UI Improvements

Date: November 25, 2026

Prompt:

Improve the existing BillKeeper dashboard to make it more professional, organized, modern, and user-friendly. Focus on improving the dashboard layout and user experience while preserving all existing working features.

1. Replace the Dashboard Greeting

- Remove the heading "Good day, family".
- Replace it with **"Household Overview"**.
- Add this subtitle below the heading:

  "Keep track of your household bills, payments, and upcoming due dates."

- Keep the current date displayed in a clean and readable format.
- Make the dashboard feel like a professional household bill management application rather than a greeting page.

2. Add a Next Payment Section

- Add a section on the Dashboard called **"Next Payment"**.
- Display the nearest upcoming unpaid bill.
- Show its:
  - Bill category
  - Amount
  - Due date
  - Remaining days before the due date
- Make this section visually noticeable but consistent with the existing design.
- Automatically update it whenever bills are added, edited, paid, archived, or deleted.
- Do not include Paid or Archived bills.
- If there are no upcoming unpaid bills, display a friendly message such as "No upcoming payments".

3. Improve the Notification Bell

- Improve the appearance and visibility of the notification bell in the upper header.
- Keep the red unread notification badge.
- Make the notification panel clean, organized, and easy to read.
- Clearly distinguish unread and read notifications.
- Display a friendly empty state when there are no notifications, such as "You're all caught up!"
- Keep the existing Mark as Read and Mark All as Read functionality.
- Preserve notification read/unread status using localStorage.
- Make sure the notification panel works properly on desktop, tablet, and mobile.

4. Improve Dashboard Summary Cards

- Keep the existing summary cards:
  - Total Bills
  - Unpaid Bills
  - Paid Bills
  - Due Soon
  - Total Unpaid Amount
- Improve their visual hierarchy, spacing, icons, and readability.
- Make sure the values are accurate and automatically update when bill records change.
- Keep all dashboard summary cards exclusively on the Dashboard.

5. Improve Overall Dashboard Appearance

- Maintain the existing green-and-white theme.
- Improve spacing, alignment, typography, card designs, and visual consistency.
- Use subtle shadows, rounded corners, and simple icons.
- Make important information easy to notice.
- Avoid unnecessary decorations and overcrowded sections.
- Maintain a clean and professional appearance.

6. Preserve Existing Functionality

- Do not remove or break existing features.
- Preserve Add, View, Edit, Delete, Archive, payment status updates, PIN protection, notification reminders, and localStorage persistence.
- Do not change the existing household PIN.
- Keep the All Bills and Archived Bills pages free from dashboard summary cards.
- Keep the application responsive on desktop, laptop, tablet, and mobile.
- Update the existing `billkeeper.html` file instead of creating a new application file.

After implementing the improvements, check the dashboard layout, Next Payment section, notification bell, and existing application functionality. Fix any errors introduced by the changes.

Prompt 5 – Fix PIN and Delete Confirmation Modal

Date: November 25, 2026

Prompt:

Fix the overlapping Household PIN and Delete Confirmation modals in the existing BillKeeper application.

Currently, clicking Delete causes the browser's native confirmation dialog and the Household PIN modal to appear at the same time. This creates overlapping dialogs, and canceling one also closes the other.

Implement the following correct sequence:

1. When the user clicks the Delete button, display only the Household PIN modal.
2. Do not display any delete confirmation dialog before PIN verification.
3. Require the correct household PIN (1004).
4. If the PIN is incorrect, keep the PIN modal open and display a clear error message.
5. If the PIN is correct, close the PIN modal first, then display a separate custom Delete Confirmation modal.
6. The Delete Confirmation modal must clearly identify the bill category and explain that deletion is permanent.
7. If the user confirms deletion, permanently remove the selected bill from localStorage and refresh all affected dashboard values, bill lists, and notifications.
8. If the user cancels deletion, close only the Delete Confirmation modal. Keep the bill record unchanged.
9. Prevent both modals from appearing simultaneously.
10. Remove the browser's native confirm() dialog and use a properly styled custom confirmation modal consistent with the BillKeeper design.
11. Make sure the same issue does not affect the Add Bill or Edit Bill PIN flows.
12. Preserve all existing application features and update the existing billkeeper.html file only.

Test the complete Delete process, including correct PIN, incorrect PIN, confirmation, cancellation, and checking that the bill is correctly retained or deleted.

Prompt 6 – Fix Responsive Layout and Resizing Issues

Date: November 25, 2026

Prompt:

Fix the responsive layout issues in the existing BillKeeper application.

Currently, when the browser window or preview area is resized, some dashboard cards and layout sections do not adjust properly and appear to remain in their original positions.

Implement the following improvements:

1. Make the entire application fluid and fully responsive. All content must automatically adjust when the browser window is enlarged, reduced, or resized.

2. Use flexible CSS layouts such as CSS Grid and Flexbox instead of fixed widths and positions wherever possible.

3. Make the main application container use available screen width appropriately while maintaining consistent spacing and reasonable maximum width on large screens.

4. Dashboard summary cards must automatically rearrange:
   - Desktop: multiple columns.
   - Tablet: fewer columns.
   - Mobile: vertically stacked cards.

5. The Next Payment, Upcoming Bills, Recent Bills, and Overdue Bills sections must also resize and rearrange properly.

6. Make the header, logo, navigation, notification bell, buttons, forms, and notification panel responsive.

7. Ensure All Bills and Archived Bills layouts also adapt to different screen sizes.

8. Prevent horizontal scrolling, overlapping elements, clipped content, and cards extending outside the visible screen.

9. Make text, buttons, and input fields readable and usable at different screen widths.

10. Use appropriate CSS media queries and flexible sizing. Avoid unnecessary fixed pixel widths and absolute positioning for the main layout.

11. Test the application at different viewport widths, including desktop, tablet, and mobile sizes. Verify that resizing the browser dynamically rearranges the layout without requiring a page refresh.

12. Preserve all existing BillKeeper functionality, design theme, PIN protection, notifications, and localStorage behavior.

Update the existing billkeeper.html file only. Do not rebuild the application from scratch.

Prompt 7 – Add 20 Sample Bills for Testing

Date: November 25, 2026

Please add 20 fictional sample household bill records to BillKeeper for testing purposes.

Requirements

1. Create 20 sample bill records using the existing bill data structure and localStorage.
2. Include a variety of categories:
   - Electricity
   - Water
   - Internet
   - Phone
   - Rent
   - Other (with custom categories such as LPG, Groceries, and Cable TV)
3. Use different bill amounts, due dates, and payment statuses (Paid and Unpaid).
4. Include bills with these due-date situations based on November 25, 2026:
   - Overdue bills
   - Due today
   - Due tomorrow
   - Due in 3 days
   - Due within the next 7 days
   - Due later in December 2026
5. Include both Paid and Unpaid records so the Dashboard summaries and reminder system can be tested properly.
6. Make the sample records appear automatically only when the app has no existing bill data. Do not add duplicates every time the app is refreshed or reopened.
7. Never overwrite, replace, or delete existing user-created bills.
8. Ensure all 20 sample records are correctly reflected in:
   - Dashboard summary cards
   - Next Payment
   - Upcoming Bills
   - Recent Bills
   - Overdue Bills
   - Notification bell and reminder panel
   - All Bills and Archived Bills sections, where applicable
9. Follow the existing Philippine Peso (₱) currency format.
10. Do not change the existing design, layout, PIN protection, or other working features.
11. Do not introduce unnecessary features or modify unrelated code.

After implementation:
- Explain which files were modified.
- Explain how the sample data is initialized.
- Confirm how the app avoids duplicate sample records.
- Summarize the changes made.

Please inspect the existing project structure and code before making changes. Review the proposed changes before applying them.

Prompt 8 – Fix HTML Label Accessibility Warning

Please inspect billkeeper.html and fix the HTML accessibility warning:

"A <label> isn't associated with a form field."
Requirements:
1. Find all label elements that are not properly associated with their corresponding form fields.
2. Connect each label to its correct input, select, or textarea using matching for and id attributes, or properly nest the form field inside its label.
3. Do not change the app's design, layout, styling, or functionality.
4. Do not modify unrelated code.
5. Check that all form labels are properly associated after the fix.

Explain which labels were fixed and what changes you made.