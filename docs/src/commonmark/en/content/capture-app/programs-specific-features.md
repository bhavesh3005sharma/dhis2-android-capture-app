# Data Sets { #capture_app_datsets }

## Data Sets in Android { #capture_app_datsets_android }

### Navigation Bar (NEW 2.4)

Use the new navigation bar to switch between the data entry form and the overview screen.

![](resources/images/image139.png){ width=25%}

### Overview Screen

The new overview tab contains the following details:

- Data set name
- Last Update
- Open/Close Status
- Period
- Org Unit
- Category option combo

![](resources/images/capture-app-image122.png){ width=25%}

#### Saving a data set

Validation rules and completion of data sets are integrated in the save button actions:

- When a data set is configured to complete only if validation passess. If the validation is successful, a dialog asking to mark as complete will show up. The app will allow completion only if all mandatory fields have value.

![](resources/images/capture-app-image131.png){ width=25%}
  
- if it is not successful, then an error dialog should show and the dataset will not be marked as complete. The description and instructions of the validation rule will be displayed to help the user identify the error.

![](resources/images/capture-app-image128.png){ width=25%}

- On a dataset that does not have setup "Complete allowed only if validation passes". When clicking on the save button; if the dataset has validation rules associated to it, then the app will ask the user to run the validation rules.
  
![](resources/images/capture-app-image130.png){ width=25%}

- If the validation is not successful, an error dialog should show but with the possibility to complete the data set anyway. The description and instructions of the validation rule will be displayed to help the user identify the error.

![](resources/images/capture-app-image129.png){ width=25%}

- If the dataset does not have validation rules, the dataset will be marked as complete if all mandatory fields have value.

### Increase Row Headers


The length of the first column in datasets is now calculated to show the full text for the Data Elements names. Users can also adjust the width to adapt it better to their screen size.

![](resources/images/capture-app-image113.png){ width=25%}

### Indicators (NEW 2.4)

Indicators are now available in default and section forms and are displayed at the bottom of the data entry form.

![](resources/images/image140.png){ width=25%}

## Supported features overview { #capture_app_datsets_supported_features }


The following is a comprehensive list of all features available for Data Sets in DHIS2 and notes on whether or not these have been implemented in the Android Capture app.

In the notes, ‘admin’ refers to someone who develops and configures a DHIS2 system, and ‘user’ refers to someone who uses apps to capture data, update it, and review reports.

|Legend|Description|
|:--:|:------|
|![](resources/icons/icon-complete.png)|Feature implemented|
|![](resources/icons/icon-incomplete.png)|Feature not implemented&nbsp;(will be ignored)|
|![](resources/icons/icon-na.png)|Not applicable|
|![](resources/icons/icon-wip.png)|Work in progress. Feature not completely implemented yet or with unexpected behaviour already reported.|


|Feature|Description of feature|Status|Notes on implementation|
|-|---|:-:|---|
|Period type|Determines the period covered by data-entry.|![](resources/icons/icon-complete.png) | |
|Expiry days|Sets the deadline (days after period) after which DHIS2 locks all data entry for the period (0 means no locks at all).  Periods can still be opened, but cells will be greyed out.| ![](resources/icons/icon-complete.png) | |
|Open future periods for data entry|This setting can be used to unlock the current period or all periods up to a certain point in the future.|![](resources/icons/icon-complete.png) | |
|Data input periods|Allows you to set a specific range of dates for a period's data-entry, and prevents data capture for periods outside of this date range.|![](resources/icons/icon-complete.png) | |
|Days after period to qualify for timely submission|Sets the deadline (days after period) after which DHIS2 treats data entry as 'late'.| ![](resources/icons/icon-complete.png)| |
|[Attribute] category combination|Allows an admin to attach a Category (set of Options) to the Data Set, generating a separate data entry screen for each Option (This is called an Attribute Category Combination in DHIS2).| ![](resources/icons/icon-complete.png)| |
|[Attribute] Category Combination option restrictions|If Attribute Category Combinations (see above) are used, then this features gives admins the ability to restrict which specific options are available in the drop-down.  Each option can be restricted to a particular range of dates and/or organisation units, and that option will not be shown if data is being captured outside of these dates or org units.| ![](resources/icons/icon-complete.png)||
|Complete notification recipients|Sends a DHIS2 message to the selected User Group when the Data Set is marked 'complete'.|![](resources/icons/icon-incomplete.png)| |
|Send notification to completing user|Sends a DHIS2 message to the data-entry user when the Data Set is marked 'complete'.|![](resources/icons/icon-incomplete.png)| |
|All fields for data elements required|Where one or more Categories are used to disaggregate a data element, this setting forces the user to either complete all disaggregations, or to leave them all empty.|![](resources/icons/icon-complete.png) | |
|Complete only if validation passes|Only allows the Data Set to be marked complete if no Validation Rules are triggered.|![](resources/icons/icon-complete.png)| |
|Skip offline|Requires the user to add a 'comment' if a value is left blank (or Data Set cannot be 'completed'). Only allows Data set to be selected for data entry while connected to the internet (although once selected, data entry can continue offline).|![](resources/icons/icon-incomplete.png)| |
|Data element decoration|Shows the description of the Data Element when the mouse hovers over the Data Element Name.|![](resources/icons/icon-complete.png) | |
|Section forms - render sections as tabs|Displays each section in the form as a separate tab, instead of all together on the same page.|![](resources/icons/icon-incomplete.png)| |
|Section forms - render vertically||![](resources/icons/icon-incomplete.png)| |
|Data Element - CatCombos|Enables an individual Data Element to be automatically disaggregated into one or more categories (eg both male/female and child/adult), with separate fields/values collected for each of these disaggregations.|![](resources/icons/icon-complete.png)| |
|Inline indicators / section form totals|Enables the default CatCombo for each data element to be overridden with a different CatCombo for this Data Set only.|![](resources/icons/icon-complete.png)| |
|Section forms - render sections as tabs|Adding indicators to Data Sets makes them available for use in section forms and custom forms; row and/or column totals can also be added to these forms.  (Both are displayed on the screen alongside data capture cells, and update automatically as values are captured.)|![](resources/icons/icon-incomplete.png)| |
|Organisation unit assignment|Ensures the Data Set is only available for those organisation units to which it has been assigned.|![](resources/icons/icon-complete.png) | |
|Compulsory data elements|This allows the marking of specific Data Elements/CatCombos as ‘compulsory’, which means users must enter a value (they cannot be left blank).| ![](resources/icons/icon-complete.png)| |
|Forms - default forms|DHIS2 automatically renders the form as table(s), with a new table started every time the Category Combinations change (= different column headings).|![](resources/icons/icon-complete.png) | |
|Forms - section forms|Form sections and section titles can be specified, giving you more control over the grouping and layout of the form (but it is still rendered automatically).  This section form automatically overrides the default form if implemented.|![](resources/icons/icon-complete.png) | |
|Forms - custom forms|A custom HTML form can be designed, giving total control over layout, and enabling JavaScript code to be included within the form.  This custom form automatically overrides the default and section forms if implemented.|![](resources/icons/icon-incomplete.png)| |
|Section forms - disable fields (grey)|With section forms, this enables you to individually 'grey out' fields (a whole data element, or specific CatCombo Options) so that users cannot enter data into it.|![](resources/icons/icon-complete.png) | |
|Multi-organisation unit forms|When this server setting is enabled, form layouts are changed to show multiple org units as rows, and all data elements/CatCombos as columns (ie very flat and wide form per org unit).|![](resources/icons/icon-incomplete.png)| |
|Data value pop-up: mark value for follow-up|Enables the user to mark this specific data value for follow-up (marked values can be reviewed in the Data Quality web app).|![](resources/icons/icon-incomplete.png)| |
|Data value pop-up: add comment to value|Enables the user to add a comment to this specific data value.|![](resources/icons/icon-incomplete.png)| |
|Data value pop-up: display data element history|Shows the history over time of this specific data element (i.e. previous 12 months' values).|![](resources/icons/icon-incomplete.png)| |
|Data value pop-up: display audit trail|Shows a history of previous edits to this specific data value.|![](resources/icons/icon-incomplete.png)| |
|Data value pop-up: min/max ranges (also accessible via Data Administration app)|This enables users to set minimum and maximum expected values for a data element, enabling DHIS2 to highlight values outside this range during data entry (but it does not prevent saving or 'completing').  You can set min/max ranges automatically/in-bulk (via the Data Administration app) or manually/individually (via the Data Entry app).|![](resources/icons/icon-incomplete.png)| |
|Print form / print blank form|Enables printing of a data-entry form, to permit data capture on paper, and data-entry later.|![](resources/icons/icon-incomplete.png)| |
|Save data|Data entered into the screen is not captured until 'saved' - until then, it is only held in memory, and is lost if power is switched off etc.|![](resources/icons/icon-complete.png)| |
|Complete data set|This enables user to mark data-entry for a period/org unit/etc as 'complete'.  Note that this is just for data-entry tracking and timeliness purposes, and does not lock the data set or prevent further edits.|![](resources/icons/icon-complete.png)| |
|Data elements: validation rules|Enables the creation of rules (at the data element level) to enforce data quality, based on comparing different values/collections of values.  (Eg number of patients seen in the month must be less than the number of visits for the month.)|![](resources/icons/icon-complete.png)| |
|Data sharing levels/Can capture data|Enables the user to add new values, edit values and delete values in the dataset.|![](resources/icons/icon-complete.png) | |
|Data sharing levels/Can view data|Enables the user to see values within the dataset.|![](resources/icons/icon-complete.png) | |
|Data sharing levels/No access|The user won’t be able to see the dataset.|![](resources/icons/icon-complete.png) | |
|Data approval workflow|If an admin selects a pre-configured Data Approval Workflow, this will be used to enforce an ‘approval’ or ‘acceptance and approval’ cascade, enabling users to sign-off and lock data.|![](resources/icons/icon-complete.png) | The process of the approval has to be done in web. Once a data set is approved, the data will not longer be editable in the app. |
|Missing values requires comment on complete|Any missing values will require a comment to justify their absence.|-||
