# Riwi Task Manager

Plataforma para que los estudiantes de Riwi administren sus tareas:
panel, calendario, categorías, búsqueda, orden, modo claro/oscuro
y versión en español e inglés. Guarda los datos con localStorage.

## Cómo se hizo

Proyecto de la materia de IA y prompts en Riwi, dentro de un concurso
del mejor front. Las reglas no permitían editar el código a mano:
todo el resultado salió de prompts.

## Mi aporte

- Definí la idea: una página para gestionar las tareas de los
  estudiantes de Riwi, con su identidad visual y en dos idiomas.
- Con ayuda de la IA, convertí esa idea en un prompt detallado,
  con criterios de aceptación y un entregable final claro.

## Prompt utilizado

PROJECT: RIWI TASK MANAGER
Centralized Academic Task Management Platform

Act as a senior product designer, UX/UI designer, business analyst, and frontend developer.

Your goal is to design and develop a modern, polished, fully interactive frontend prototype for a web application called Riwi Task Manager.

The application should centralize all academic tasks, assignments, challenges, activities, and deadlines that Riwi students currently have distributed across different pages and platforms.

The result must look and feel like a real SaaS product, with a professional interface, excellent user experience, clear information architecture, and functional interactions.

This is a frontend-only prototype. Do not build a backend or real authentication system.

1. PROJECT OVERVIEW
The problem

Riwi students receive assignments and activities from different learning areas and platforms.

These tasks are distributed across different pages, sections, and sources, making it difficult to:

Keep track of all academic responsibilities.
Remember every deadline.
Identify which activities are more urgent.
Monitor academic progress.
Organize activities from different learning areas.
Avoid forgetting assignments or complementary activities.
The proposed solution

Build a centralized task management platform where students can access all their academic responsibilities from a single dashboard.

The platform should allow students to:

Visualize all their tasks in one place.
Organize activities by learning category.
Track task completion.
Identify approaching and overdue deadlines.
Prioritize their daily activities.
Create personal reminders and additional tasks.
Monitor their progress across different learning areas.

The main concept is:

One platform. All your tasks. No missed deadlines.

2. BUSINESS REQUIREMENTS

The application must fulfill the following business objectives:

Centralize academic activities from multiple simulated sources.
Reduce the likelihood of forgotten or missed assignments.
Improve student organization and time management.
Make deadlines and task priorities immediately visible.
Provide a personalized experience for different simulated students.
Allow students to manage both official academic activities and personal reminders.
Display progress across all learning categories.

Since this is a frontend-only prototype, simulate the integration of different Riwi pages and platforms using realistic mock data. Do not claim that the application is actually connected to Riwi's systems.

3. TASK CATEGORIES

The application must support four main categories.

Each category should have a distinct visual identity.

3.1 Development

Programming-related activities, including:

Coding challenges.
Programming exercises.
Projects.
Technical assignments.
Complementary programming activities.
Research and documentation.

Suggested icon: Code-2.

Suggested color: Riwi Purple (#6857E8).

3.2 English

English learning activities, including:

Speaking.
Listening.
Grammar.
Vocabulary.
Writing.
Presentations.
English assignments.

Suggested icon: Languages.

Suggested color: Blue (#2563EB).

3.3 Socio-emotional Skills

Activities related to personal and professional development, including:

Teamwork.
Communication.
Leadership.
Personal reflection.
Emotional intelligence.
Collaboration.
Personal development activities.

Suggested icon: Brain.

Suggested color: Pink (#DB2777).

3.4 Other

A flexible category for activities that do not fit into the previous categories.

Examples:

Administrative responsibilities.
Additional assignments.
Personal reminders.
Special activities.
Complementary tasks.
Miscellaneous responsibilities.

Suggested icon: Layers.

Suggested color: Gray (#64748B).

IMPORTANT:

The four categories must remain independent and fixed.

Students must also be able to choose a task type independently of its category.

Examples:

Development + Main Challenge.
Development + Complementary Activity.
English + Practice.
Socio-emotional Skills + Reflection.
Other + Personal Reminder.

Do not create unnecessary categories for every type of activity.

4. TASK MANAGEMENT SYSTEM

Every task should have the following properties:

Unique ID.
Task title.
Description.
Category.
Task type.
Deadline.
Completion status.
Priority.
Source or origin.
Creation date.
Optional notes.
Optional external source URL.
Task types

Include flexible predefined task types:

Main Challenge.
Practice.
Complementary Activity.
Project.
Assessment.
Personal Reminder.
Administrative Task.
Other.

The task type must be optional and independent of the main category.

Task statuses

Support the following states:

Pending.
In Progress.
Completed.
Overdue.

Overdue status should be calculated automatically when a deadline passes and the task has not been completed.

Task creation

Implement a highly accessible Quick Add Task feature.

The button should be easy to find, preferably in the dashboard header and/or as a floating action button.

When clicked, open a modal or side panel containing:

Task title.
Description.
Category selection.
Task type.
Deadline.
Priority.
Source.
Optional notes.

The user should be able to create a task quickly without navigating through multiple pages.

Include form validation and clear feedback.

Students must also be able to:

Edit tasks.
Delete tasks, with a confirmation step.
Mark tasks as completed.
Reopen completed tasks.
Change task status.
View detailed task information.

Use localStorage to persist changes between page reloads.

5. DEADLINE AND PRIORITY SYSTEM

This is one of the most important features of the application.

The visual system must immediately communicate which tasks require attention.

Use dynamic deadline indicators based on the current date.

Suggested logic:

Completed: Green.
More than 7 days remaining: Neutral gray.
4–7 days remaining: Yellow.
1–3 days remaining: Orange.
Due today: Red.
Overdue: Dark red.

Completed tasks must always remain green, regardless of their original deadline.

Priority should also be independent of deadline proximity.

Support:

Low.
Medium.
High.

Display deadline labels such as:

Due in 10 days.
Due in 3 days.
Due tomorrow.
Due today.
Overdue by 2 days.
Completed.

Use readable labels and icons in addition to color. Never rely on color alone to communicate task status.

The deadline system must update automatically according to the current date.

6. LANGUAGE SELECTOR — SPANISH AND ENGLISH

This is an important feature of the application.

Implement a language selector in the top-right corner of the interface.

It must be visible on:

Landing page.
Simulated login page.
Main dashboard.
All internal application pages.
Language options

Support two complete interface languages:

🇨🇴 Español (ES).
🇺🇸 English (EN).

Use a compact, elegant language selector with recognizable flag icons and language labels or abbreviations.

Suggested appearance:

[ 🇨🇴 ES | 🇺🇸 EN ]

The selector should be easy to identify without taking too much space.

Translation requirements

The entire application must be translated, not just the main headings.

All visible interface elements must change language when the student switches languages, including:

Navigation menu.
Page titles.
Buttons.
Task categories.
Task types.
Task statuses.
Priority labels.
Dashboard statistics.
Form labels.
Input placeholders.
Search and filters.
Calendar.
Date formatting.
Notifications.
Confirmation dialogs.
Empty states.
Error messages.
Success messages.
Tooltips.
Landing page content.
Login page content.
Settings.
Progress and analytics sections.

Use natural translations, not literal or awkward translations.

Important translation examples
English	Español
Dashboard	Panel principal
My Tasks	Mis tareas
Development	Desarrollo
English	Inglés
Socio-emotional Skills	Habilidades socioemocionales
Other	Otro
Completed	Completada
Pending	Pendiente
In Progress	En progreso
Overdue	Vencida
Due Today	Vence hoy
Upcoming Deadlines	Próximas entregas
Quick Add Task	Agregar tarea
My Learning Journey	Mi progreso de aprendizaje
Settings	Configuración
Save Changes	Guardar cambios
Cancel	Cancelar
Delete Task	Eliminar tarea
Technical implementation

Implement a centralized internationalization system (i18n).

Preferred options:

react-i18next.
i18next.
Another appropriate React internationalization solution.

Do not hardcode interface text directly into components.

Store translations in organized language dictionaries or translation files.

Use language keys to render the appropriate text.

The selected language must persist using localStorage.

When the user refreshes the page, the selected language must remain active.

The language selector must update the interface immediately without reloading the application.

Date and localization support

Dates should adapt to the selected language.

Spanish:

DD/MM/YYYY.
Spanish month and weekday names.
Natural Spanish deadline labels.

English:

MM/DD/YYYY.
English month and weekday names.
Natural English deadline labels.

Use appropriate locale formatting through JavaScript Intl APIs.

Important: Changing the interface language must never change the actual task deadlines or user data.

7. LANDING PAGE

Create a professional landing page that introduces the platform.

It should include:

Header
Riwi logo.
Navigation links.
Language selector in the top-right corner.
CTA button to access the platform.
Hero section
Platform name: Riwi Task Manager.
A clear headline explaining the main value proposition.
A short description.
A prominent CTA button: "Get Started" / "Comenzar".
A visual preview or mockup of the dashboard.

Suggested headline:

"Your entire learning journey, organized in one place."

Spanish version:

"Tu proceso de aprendizaje, organizado en un solo lugar."

Suggested description:

"Keep track of every assignment, challenge, and deadline. Stay organized, monitor your progress, and never miss an important task again."

Spanish version:

"Organiza tus actividades, controla tus entregas y mantén el seguimiento de tu progreso. Nunca vuelvas a olvidar una tarea importante."

Features section

Showcase the main benefits:

Centralized tasks.
Smart deadline tracking.
Progress monitoring.
Personalized dashboard.
Quick task creation.
Final CTA

Encourage students to access their dashboard.

The landing page should be visually attractive but not excessively long.

8. SIMULATED LOGIN AND STUDENT PROFILES

Create a simulated authentication experience.

There is no backend or real user authentication.

The login screen should include:

Riwi branding.
A welcome message.
Student selection.
A simulated login button.
Language selector.

Provide at least three different mock student profiles.

Each profile should have:

A different name.
A different avatar or initials.
Different task distributions.
Different completed and pending tasks.
Different deadlines.
Different progress percentages.

The purpose is to demonstrate how different Riwi students would experience the platform.

Allow users to switch between simulated accounts.

Switching accounts must load the corresponding task dataset and preserve individual progress using localStorage.

9. MAIN DASHBOARD

The dashboard is the core of the application.

It must be the first screen students see after accessing their simulated account.

Use a clean, modern dashboard layout.

9.1 Sidebar navigation

Include:

Dashboard.
My Tasks.
Calendar.
Categories.
My Learning Journey.
Settings.

The sidebar should include:

Riwi logo or brand representation.
Navigation icons.
Active navigation state.
Student profile information.
Logout or switch account option.

On mobile, use a collapsible sidebar or appropriate mobile navigation.

9.2 Dashboard header

Display:

Personalized greeting.
Current date.
Search bar.
Notifications or reminders icon.
Language selector.
Quick Add Task button.
Student avatar.
9.3 Summary cards

Display the following statistics:

Total Tasks.
Completed.
Pending.
Overdue.
Due Soon.

Each card should include a relevant icon, number, and subtle visual indicator.

Make sure the values are calculated from the actual mock task data and update when tasks change.

9.4 Category overview

Display four visual cards:

Development.
English.
Socio-emotional Skills.
Other.

Each card should display:

Category icon.
Number of total tasks.
Completed tasks.
Pending tasks.
Completion percentage.
Progress bar.

Make the cards clickable so users can filter tasks by category.

9.5 Today's Focus

Create a section called "Today's Focus".

Display tasks that:

Are due today.
Are overdue.
Have approaching deadlines.
Have high priority.

Prioritize urgent tasks.

9.6 Upcoming Deadlines

Create a section showing upcoming assignments ordered by deadline.

Use visual urgency indicators.

9.7 Recent Activity

Display recent student actions, such as:

Task completed.
New task created.
Deadline updated.
Task reopened.

Use realistic mock activity data.

10. MY TASKS PAGE

Create a dedicated task management page.

This page should provide a complete view of all activities.

Include:

Search

Allow searching by:

Task title.
Description.
Category.
Filters

Allow filtering by:

Category.
Status.
Priority.
Task type.
Deadline.
Source.
Sorting

Allow sorting by:

Closest deadline.
Furthest deadline.
Priority.
Recently created.
Alphabetical order.
View modes

Provide at least two view modes:

List view.
Card view.

Every task should display:

Title.
Category.
Task type.
Deadline.
Priority.
Status.
Source.

Use clear visual hierarchy and avoid overcrowded task cards.

Include empty states when no tasks match the selected filters.

11. CALENDAR PAGE

Create a calendar where students can visualize all their tasks and deadlines.

Include:

Monthly calendar view.
Weekly view if feasible.
Task indicators on the corresponding dates.
Category color indicators.
Deadline details when selecting a task or date.
Navigation between months.

Allow users to quickly identify days with multiple deadlines.

Use the same task data as the main dashboard.

The calendar must adapt its language and date formatting to the selected locale.

12. MY LEARNING JOURNEY

Create a page that visualizes the student's overall academic progress.

Include:

Overall completion percentage.
Completed versus pending tasks.
Progress by category.
Completed tasks over time.
Learning activity statistics.

The goal is to make students feel that they are progressing through their learning journey.

Use simple and readable charts.

Do not invent academic grades or performance evaluations. Only visualize task-management data.

All chart labels and legends must support both languages.

13. SETTINGS

Create a simple settings page.

Include:

Student profile information.
Simulated account switching.
Language preferences.
Theme preferences if feasible.
Notification preferences.
Task display preferences.

The language preference should also be accessible from the global header.

Changing the language in Settings or the header must update the entire application.

14. QUICK ADD TASK — IMPORTANT FEATURE

This feature deserves special attention.

Students often receive instructions verbally or through different platforms.

They should be able to register these activities immediately.

Implement a Quick Add Task button that is accessible throughout the application.

It should allow users to add an activity in a few steps.

Suggested interaction:

Click Quick Add Task.
Enter the title.
Select a category.
Set a deadline.
Optionally select a task type and priority.
Save.

The task should immediately appear in the dashboard, task list, calendar, and corresponding category.

All labels, validation messages, and confirmation messages must adapt to the selected language.

This feature is essential to the product concept.

15. VISUAL IDENTITY AND DESIGN SYSTEM

Use the provided Riwi logo as the primary visual reference.

The interface should reflect the brand identity without making the design excessively dark or visually heavy.

Primary color palette
Deep Navy: #171B49.
Riwi Purple: #6857E8.
White: #FFFFFF.
Soft Gray: #F4F5FA.
Semantic colors
Green: #22C55E — Completed tasks.
Yellow: #EAB308 — Approaching deadlines.
Orange: #F97316 — Urgent tasks.
Red: #EF4444 — Due today.
Dark Red: #B91C1C — Overdue tasks.
Category colors
Development: #6857E8.
English: #2563EB.
Socio-emotional Skills: #DB2777.
Other: #64748B.
Design guidelines

Use:

Clean white surfaces.
Soft gray backgrounds.
Subtle shadows.
Rounded corners.
Consistent spacing.
Modern typography.
Clear visual hierarchy.
Minimal but meaningful animations.
Consistent iconography.

Suggested visual style:

Modern SaaS dashboard, minimal, professional, friendly, and productivity-oriented.

Avoid:

Excessive gradients.
Too many competing colors.
Overloaded dashboards.
Unnecessary animations.
Inconsistent spacing.
Excessive use of decorative elements.

Prioritize usability over decoration.

The language selector should be visually consistent with the rest of the interface, compact, and easy to access.

16. UX/UI AND ACCESSIBILITY REQUIREMENTS

The application must follow good UX/UI principles.

Prioritize:

Clear navigation.
Consistent interaction patterns.
Immediate visual feedback.
Responsive layouts.
Readable typography.
Accessible color contrast.
Keyboard-friendly interactions.
Meaningful empty states.
Clear confirmation messages.
Error handling.
Reusable components.

Important UX details:

Confirm before deleting tasks.
Provide feedback when tasks are saved or updated.
Keep the Quick Add Task action easily accessible.
Make task status changes intuitive.
Avoid unnecessary navigation.
Preserve filters when appropriate.
Make the dashboard useful at a glance.
Make the language selector accessible on every major screen.

The application should be easy to understand even for a first-time user.

17. TECHNOLOGY AND ARCHITECTURE

Choose a modern frontend technology stack.

Preferred technologies:

React.
TypeScript.
Tailwind CSS.
Lucide icons.
Recharts or another suitable chart library.
React Router if routing is needed.
react-i18next and i18next for internationalization.

Use reusable components and a clean project structure.

Suggested component architecture:

Layout.
Sidebar.
Header.
LanguageSelector.
Dashboard.
SummaryCard.
CategoryCard.
TaskCard.
TaskList.
TaskForm.
QuickAddTask.
DeadlineBadge.
ProgressBar.
Calendar.
Charts.
StudentProfile.

Create a centralized task data model and reusable functions for:

Deadline calculations.
Task status.
Category statistics.
Progress calculations.
Filtering.
Sorting.
Locale-aware date formatting.

Use localStorage for:

Simulated student accounts.
Task creation and editing.
Completion status.
Language preference.
Preferences.
Individual student progress.

Use separate translation dictionaries for Spanish and English.

No backend, external database, or real authentication is required.

Avoid unnecessary dependencies.

18. MOCK DATA

Populate the application with realistic sample data.

Include at least:

Three simulated students.
20–30 tasks distributed across the four categories.
Different deadlines.
Completed tasks.
Pending tasks.
In-progress tasks.
Overdue tasks.
High, medium, and low priorities.
Different task types.
Different task sources.

Make sure the data is realistic and diverse.

The dashboard must not look empty.

The mock data should demonstrate all important application features.

Include tasks from simulated sources such as:

Riwi learning platform.
Development challenges.
English activities.
Instructor assignments.
Personal reminders.

Do not represent these mock sources as actual integrations.

Store task category and status as stable internal values rather than translated strings. Translate them only when displaying them in the interface.

This ensures that switching languages does not corrupt task data or filters.

19. RESPONSIVENESS

The application must work properly on:

Desktop.
Laptop.
Tablet.
Mobile.

Desktop should be the primary design target.

On mobile:

Sidebar should become a collapsible menu.
Cards should adapt to smaller screens.
Task lists should remain readable.
Forms should be easy to complete.
Buttons should have appropriate touch targets.
Language selector should remain accessible.

Do not simply shrink the desktop interface. Adapt the layout to the device.

20. FUNCTIONALITY AND QUALITY REQUIREMENTS

This is not a static visual mockup.

Every visible interactive element should perform its intended action.

Verify that:

Landing page navigation works.
Simulated login works.
Account switching works.
Dashboard statistics update dynamically.
Category filtering works.
Search works.
Sorting works.
Task creation works.
Task editing works.
Task deletion works.
Task completion works.
Completed tasks can be reopened.
Deadline indicators update dynamically.
Calendar displays the correct tasks.
Progress indicators update correctly.
Language switching works instantly.
All screens are fully translated.
Language preference persists after reload.
Date formatting changes with the language.
Switching languages does not modify task data.
localStorage persistence works.
Responsive navigation works.

Avoid placeholder buttons that do nothing.

If a feature is visually represented, it should have a functional interaction or be clearly marked as a prototype element.

21. FINAL DELIVERABLE

Build a complete, polished, interactive frontend prototype.

The final product must include:

Landing page.
Simulated login.
Multiple simulated student profiles.
Main dashboard.
Four task categories.
Task management system.
Quick Add Task functionality.
Dynamic deadline indicators.
Search, filtering, and sorting.
Calendar.
My Learning Journey.
Settings.
Spanish and English language selector.
Complete interface internationalization.
LocalStorage persistence.
Responsive design.
FINAL INSTRUCTIONS

Before implementation:

Analyze the business requirements.
Establish the information architecture.
Define the reusable component structure.
Plan the main user flows.
Define the internationalization strategy.
Ensure the visual design is consistent with Riwi's identity.

Then implement the application.

Prioritize a cohesive product experience rather than building isolated screens.

Do not stop after creating the landing page or a static dashboard.

Make sure the entire prototype is navigable and interactive.

The result should demonstrate how Riwi students could manage their entire academic workload through one centralized platform, with the flexibility to use the interface in either Spanish or English.

The ultimate goal: Help students stay organized, take control of their learning journey, and never miss an important task again.