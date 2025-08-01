# Creating a Looker Modeled Query and Working with Quick Start

### Task 1. Create a modeled query in Explore
In this task, you will use Looker Explore to create a modeled query with dimensions, measures, and filters to provide a basic-level business insight.

In the Looker navigation menu, click Explore.

Under E-Commerce Training, click Order Items.

Select the fields below:

Under Users > Dimensions, click State.
Under Products > Dimensions, click Department.
Under Users > Measures, click Count.
Under Order Items > Measures, click Order Count.
Under Users>Dimensions, find Country and click the filter icon (filter icon) next to it to filter on the dimension.

In the Filter pane, set the Users Country filter to is equal to USA.

In the Data pane, click on the column name Users Count to sort in descending order.

Click Run and review the results data.
<img width="1917" height="910" alt="Screenshot 2025-08-01 2 22 28 PM" src="https://github.com/user-attachments/assets/9934aa9a-017e-48b7-9fb9-f4ff6e0f25ad" />



### Task 2. Save the modeled query in LookML
In this task, you will save the modeled query from Explore to LookML.

On the Explore page with modeled query, click on Settings (Settings gear icon) next to Run (top right of page), and select Get LookML.

Click the Aggregate Table tab and copy the LookML code.
<img width="1917" height="910" alt="Screenshot 2025-08-01 2 25 45 PM" src="https://github.com/user-attachments/assets/d23780cf-4129-400e-9aef-2e99fc36f2e3" />


Open a new Looker window in a new tab. On the bottom left of the Looker User Interface, click the toggle button to enter Development mode.

On the left side navigation menu of the Looker User Interface, click Develop.

Under Projects, click on qwiklabs-ecommerce.

In the training_ecommerce.model file, paste the copied code after explore order_items but before explore events, around row 43.

Lines 41 to 56 of the training_ecommerce.model script

Remove the line for aggregate_table and the ending closing parenthesis. There will now only be two closing parenthesis at the end of the explore+ definition.

Then, remove the lines for the materialization parameter including datagroup_trigger.

Add a name in the query parameter, start_from_here.

Click Save Changes.
<img width="1917" height="910" alt="Screenshot 2025-08-01 2 23 57 PM" src="https://github.com/user-attachments/assets/e7dea972-d222-46f2-9f1a-5891b2fa2def" />

Updated lines 43 to 51 of the training_ecommerce.model script
<img width="1915" height="915" alt="Screenshot 2025-08-01 2 31 36 PM" src="https://github.com/user-attachments/assets/f1b69262-d7b3-44be-a5aa-7ff3e65120f4" />

Send LookML changes from development branch to production
Click Validate LookML

Click Commit Changes & Push.

In the Commit window, add a message to specify the changes you made, and click Commit.

Click Deploy to Production.


### Task 3. Create a Look report using the modeled query

In this task, you will build a Look report using the modeled query.
<img width="1915" height="915" alt="Screenshot 2025-08-01 2 33 37 PM" src="https://github.com/user-attachments/assets/e611bc3e-2dd0-429c-9c6b-2cd56232748e" />

Open a new Looker window in a new tab.

On the left side navigation menu of the Looker User Interface, click Explore> Order Items. Click Start From Here under Quick Start.

The Start From Here action tile in the Quick Start section

In the Data pane, click on the gear icon on column name Products Department and select pivot.

In the Data pane, click on the gear icon on column name Users Count and select Hide from Visualization.
<img width="1917" height="908" alt="Screenshot 2025-08-01 2 42 36 PM" src="https://github.com/user-attachments/assets/28e3e328-4357-456d-88f9-5cde7bda6ff4" />


Expand Visualization pane and choose Column chart.

Click on the gear icon (Gear icon) in the Visualization pane. Under Plot, choose Stacked as Series Positioning.

Click on gear icon (Gear icon) next to Run (top right of page), and select Save > As a Look.

Enter a title for the Look report, Order Items Count per State. Chose the Shared folder to save the report.

Click Save.

Open a new Looker window in a new tab. Click Shared folders.

Click the Order Items Count per State Look report and review the data and visualization.

<img width="1917" height="908" alt="Screenshot 2025-08-01 2 42 42 PM" src="https://github.com/user-attachments/assets/de939e46-b0d5-48be-b7bc-f42cf06b6b6e" />


<img width="1917" height="908" alt="Screenshot 2025-08-01 2 46 12 PM" src="https://github.com/user-attachments/assets/b7c1b2d4-0091-459a-93f0-a1cca9bd3a17" />

