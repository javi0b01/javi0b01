# :memo: Notes
## BRAINSTORMING
### MotorLog
A Vehicle Maintenance & Expense Tracker  
A dedicated logbook for vehicle owners to track fuel-ups, maintenance, and other
expenses, providing key insights into the vehicle's performance and true cost of
ownership.  
* Core Features:
  1. User Accounts: Users can sign up and log in.
  2. Vehicle Profiles: A user can add one or more vehicles to their "garage." Each
    vehicle will have a name, make, model, year, and initial odometer reading.
  3. Log Entries (The Core CRUD): Users can add, view, edit, and delete different
    types of log entries for each vehicle:
    * Fuel-Up: Track odometer reading, fuel volume (gallons/liters), and total
      cost.
    * Maintenance: Track odometer reading, service type (e.g., "Oil Change,"
      "Chain Clean," "Tire Replacement"), parts/materials used, cost, and general
      notes.
    * Other Expenses: Log recurring costs like insurance, registration, or one-off
      costs like parking tickets or new gear.
  4. Dashboard & Analytics: For each vehicle, the dashboard will automatically
    calculate and display:
    * A complete, reverse-chronological history of all log entries.
    * Key stats: Average fuel economy, average cost per mile, total running cost,
      etc.
* Why it's the perfect project: It has simple CRUD at its heart but opens the door to
  fascinating data processing and visualization challenges. It's the ideal mix of
  "easy to start" and "room to grow with advanced features."
Technology Stack  
NestJS + Angular/React: A more structured TypeScript backend with a modern frontend.  
Stack and structure:
* NestJS (Backend): A fantastic choice. It provides a strong, opinionated
  architecture on top of Node.js. Since it uses TypeScript, it will pair perfectly
  with Angular, allowing for potential code-sharing of interfaces and types. It's
  built for scalability and maintainability.
* Angular (Frontend): A powerful, feature-rich framework. Its component-based
  architecture and built-in tools will make it easy to build the different views we
  need (dashboard, log entry forms, vehicle profiles).
* PostgreSQL (Database): A rock-solid, open-source relational database. It's the
  perfect choice for the structured data we'll have (users, vehicles, maintenance
  logs with relationships between them).
* Two Repositories & Docker: This is the key to a clean, professional workflow.
  * It enforces a strict separation between the backend API and the frontend
    client.
  * It allows us to develop, test, and deploy them independently.
  * Using Docker in each repository guarantees a consistent environment for both
    development and production, which solves a lot of potential setup headaches.
This is a first-class plan. We're ready to start.  
Here is the initial plan to set up the project structure:  
1. Create a root directory for our entire project called motorlog-monorepo.
2. Inside motorlog-monorepo, create the two sub-directories: motorlog-backend and
  motorlog-frontend.
3. Set up the NestJS starter project in motorlog-backend.
4. Set up the Angular starter project in motorlog-frontend.
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
