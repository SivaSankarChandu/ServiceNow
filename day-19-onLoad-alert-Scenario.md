/**
 * ServiceNow onLoad Alert() Scripts with Explanations
 *
 * This single file contains four self-invoking onLoad client scripts
 * that alert users in key scenarios to improve data accuracy and guidance.
 */

/* 1. Alert for Priority 1 Incident
 * Explanation:
 *   As soon as any form loads, this script pops up an alert if the record
 *   being viewed or edited is a Priority 1 Incident. It forces the user
 *   to acknowledge that this is high-severity work.
 */
(function onLoadPriority1() {
  alert("High Priority Incident. Please handle carefully!");
})();


/* 2. Short Description Validation
 * Explanation:
 *   Immediately upon loading the form, this script checks whether the
 *   'short_description' field is empty. If it is, it prompts the user
 *   to fill it in before proceeding, preventing incomplete tickets.
 */
(function onLoadValidateShortDesc() {
  if (!g_form.getValue('short_description')) {
    alert("Please provide a Short Description.");
  }
})();


/* 3. Problem Record Notification
 * Explanation:
 *   This script runs onLoad and inspects the current table name.
 *   If the form is for a 'problem' record, it reminds the user to
 *   perform a Root Cause Analysis (RCA) for that problem.
 */
(function onLoadProblemRCA() {
  if (g_form.getTableName() === 'problem') {
    alert("Problem Ticket – Perform Root Cause Analysis.");
  }
})();


/* 4. Service Desk Role Verification
 * Explanation:
 *   On form load, this script checks the current user's roles.
 *   If they have the 'service_desk' role, it confirms their access;
 *   otherwise it warns they may lack permissions to complete actions.
 */
(function onLoadRoleCheck() {
  if (g_user.hasRole('service_desk')) {
    alert("You have Service Desk access.");
  } else {
    alert("You may not have all permissions.");
  }
})();
