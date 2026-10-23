SpendWise Dashboard Shell - Project Documentation

Welcome to the SpendWise Dashboard Shell, the foundation of your capstone project. This project implements a clean, modern, and fully responsive financial dashboard layout built using modern CSS layout techniques (CSS Grid and Flexbox), custom CSS properties, and subtle micro-interactions.

---

Project Structure

The project is structured into two core files:
1. index.html: The semantic markup containing the dashboard layout, navigation, header, and the six category cards.
2. style.css: The stylesheet governing the theme, layout architecture, responsiveness, and animations.

---

What Each Part Does

1. The Macro Layout (CSS Grid)
* .dashboard-container: Uses CSS Grid (grid-template-columns: 260px 1fr) to divide the viewport into two distinct macro areas: a fixed-width sidebar for navigation on the left, and a flexible main content area that fills the remaining space on the right.
* .cards-grid: Uses a responsive CSS Grid layout (grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))) to automatically arrange the financial category cards into an organized grid that adapts to screen dimensions.

2. Internal Component Layout (Flexbox)
* Sidebar (.sidebar): Uses Flexbox (flex-direction: column) to vertically stack the brand logo and navigation links with consistent spacing.
* Header (.dashboard-header): Uses Flexbox with justify-content: space-between to separate the page title and greeting from user profile actions and notification controls.
* Cards (.card): Each financial card is structured using Flexbox to evenly distribute content between the top header (icon and status badge), the middle body (category name and financial amount), and the bottom footer (progress bar and timestamp text).

3. Theme & Custom Properties (:root)
* All design tokens—such as brand colors, background surfaces, card containers, and text hierarchy—are declared as CSS Custom Properties on the :root selector.
* Stretch Goal (Dark Theme): Automatically overrides the :root color tokens inside a @media (prefers-color-scheme: dark) query, seamlessly shifting the color palette to an accessible dark mode without altering structural styles.

4. Responsiveness (Mobile Adaptation)
* A media query (@media (max-width: 768px)) targets tablet and mobile viewports.
* Below 768px, the dashboard container collapses the two-column grid into a single-column layout, hiding the fixed sidebar and stacking the header elements and category cards vertically for optimal mobile readability.

5. Card Micro-Interactions
* Enhances user experience by implementing subtle animations on both hover and keyboard focus (:focus).
* Uses transition: transform 250ms ease, box-shadow 250ms ease; combined with transform: translateY(-4px) to give the cards a smooth "lifting" effect when interacted with, fulfilling accessibility and animation constraints.
