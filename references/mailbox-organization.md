# Mailbox organization

Use this reference for classification, folder and label naming, merging categories, incoming-mail rules, and exceptions. Read current mailbox evidence before making changes; past account names, browser tabs, labels, and rules may have changed.

## Establish the outcome for each account

Confirm the account and provider from the live mailbox. A custom-domain address does not establish which provider hosts it. Reuse an appropriate authenticated tab or connector; do not transfer cookies or tokens between browsers.

Distinguish three independent choices: which existing mail to classify, what happens to future mail, and whether classified mail remains in the inbox. Gmail custom labels can coexist with the Inbox label; applying one does not archive the message. A folder-based provider may move a message out of the inbox. Carry the user's choice forward for the relevant account instead of assuming all accounts use the same behavior.

When the user authorizes organizing all clear categories, inspect the mail, choose bounded categories, and complete both historical classification and requested future rules. Ask only where a meaningful boundary or inbox-retention choice remains unresolved. Do not repeat an already answered question.

## Build categories from the mail

Review sender, subject, current location, and relevant dates across the requested range before choosing categories. Use the mailbox's actual work types and recurring correspondence rather than importing another account's taxonomy. Read bodies only when metadata cannot resolve the classification.

Prefer short, consistent names that help the user review work. Fix obvious typos and reuse suitable existing categories. Separate broad work types from service-specific categories only when that distinction helps retrieval. Keep ambiguous mail available for review rather than forcing it into a category or deleting it as unneeded.

Prefer verified sender addresses or domains for recurring categories. Use a subject condition when the same sender delivers different types of mail, such as pull-request discussion and workflow runs. Verify each historical sender variant; a display name alone is not a reliable future rule. Do not collect unrelated services into a rule simply because their messages contain a common word.

## Rename and merge without losing mail

Rename a suitable existing label or folder when its identity should remain the same. When merging categories, add or move every authorized item to the destination, verify coverage, and then remove the obsolete label or folder using the provider's actual semantics. Removing a Gmail label does not delete its messages; deleting a folder on another provider may delete its contents.

Check rules that reference renamed or merged categories. Some providers retain a stable label ID; others require an explicit destination update. Read back the saved destination and enabled state. Preserve manual ordering unless sorting or reordering was requested; if the user wants to sort personally, open the relevant management view for them.

## Keep verification mail available

When the user asks for verification mail to stay in the inbox without categories, treat this as an exception to the relevant classification and cleanup rules. Apply it to each named account. Include verification codes, one-time passwords, device or account verification, and sign-in links as supported by the user's scope and observed mail.

Use distinctive subject phrases and verified sender evidence. Consider the languages and variants actually present, including wording such as `verification code`, `confirmation code`, `one-time password`, `log in code`, `sign in code`, `login link`, `verify your email`, `验证码`, and `驗證碼`. These are starting points, not a complete universal detector. Check variants in existing mail and do not claim keyword rules can recognize every possible future wording.

Avoid broad matches on `code`, `verify`, or body boilerplate: code repositories, artist verification correspondence, and contracts mentioning an access code can be ordinary work. A login or bank activity alert is not automatically a one-time credential. Preserve uncertain business correspondence for review.

For existing matches, inspect location before changing it. Remove custom classification labels and move active mail to the inbox as requested. Distinguish system categories from custom labels. Exclude Trash, Spam, and sent-only mail unless the user requests otherwise; a new inbox-retention preference does not authorize restoring mail previously deleted. Preserve read state, stars, attachments, and unrelated labels or actions.

Do not open authentication links or expose code values, token-bearing URLs, or message bodies in logs, screenshots, examples, or reports. Report subjects only when necessary, with embedded codes omitted.

## Make future rules agree with the exception

Inspect every enabled rule that could move, label, archive, or delete the excepted mail, including older rules. On Gmail, matching filters apply independently: an additional rule that keeps mail in the inbox does not cancel another filter's custom label or delete action. Add the exception to all conflicting filters and preserve their other conditions and actions.

On providers with ordered rules, verify priority and whether processing actually stops after a match. A new first rule is sufficient only if the provider supports and saves the required stop behavior. Otherwise, add exclusions to the conflicting rules. Do not assume moving to the inbox prevents a later rule from moving it elsewhere.

Preserve Boolean logic. Adding a negative subject condition to an ANY group can broaden the rule to almost all mail. Express the intended logic as the original positive match AND NOT any verification match, using supported grouping or equivalent separate rules. Check that ordinary category mail still matches and verification mail does not.

Historical changes and future rules are separate operations. A provider's “apply to existing mail” prompt may cover only the inbox, not custom folders. Updating exclusions will not necessarily remove labels already applied. Do not rerun unrelated classification or delete actions on historical mail merely to save a rule.

## Provider details and browser recovery

- **Gmail:** Manage filters under Settings → See all settings → Filters and Blocked Addresses. Exclusions can use the “Doesn't have” field with supported search operators. Confirm the final negative query and unchanged action list. Remove old custom labels separately. Multi-selection label menus may show a mixed state as checked; verify the actual unchecked state before applying removal.
- **QQ Mail:** Manage rules under Settings → Incoming-mail rules. Verify ALL versus ANY conditions, the subject operator, destination, and enabled state. A subject “does not contain any” condition can express an exception under ALL conditions. The UI may limit values per condition; split the list into additional negative conditions and read back every saved value. Do not assume a historical-execution prompt covers folders outside the inbox.

Use the current UI and supported tool schemas rather than fixed selectors or limits. Inspect values after text entry, especially with an input method active. If filling a field does not update the application state, use a supported input or focus action and check the resulting value; do not submit a malformed address or query.

After navigation or a save, use a fresh observation before choosing the next action. Search loading can hide an edit panel, and a warning can make the background controls inaccessible. Reopen the appropriate panel or resolve the actual warning, then verify the saved rule. A click, closed dialog, or temporary counter is not proof of persistence. On an uncertain result, inspect the current rule before adding another condition or retrying the mutation.

## Verify and report

Read back saved conditions, destinations, actions, enabled states, and applicable priority. Check changed mail across the requested scope, including pagination, and confirm both location and custom labels. Counts may represent messages or conversations; name the unit accurately and do not treat a visible page as the entire mailbox.

For verification exceptions, check representative positive matches and ordinary category mail that should remain classified. Verify that active matched mail is in the inbox without the excluded custom labels. State any wording, search-range, login, or provider limitations that remain; do not call an incomplete rule migration complete.

Report the actual changes briefly. Keep account-specific category lists and rule details in the user's mailbox or authorized private task material, never in the public skill or its examples. Leave a requested management preview open; close only the tabs the user asked to close.
