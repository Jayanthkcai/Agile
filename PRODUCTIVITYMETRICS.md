**DORA Matrix**
The DORA (DevOps Research and Assessment) Matrix is a framework developed by the DevOps Research and Assessment (DORA) team to measure the performance and capabilities of software delivery and operational practices within organizations. It consists of four key metrics:
- **Deployment Frequency**: How often an organization successfully deploys code to production. High deployment frequency indicates faster release cycles and agility.
- **Lead Time for Changes**: The time it takes for code changes to go from commit to deployment. Short lead times indicate efficient development processes and rapid feedback loops.
- **Mean Time to Recover (MTTR)**: The average time it takes for a system to recover from failures or incidents. Low MTTR indicates effective incident response and resilience.
- **Change Failure Rate**: The percentage of changes that result in a failure or require remediation. A low change failure rate reflects the stability and reliability of the deployment process.

**Productivity Metrics**
<table>
    <thead><tr><th>Category</th><th>Metrics</th><th>Description</th></tr></thead>
    <tbody>
        <tr><td>Availability</td><td>Uptime</td><td>- Monitor server uptime</td></tr><tr><td></td><td>Time to Restore Service (MTTR)</td><td>- Identify incidents</br>- Resolve issues</br>- Restore service within SLA</td></tr>
        <tr><td>Quality</td><td>Total Customer Defects</td><td>- Track reported defects</br>- Categorize and prioritize issues</td></tr><tr><td></td><td>Defect Aging</td><td>- Measure time from defect report to resolution</td></tr>
        <tr><td>Delivery</td><td>Deployment Frequency</td><td>- Count successful deployments per unit of time</td></tr><tr><td></td><td>Change Failure Rate</td><td>- Track failed deployments</br>- Analyze causes of failures</td></tr>
        <tr><td>Workflow</td><td>Coding Days</td><td>- Measure days spent on coding tasks</td></tr><tr><td></td><td>Commit Frequency</td><td>- Count commits to version control per developer/team</td></tr><tr><td></td><td>PR Time to Merge</td><td>- Calculate time taken for pull requests to be reviewed, approved, and merged</td></tr></tbody></table>

**Coding Days**: Suppose a person committed code for 4 days in a sprint and the calculation will look like,
    (number of days commits)/(number of person eligible days in a sprint) * min(7 , number of person eligible days in a sprint)
    (4/10) * 7 = 2.8 is the coding days

**Commit Frequency**: Suppose a person committed code in first week( Wed : 2 Times, Friday: 1 Time) and in Second Week (Mon :3 Times, Thur: 2 Times) in a sprint and the calculation will look like,
     (total number of commits)/(number of person eligible days in a sprint) * min(7 , number of person eligible days in a sprint)
     (8/10) * 7 = 5.6 is the Commit Frequency.

**JIRA**

Go to the "Issues" tab and use the JQL (JIRA Query Language) to filter 

**Individual Performance**

- **Issue Resolution**
    - Query Example: assignee = "username" AND sprint in <Sprints> AND status = Done
    - Measure Resolved Issues: Count the number of issues resolved by the individual.
- **Commit Frequency**
    - Link JIRA with Git: Use JIRA integrations with version control systems like Git.
    - Track Commits: Monitor the number of commits made by the individual linked to JIRA issues.
- **Story Points Completed**
    - Query Example: assignee = "username" AND sprint in <Sprints>
    - Measure: Calculate the total number of story points an individual completes in a sprint, which reflects their contribution to larger tasks.
- **Average Time Spent on Issues**
    - Query Example: assignee = "username" AND sprint in <Sprints>
    - Measure: Calculate the average time taken to resolve issues, providing insight into efficiency
- **Blocker Resolution**
    - Query Example: assignee = "username" AND issueType = Blocker AND status = Done
    - Measure: Track the number of high-priority issues (blockers) resolved by the individual, indicating their impact on critical tasks.

**Team Performance**
- **Burndown Chart**
    - Access Reports: Go to the "Reports" section and select "Burndown Chart."
    - Interpret Data: This chart shows the amount of work completed versus the amount of work remaining in the sprint.

- **Velocity Chart**
        - Access Reports: Go to the "Reports" section and select "Velocity Chart."
        - Measure Velocity: This chart shows the average amount of work (story points) a team completes in a sprint, which helps in understanding the team's capacity.

- **Sprint Report**
        - Access Reports: Go to the "Reports" section and select "Sprint Report."
        - Analyze Completed vs. Incomplete Work: This report gives an overview of completed and incomplete issues in the sprint, providing insight into team productivity.

- **Control Chart**
        - Access Reports: Go to the "Reports" section and select "Control Chart."
        - Cycle Time and Lead Time: Measure the cycle time and lead time for issues, indicating how long it takes for issues to move from "In Progress" to "Done."

**Cycle Time**: This is the amount of time it takes for a task to go from the start of work to completion. It measures the duration from when work actually begins on an item until it is finished.
- Example: If a developer starts working on a bug fix on Monday and completes it on Wednesday, the cycle time is 3 days.

**Lead Time**: This is the total time from when a task is requested to when it is completed. It measures the duration from when an item is added to the backlog until it is finished, including any waiting time before work starts.
- Example: If a bug is reported on Monday, the developer starts working on it on Wednesday, and it is completed by Friday, the lead time is 5 days.