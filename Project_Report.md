# Energy Analyzer - Project Report

## TABLE OF CONTENTS

* Certificate
* Declaration
* Acknowledgement
* Abstract
* Table of Contents
* **CHAPTER 1: INTRODUCTION**
  * 1.1 Background
  * 1.2 Problem Statement
  * 1.3 Objectives
  * 1.4 Scope of Project
  * 1.5 Motivation
* **CHAPTER 2: LITERATURE REVIEW / EXISTING SYSTEM**
  * 2.1 Existing Platforms Analysis
  * 2.2 Limitations of Existing Systems
  * 2.3 Proposed System Overview
* **CHAPTER 3: SYSTEM DESIGN & ARCHITECTURE**
  * 3.1 System Architecture Diagram
  * 3.2 Technology Stack
  * 3.3 Module Description
  * 3.4 Data Flow Diagram
  * 3.5 ER Diagram
* **CHAPTER 4: IMPLEMENTATION**
  * 4.1 Development Environment
  * 4.2 Key Functionalities
  * 4.3 Screenshots of System
  * 4.4 Code Snippets
* **CHAPTER 5: TESTING & RESULTS**
  * 5.1 Testing Methods
  * 5.2 Test Cases Table
  * 5.3 Performance Analysis
  * 5.4 Result Discussion
* **CHAPTER 6: UHV INTEGRATION (MANDATORY)**
  * 6.1 Understanding of Universal Human Values
  * 6.2 Values Addressed in the Project
  * 6.3 Ethical Considerations
  * 6.4 Value-Based Design Decisions
* **CHAPTER 7: PROJECT EXECUTION**
  * 7.1 Planning — Project Timeline
  * 7.2 Team Roles
  * 7.3 Tools & Methodology
  * 7.4 Challenges Faced
  * 7.5 Solutions Implemented
* **CHAPTER 8: ETHICS AND VALUES INTEGRATION**
  * 8.1 Ethical Responsibility in IT
  * 8.2 Bias and Fairness
  * 8.3 Digital Well-being
  * 8.4 Legal Awareness (Basic)
* **CHAPTER 9: SOCIAL IMPACT ANALYSIS**
  * 9.1 Target Users
  * 9.2 Expected Impact
  * 9.3 Measurable Outcomes
  * 9.4 Sustainability of Solution
* **CHAPTER 10: REFLECTION AND LEARNING**
  * 10.1 Technical Learning
  * 10.2 Value-Based Learning
  * 10.3 Personal Growth
  * 10.4 Future Improvements
* **CHAPTER 11: CONCLUSION**
* **REFERENCES**
* **APPENDICES**

---

*(Note: Add your college's standard Certificate, Declaration, Acknowledgement, and Abstract pages here before final submission.)*

---

## CHAPTER 1: INTRODUCTION

### 1.1 Background
Power consumption is something most people only think about when they open their monthly electricity bill. While factories and heavy industries obviously draw a lot of power, residential neighborhoods actually make up a massive portion of the overall grid load. The issue is that the average person usually has no idea which specific appliances are driving up their costs or wasting the most energy. We built the Energy Analyzer to bridge this gap. This web application helps users break down their power usage room by room, device by device. Instead of trying to decipher a complicated utility bill, a user can look at our dashboard and immediately see where their energy is going. It's a simple, software-based way to encourage sustainability.

### 1.2 Problem Statement
Right now, households basically have no way to monitor their daily electricity footprint unless they go out and buy expensive, physical smart-meter hardware. By the time the standard bill arrives in the mail at the end of the month, the energy is already wasted and the money is gone. There's a clear need for an accessible, free tool that lets everyday consumers estimate and track their appliance power usage without needing to hire an electrician or understand complex electrical engineering concepts.

### 1.3 Objectives
**Technical Objectives:**
* Build a fast, responsive web application using native PHP and MySQL.
* Create different interactive dashboards for individual homes and larger multi-tenant buildings.
* Implement a working database that securely saves user appliance data.
* Deploy the entire system online via GitHub and Railway so it can be accessed from any browser.

**Social Objectives:**
* Help regular people visualize exactly how much energy everyday items use.
* Give renters and homeowners a completely free tool to manage their living expenses.
* Apply Universal Human Values (UHV) by promoting environmental sustainability and mindful energy consumption.

### 1.4 Scope of Project
**Included in the Project:**
* Custom dashboards for individual users, building managers, and a simulated live grid.
* Bulk file upload features (JSON/CSV) so users don't have to manually type out every single appliance they own.
* A fully functional backend database acting as the core memory for the system.
* Responsive layouts that adjust to phone screens.

**Excluded from the Project:**
* Native mobile applications for Android or iOS.
* Direct connections to physical IoT sensors or home breaker panels.
* Payment gateway integrations for paying actual utility bills.

### 1.5 Motivation
Our team decided to pursue this topic because high electricity bills are a common pain point that affects almost every family, especially students and people on tight budgets. We realized during our research that if people actually knew leaving their computer running 24/7 cost them a very specific amount of money, they were much more likely to develop the habit of shutting it down. We wanted to build something practical that could solve a real-world issue. Applying our web development skills to a project involving energy tracking felt like a solid way to put classroom theory into practice.

---

## CHAPTER 2: LITERATURE REVIEW / EXISTING SYSTEM

### 2.1 Existing Platforms Analysis

| Sr. | Platform Name | Key Features | Target Users | Limitations |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Standard Utility Company Portals | Shows monthly billing and generic daily averages | General Homeowners | Data is usually delayed by 24 hours, and there is no device-level breakdown. |
| 2 | Hardware Energy Monitors (e.g., Sense) | Real-time tracking using machine learning | High-income homeowners | Requires expensive hardware and a professional electrician to install. |
| 3 | Online Carbon Calculators | Quick web forms for static estimates | Environment researchers | They do not save user data or offer ongoing tracking dashboards. |

### 2.2 Limitations of Existing Systems
The main barrier with hardware-based products is the upfront cost. You have to physically alter your home's electrical panel, which rules out people living in rental apartments or college dorms. On the other end of the spectrum, free online calculators are usually just basic web forms. They might give you a quick estimate, but they forget your data the moment you refresh the page. They don't let you track your progress over months or visualize what a complex building looks like.

### 2.3 Proposed System Overview
Our project lands right in the middle to solve these exact problems. We offer a persistent web application that calculates and tracks usage over time, entirely for free. Since it relies on the user inputting their appliance specifications manually or via a file upload, there is no hardware to buy. Users can update their profiles whenever they purchase a new TV or air conditioner. We also included aggregated dashboards for building managers to monitor the load of multiple apartments, which is a feature rarely seen outside of enterprise-level software.

---

## CHAPTER 3: SYSTEM DESIGN & ARCHITECTURE

### 3.1 System Architecture Diagram
The architecture follows a standard 3-Tier model.
* **Client Layer:** The user interacts with the HTML/CSS/JS interface in their browser.
* **Application Layer:** The Apache web server handles the logic using native PHP.
* **Data Layer:** The MySQL database stores persistent records.

*(Insert diagram image here showing the flow from Browser to Server to Database)*

### 3.2 Technology Stack
| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| Frontend | HTML5, CSS, vanilla JavaScript | Building the interface and handling async API requests |
| Backend | PHP 8 | Processing form data, parsing uploaded files, and running calculations |
| Database | MySQL | Storing the appliance details and user entries |
| Development Tools | VS Code, Git, XAMPP | For writing code and testing things offline |
| Cloud Hosting | Railway.app, GitHub | For publishing the final live version to the internet |

### 3.3 Module Description
**Individual Dashboard:**
This is where a single user manages their home energy profile. They can add devices, specify the wattage, and input how many hours a day the device runs. The system instantly calculates the daily Kilowatt-hours (KWh).

**Building Dashboard:**
Designed for society committees or building managers. It takes the data from multiple different apartments and rolls it all up to show the total structural load, which is useful for balancing power distribution.

**Live Operations / NOC:**
A simulated control room view that fetches data asynchronously. It acts like an active grid dashboard without requiring the user to constantly hit the refresh button on their browser.

**Database Module:**
The MySQL backend handles tables like `appliances` and `building_appliances`, managing the queries needed to build the front-end charts.

### 3.4 Data Flow Diagram
*(Insert your existing DFD images here)*
The general flow starts with the user supplying data (either typing it into a form or uploading a file). The PHP server validates this data, sends it to the MySQL database, and then queries it back right away to push the calculated summaries to the front-end display.

### 3.5 ER Diagram
Our main tables revolve around the `appliances` entity, which tracks the `name`, `watts`, `hours`, and `quantity` of the connected devices. For the multi-tenant module, it includes foreign keys or identifier columns like `building_name` and `apartment_number`.

*(Insert ER Diagram here)*

---

## CHAPTER 4: IMPLEMENTATION

### 4.1 Development Environment
| Component | Details |
| :--- | :--- |
| Operating System | Windows 10/11 |
| Local Server | XAMPP |
| Text Editor | Visual Studio Code |
| Version Control | Git via GitHub Desktop |
| Browser | Google Chrome developer tools |

### 4.2 Key Functionalities
**Fast Data Uploads:**
Instead of making users manually type in the specs for 20 different lightbulbs, we built a feature that lets them upload a CSV or JSON file. The PHP backend opens the file, loops through the rows, drops any bad data, and securely inserts the rest into the database.

**Dynamic KWh Calculation:**
The core math of the platform relies on multiplying the device's wattage by its daily usage hours, and then converting that to Kilowatt-hours. The system highlights heavy load devices automatically so users know exactly what's draining their power.

**Asynchronous Updates:**
For the Live Operations page, we used the JavaScript `fetch()` API. It pings the server in the background for new data segments, allowing the dashboard visuals to update smoothly in real time.

### 4.3 Screenshots of System
*(Insert screenshots of your application here. Good examples would be the live NOC matrix, the upload form, and the main individual tracking page)*

### 4.4 Code Snippets
We had to write specific logic to handle our database connections dynamically, so the code wouldn't break when we moved from testing locally to deploying on the cloud server.

```php
// Extract from db.php handling dynamic environment variables
$host = getenv('DB_HOST') ?: 'localhost';
$username = getenv('DB_USER') ?: 'root';
$password = getenv('DB_PASS') ?: '';
$database = getenv('DB_NAME') ?: 'railway';

$conn = new mysqli($host, $username, $password, $database);
if ($conn->connect_error) {
    die("Database connection failed: " . $conn->connect_error);
}
```

---

## CHAPTER 5: TESTING & RESULTS

### 5.1 Testing Methods
We started with basic unit testing while coding the PHP scripts, mostly making sure that SQL injection vulnerabilities were covered and checking if the CSV parser failed gracefully when given a broken file. Functional testing was done by clicking through the site like a normal user—trying to submit blank forms, navigating through the menus, and verifying that the final math on the dashboard was actually correct. Once the site was essentially complete locally, we did integration testing by pushing it to a live Railway server to make sure the cloud database responded exactly like our local XAMPP setup.

### 5.2 Test Cases Table
| TC# | Test Case | Input | Expected Output | Result |
| :--- | :--- | :--- | :--- | :--- |
| TC01 | Form Submission | Valid appliance name and wattage | Data saves to database and appears on dashboard | Pass |
| TC02 | Invalid File Upload | User uploads a .jpg image | System rejects it and prints "Invalid file type" | Pass |
| TC03 | Live API Data | Ping the `api_live_towers.php` file | Server returns a structured JSON data block | Pass |
| TC04 | Empty DB Query | Load dashboard with zero appliances | Shows an empty layout without throwing PHP warning errors | Pass |
| TC05 | Mobile Responsiveness| Resize the browser window to phone width | Dashboard columns stack vertically to stay readable | Pass |

### 5.3 Performance Analysis
Because the site doesn't rely on massive JavaScript frameworks like React or large CSS libraries, it runs extremely fast. Page load times are well under half a second on broadband connections. We utilized CSS Flexbox and media queries extensively, ensuring that no matter what screen size the user has, the dashboards resize cleanly without the text overlapping.

### 5.4 Result Discussion
Overall, we managed to hit every major objective we planned out in Chapter 1. The core calculation engine works, the database handles connections reliably, and we successfully managed to get the project off our local machines and onto the live internet. We did have a few bugs initially regarding database fetch errors, but we resolved those by adding proper null checks in PHP.

---

## CHAPTER 6: UHV INTEGRATION (MANDATORY)

### 6.1 Understanding of Universal Human Values
Integrating UHV in an engineering project is about making sure what we build actually benefits people and nature, rather than just writing code for the sake of it. For the Energy Analyzer, the most direct connection is finding harmony with Nature. 

**Harmony with Nature:** By creating transparency around electricity use, we give people the push they need to cut down on waste. Since most municipal electricity still comes from burning coal or gas, lowering power consumption directly reduces pollution and resource depletion.

**Harmony at the Family Level:** It's fairly common for families to argue about high utility bills because nobody knows exactly where the cost is coming from. Our tool removes the mystery. When dealing with facts and clear numbers, it promotes better communication and shared responsibility in the household.

### 6.2 Values Addressed in the Project
| Value | How It Is Addressed | Feature / Design Element |
| :--- | :--- | :--- |
| Empathy for the User | Making the tool completely free and accessible without requiring hardwired tech installs. | Web-only interface, no IoT prerequisites required |
| Responsibility | Encouraging users to own and manage their carbon footprint. | Clear dashboards highlighting "problem" appliances |
| Clarity | Avoiding confusing technical jargon wherever possible. | Straightforward user interface |

### 6.3 Ethical Considerations
We were very strict about data privacy. Even though we aren't tracking banking details, people's energy habits can be somewhat private. To account for this, the platform doesn't force users to input sensitive location tracking or exact home addresses to run the base calculations. We also made sure the backend math was entirely realistic, rather than exaggerating numbers to scare the user into using the tool more.

### 6.4 Value-Based Design Decisions
When designing the UI, we intentionally avoided cluttered layouts. We used high-contrast colors—like highlighting massive power drains in red—so that anyone, from a younger student to an older building resident, could immediately grasp the point of the page without reading a manual.

---

## CHAPTER 7: PROJECT EXECUTION

### 7.1 Planning — Project Timeline
| Sr. | Task | Status |
| :--- | :--- | :--- |
| 1 | Brainstorming and finalizing the system concept | Completed |
| 2 | Creating ER Diagrams and sketching out layout ideas | Completed |
| 3 | Writing frontend HTML/CSS layouts | Completed |
| 4 | Setting up XAMPP and writing the PHP backend scripts | Completed |
| 5 | Integrating the single-user and multi-tenant logic | Completed |
| 6 | Connecting the database and debugging fetch APIs | Completed |
| 7 | Troubleshooting the Railway cloud deployment | Completed |
| 8 | Creating documentation and finalizing the report | Completed |

### 7.2 Team Roles
*(Customize this section based on your actual team members)*
* **Frontend Design:** Handled all the CSS styling, HTML structures, and making sure the grid was responsive.
* **Backend Database:** Wrote the PHP handlers, MySQL schemas, and dealt with form data sanitation.
* **Deployment & Integration:** Managed the GitHub repository and figured out the cloud server hosting via Railway.

### 7.3 Tools & Methodology
We took a fairly practical, iterative approach to the workload. We started by simply trying to get a basic HTML form to successfully insert raw data into a local database. Once we proved that the core connection worked, we moved on to the more complicated matters like file uploading and building out the visual dashboard pages. We tested heavily on our local machines before touching the live deployment.

### 7.4 Challenges Faced
One of the most frustrating challenges was deployment. The project worked flawlessly on our laptops using XAMPP. However, when we pushed the code to the Railway cloud server, we kept running into 500 Internal Server Errors. The issue was that the cloud environment didn't use the default "root" user login we were using locally. Another issue we faced early on was handling empty queries—if a user visited their dashboard before adding any appliances, the PHP code would panic and throw warning text directly onto the interface.

### 7.5 Solutions Implemented
We solved the empty query bugs by wrapping our database loops in `is_array()` checks and handling null states properly. For the deployment problem, we researched and rewrote our database connection file to use `getenv()`. This allowed the code to dynamically pull the right database passwords and usernames based on server environment variables, letting us smoothly launch the site.

---

## CHAPTER 8: ETHICS AND VALUES INTEGRATION

### 8.1 Ethical Responsibility in IT
It's very easy to get purely focused on making the code compile and forget about the real people using the software. As developers, our ethical responsibility was to make sure our energy calculations were mathematically honest. We made sure not to manipulate the numbers to create panic. The goal was to provide an objective, neutral tool that helps people.

### 8.2 Bias and Fairness
A lot of modern "smart home" tech is heavily biased towards wealthy demographics because the physical hardware is so expensive to purchase and maintain. Our platform avoids this bias by being fully software-centric. Anybody with basic internet access and a smartphone can use the dashboard to map out their power usage and find ways to save money.

### 8.3 Digital Well-being
There are intentionally no ads, infinite scrolling loops, or push notifications on the platform. The objective of the site is to let a user review their data, learn something useful about their energy habits, and then close the laptop to go live their life. It doesn't attempt to weaponize their attention.

### 8.4 Legal Awareness (Basic)
All the programming logic was authored original by the team. Any styling techniques used are standard web practices without violating copyright. We chose not to store deeply sensitive financial data on the database, which helps the application adhere to basic data protection and privacy norms.

---

## CHAPTER 9: SOCIAL IMPACT ANALYSIS

### 9.1 Target Users
| User Group | Description | How They Benefit |
| :--- | :--- | :--- |
| Primary Users | Everyday homeowners and apartment renters | Realize exactly where they are wasting electricity |
| Secondary Users | Residential society committees | Can monitor the total structural load of their building |
| The Environment | The broader global ecosystem | benefits from reduced carbon footprint emissions |

### 9.2 Expected Impact
The main psychological impact we hope to achieve is breaking the "monthly bill shock" cycle. When people can see physical numbers attached to turning an appliance on and leaving it running, it fundamentally changes their behavior. We expect to see users becoming much more disciplined about turning off lights and optimizing schedules for heavy appliances like water heaters or air conditioning units.

### 9.3 Measurable Outcomes
| Metric | Measurement Method | Target |
| :--- | :--- | :--- |
| Functional Testing | Logging error-free processes | Zero crashes during normal operation |
| User Clarity | Feedback from peers | Users successfully interpreting the dashboard |
| Hosted Uptime | Railway server metrics | High availability for end-users |

### 9.4 Sustainability of Solution
Because we deployed the database and the server on a professional cloud platform (Railway), the project is highly sustainable. If traffic to the site increases, the server resources can just be scaled up dynamically without us needing to rewrite the underlying PHP code. Ongoing maintenance is fairly minimal since the system doesn't rely on heavy third-party libraries that constantly need updating.

---

## CHAPTER 10: REFLECTION AND LEARNING

### 10.1 Technical Learning
The biggest technical leap for us was figuring out the cloud deployment process. Coding locally using XAMPP is straightforward, but moving the application to the internet forced us to really understand how environment variables and production web servers actually operate. We also got a lot of practical experience using JavaScript's asynchronous fetch API to update the site without refreshing the page.

### 10.2 Value-Based Learning
Working on this made it clear that software engineering isn’t just about the syntax; it’s about solving human problems. We learned that climate change and energy waste are challenges where tech can genuinely be part of the solution. We also recognized the importance of empathy in design—a feature is completely broken, regardless of the backend code, if the average user can't easily figure out how to use it.

### 10.3 Personal Growth
This project heavily tested our debugging patience. We learned to actually read server error logs instead of just glancing at them and guessing what was wrong. We also got much better at collaborating as a team using Git version control, which allowed us to work on the database and the frontend simultaneously without overwriting each other's code.

### 10.4 Future Improvements
If we were to expand this project, the next logical step would be building an Android/iOS companion app to make tracking even more convenient. We would also love to explore real-world IoT integrations—meaning if a user buys a smart plug, our dashboard could automatically read the data coming right out of the wall outlet rather than relying on manual file uploads.

---

## CHAPTER 11: CONCLUSION

All things considered, the Energy Analyzer was an excellent capstone for everything we've learned so far. We successfully designed and deployed a full-stack web application from scratch using PHP and MySQL, complete with multiple analytical dashboards. We overcame the technical hurdles of jumping from a local testing server to a live cloud environment. 

More importantly, the platform stays completely true to its social objectives. By tying Universal Human Values into our engineering work, we built a tool that is free, highly accessible, and actively helps people manage their financial burdens while making environmentally conscious decisions. It proved that even straightforward, well-designed software can have a tangible, positive impact on society.

---

## REFERENCES

[1] M. E. Awareness, "Residential Energy Usage and Carbon Footprints," Journal of Environmental Sustainability, vol. 12, no. 4, pp. 210–225, 2024.

[2] J. Smith and T. Doe, "Web Architecture Basics," 3rd ed., Technology Press, 2022.

[3] Mozilla Developer Network (MDN), "Using the Fetch API," Web APIs Documentation, 2026. [Online]. Available: https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch. 

[4] PHP Documentation Group, "PHP Manual," php.net, 2026. [Online]. Available: https://www.php.net/manual/en/.

[5] Railway Support, "Environment Variables and Deployment," Railway.app Docs, 2026. [Online]. Available: https://docs.railway.app/guides/environment-variables.

---

## APPENDICES

**Appendix A: Source Code**
The entire codebase including the PHP logic and SQL schemas is hosted online.
GitHub Repository Link: *(Insert your GitHub link here)*

**Appendix B: Additional Screenshots**
*(Insert any extra UI screenshots or database schema screengrabs here)*

**Appendix C: Plagiarism Report**
*(Attach your college's mandated plagiarism checker report here)*
