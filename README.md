# Class-579-Week-1-Portfolio-Entry---QA-Dashboard
A web application for tracking quality assurance tasks and risk levels, as well as providing alerts for high-risk items.

**Live Demo**
https://v0-simple-qa-dashboard.vercel.app/

**Overview**
This QA Risk Dashboard was developed to prevent system integration failures like the "Payroll Meltdown" scenario inspired by UK Rail System and "The Phoenix Project." The dashboard helps validate systems integrations, track cross-team dependencies, and sends alerts before going live.

**Features**

**Run QA Check Button:** Simulates refreshing data from backend systems

**CSV Upload:** Supports uploading task data with a defined format

**Summary Statistics:**
Clickable cards showing the number of incomplete tasks
Clickable cards showing high-risk issues
Toggle filters to view specific task categories

**Responsive Task Table:**
Department
Task name
Completion Status (✅/❌)
Risk Level (None, Medium, High — color-coded)
Notes

**Alert System:** Shows Slack-style warnings for critical high-risk tasks with:
Expandable details
Team-specific suggestions
Comment capability for team communication

**Interactive QA Checklist:** Organized by department for easy tracking

**Filtering Capability:** Easily filter to view incomplete or high-risk tasks

**Data Export:** Download filtered tasks, alerts, and checklists

**Modern UI:** Clean, readable design with cards, badges, and simple fonts

_________________________________________________________________________________________
**Screenshots**

**Dashboard Overview**
![image](https://github.com/user-attachments/assets/1d2d68f3-0330-4d8f-ab5e-ba571c60ffcd)
Dashboard Overview Main dashboard shows summary cards for incomplete tasks and high-risk issues

**Filtered View**
![image](https://github.com/user-attachments/assets/a4d11aba-8dd0-49ef-bf4e-a7251c6850b1)
Filtered View Table filtered to show only high-risk issues

**Task Table**
![image](https://github.com/user-attachments/assets/a6040904-6829-438f-9697-1275840fc7c7)
Task Table Responsive table displaying all QA tasks with completion status and risk levels

**Risk Alerts**
![image](https://github.com/user-attachments/assets/dc84bedd-0569-44f4-b1f4-c7be2d424d43)
Risk Alerts: Slack-style warning cards for high-risk items grouped by department

**Alert Details**
![image](https://github.com/user-attachments/assets/e3177d54-e348-491f-a99b-33be1133a8c9)
Alert Detail:s Expanded alert showing details and allowing for team communication

**QA Checklist**
![image](https://github.com/user-attachments/assets/6b88e3cd-46a3-43e0-b8c9-39169d19a91b)
QA Checklist Interactive checklist organized by department for tracking completion

-----------------------------------------------------------------------------------------------------
**Video Walkthrough**

https://youtu.be/OpK_aLamGSg

**Technologies Used**
- React.js
- Next.js
- CSS/Tailwind CSS
- JSON for mock data (easily replaceable with real API data)


**Usage**
- Click "Run QA Check" to simulate refreshing the data
- Upload CSV files with the specified format to analyze new tasks
- Use the summary cards to filter for incomplete tasks or high-risk issues
- Review the table for detailed information on all tasks
- Check the alerts section for critical warnings
- Download filtered data, alerts, or checklists as needed


**Risk Assessment Logic**
The dashboard analyzes task notes to automatically identify risk levels using keyword detection:

- // High risk keywords

const HIGH_RISK_KEYWORDS = ["assumed", "unverified", "outdated", "no one responded", "critical", "urgent", "failed"];


- // Medium risk keywords

const MEDIUM_RISK_KEYWORDS = ["delayed", "pending", "waiting", "scheduled", "partial"];

Tasks containing high-risk keywords are flagged for immediate attention, while those with medium-risk keywords are highlighted for monitoring. This automated risk assessment helps teams quickly identify potential integration issues before deployment.

**Installation**
1. Clone the repository:

- git clone https://github.com/your-username/qa-risk-dashboard.git
2. Navigate to the project directory:
  
- cd qa-risk-dashboard

3. Install dependencies:

- npm install

5. Run the development server:

- npm run dev

7. Open your browser and visit http://localhost:3000

**Future Enhancements**
- Integration with real backend APIs
- Authentication system
- Email notification system
- Historical data tracking
- Custom risk assessment algorithms
- Enhanced team collaboration features
- Automated remediation suggestions
