# 🥛 Doodh Tracker – Dairy Delivery & Billing System

A simple, mobile-friendly web application that helps a local dairy shopkeeper track daily doorstep milk delivery, confirm that each customer has received the milk, send a "milk delivered" message, and collect monthly payments with accurate, itemised bills and timely reminders.

---

## 1. Problem Statement

Small dairy shopkeepers usually record milk deliveries in a paper notebook. This causes several everyday problems:

- Deliveries are missed, forgotten or written down wrongly.
- Customers dispute the monthly bill because they cannot see which days they received milk.
- Calculating each customer's total litres and amount at month end takes a lot of time.
- Shopkeepers forget to follow up with customers who have not paid.
- Customers who do not read English find written messages hard to follow.

## 2. Objective

To give the shopkeeper one easy tool that:

1. Records the milk delivered to every customer every day.
2. Notifies the customer that the milk has been delivered at their doorstep, **only after it has been received**.
3. Keeps an accurate month-wise record of each customer's milk purchase.
4. Calculates the final amount to be paid and sends it to the customer directly.
5. Reminds the shopkeeper, month after month, about unpaid bills.
6. Works in the language each customer is comfortable with.

## 3. Key Features

### Daily Delivery
- Customer list with default daily quantity (in litres) and rate per litre.
- Quantity can be changed for any day (extra milk, half a litre, or no milk).
- A **"Delivered & received"** button confirms the milk has reached the customer. Only confirmed deliveries are counted in the bill.
- An automatic **"Milk delivered at your doorstep"** message is prepared for the customer, including the milk total and amount for the month so far.
- **Mark all received** for quick one-tap entry, and an **Undo** option for mistakes.
- A progress bar shows how many deliveries are completed for the day.

### Monthly Billing
- Each customer's bill shows the date-wise litres, number of days, total litres, rate, total amount, payments already made and the **final amount to pay**.
- A ready-to-send bill message with the full month detail.
- **Record payment** to reduce the pending balance (full or partial payments).
- **Print / Save as PDF** option for a formal bill.

### Payment Reminders
- The shopkeeper chooses a day of the month from which reminders start.
- From that day, a banner appears at the top of the app listing customers who have not paid last month's bill, with the total pending amount.
- One click takes the shopkeeper to the bill screen to send the reminders.

### Payment History
- A running list of every payment received, with date, customer name and the month it was for.

### Multi-language Support
- The whole app can be switched between **English, हिन्दी (Hindi) and मराठी (Marathi)**.
- Each customer has their own **message language**, so one customer can receive Hindi messages while another receives Marathi or English.

### Dashboard and Design
- Summary cards for litres delivered today, billing for the month and money collected.
- Colourful avatars, rounded cards, a gradient header and friendly empty screens.
- Responsive layout for phones and computers, with automatic dark mode.

## 4. How It Works (Workflow)

1. **Setup:** The shopkeeper enters the shop name and adds customers with their name, mobile number, daily litres, rate per litre and preferred message language.
2. **Every day:** The shopkeeper opens the *Delivery* tab, adjusts the quantity if needed, and presses **Delivered & received** once the customer has the milk.
3. **Instant message:** The app prepares the delivery message in the customer's language. The shopkeeper sends it with the **WhatsApp** or **SMS** button, or copies it.
4. **Month end:** In the *Bill* tab the app totals the month's received milk for each customer and shows the final amount.
5. **Reminder and payment:** The reminder banner shows unpaid customers. The shopkeeper sends the bill message and later records the payment, which updates the balance and the history.

## 5. Technologies Used

| Part | Technology |
|------|------------|
| Structure | HTML5 |
| Styling | CSS3 (flexbox, grid, media queries for dark mode and print) |
| Logic | Vanilla JavaScript (no frameworks or libraries) |
| Data storage | Browser `localStorage` |
| Messaging | WhatsApp click-to-chat links (`wa.me`) and `sms:` links |

## 6. Project Structure

```
dairy-project/
├── index.html   # Page structure
├── style.css    # Design, layout, dark mode and print styles
├── script.js    # Application logic, translations and billing
└── README.md    # Project description
```

## 7. How to Run

1. Keep all files in the **same folder** with the names shown above.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari). No installation or internet connection is needed to use it.
3. To make it available online, upload the folder to a free host such as Netlify, GitHub Pages or Cloudflare Pages.

## 8. Limitations

- Messages are **prepared** by the app, but the shopkeeper still presses the WhatsApp or SMS button to send them. Nothing is sent automatically.
- Reminders appear as a banner when the app is opened. They are not push notifications.
- Data is stored in the browser of the device being used. It is not shared between devices, and clearing the browser data will erase it.
- Hindi and Marathi translations should be reviewed by a native speaker before being used with customers.

## 9. Future Scope

- A backend (for example Flask or Node.js with SQLite or MySQL) so data is stored on a server and shared across devices.
- Fully automatic SMS or WhatsApp sending through a messaging service such as Twilio or MSG91, including scheduled monthly reminders.
- Online payment links (UPI) inside the bill message.
- Customer login to view their own delivery calendar and bills.
- Delivery-boy accounts and route planning.
- Monthly reports and charts for sales, collections and pending dues.
- Backup and export of data to Excel or PDF.
- An Android app version.

## 10. Conclusion

Doodh Tracker replaces the paper notebook with a clear, accurate and easy-to-use digital record. It reduces billing disputes, saves the shopkeeper's time at month end, helps in recovering payments on time, and keeps customers informed in their own language.
