# Xanadu

Xanadu is a framework for developing Database Driven Web Apps. 

Xanadu uses PHP, MySQL, HTML, Bootstrap, CSS, and Javascript with several amazing includes.

We've been developing Database Apps for decades with FileMaker and Xojo. FileMaker rocks but licensing became too expensive. Xojo has fantastic pricing, but is perpetually buggy. We had to find an alternative platform. PHP kept coming up in our searches. Long story short, we decided PHP is the best option just to get back to an affordable and solid platform.

Read more about Xanadu: https://campsoftware.com/products/xanadu.php

# Xanadu Pro Change Log

Use when possible: [ Fixed, Updated, Moved, Added, Removed, Renamed, Replaced, Decided, NOTE ]

2025-06-17-16-57-14
- Removed Xanadu from GitHub. No longer using git until there's a reason.

2025-06-17-15-32-51
- Added to XanLabs a ChartJS example. Also refactored how examples are loaded.

2025-06-17-14-37-08
- Added a sample PWA app in /pwa/. Safari's limitations make it less useful.
- Fixed missing renaming of Modules and Recs attributes.
- Added an openWeatherMapAPI class with functions for both  City and GPS Coordinates.
- Added an openWeatherMapAPI Setting for the API Key.
- Added \xan\strCaseTitleSmart that ignored 'small' words.

2025-06-13-12-50-02
- Renamed moduleMini properties to start with a lowercase char.

  2025-06-12-16-26-28
- Added module->tablesRelatedParentA and module->tablesRelatedChildA.
- Renamed module properties to start with a lowercase char.

2025-06-12-14-02-51
- Moved to from CampSolutionsInc to campsoftware

2025-06-12-14-01-04
- Moved to from campsoftware to CampSolutionsInc

2025-06-12-12-27-30
- Updated recs->recordDelete to combine recordDeleteRelated.

2025-06-11-16-51-54
- Added anchors to calls to 'window.location.href = "/logout' to find where the unexcpected logouts occur.
- Renamed recSaveAfter to recSaveAfterJS to be clear about its purpose.
- Updated ProjectsTasks recSaveAfterJS Trigger check refactor added a function moduleTriggerWait.

2025-06-11-15-27-22
- Removed modules->recMassageDo in favor of running some empty functions instead.
- Removed modules rec Before/After Traits by commenting them out.

2025-06-11-11-56-08
- Renamed tons for consistency.

2025-06-10-17-59-36
- Updated functions files to organize functions.
- Renamed tons for consistency.

2025-06-09-16-41-21
- Updated Sales and Projects recTitle and recColFormattingTags.

2025-06-09-15-40-08
- Fixed a bug in recsPDO.php. Fixed by assuming values are strings unless is_numeric.

2025-06-09-14-54-04
- Added Schema DataTypeSimple to set nulls to the correct type defaulting to "" or 0. Works with MySQL COUNT, but does not work with SUM, AVG, MIN, MAX, GROUP_CONCAT, STDDEV, VARIANCE if no recs ard found. COUNT will equal zero, but the others will be null. Can use COALESCE( SUM( Amount ), 0 ) to not return a null.

2025-06-09-11-01-38
- Fixed an issue in module->recCol_Picker.
- Renamed functions-internet.php emailAddressIsValid to emailAddressIsNotValid.
- Added functions-internet.php emailAddressIsValid.
- Updated eleTable->render default width from 99% to 100%

2025-06-08-17-03-50
- Updated recs and recsPDO to set all null values to an empty string.
- Updated two functions files using AI Find Problems. Fixed a few issues.
- Updated functions-dataMassage.php params to accept "?dataType $var" and immediately replace a null "$var ??= ''"

2025-06-07-18-21-28
- Updated \xan\recs but commented out for now. Looking into dealing with unexpected NULLs.
- Updated ProjectsTasks->recMassage Titles formatted as "Hal Notes" to check for nulls in the exploded values. Added a check for a hyphen in \xan\strLeft( $taskDesc1, 1 ).

2025-06-07-14-44-53
- Removed window.logoutAutoDT and replaced with a local variable.
- Updated ProjectsTasks to process notes formatted as "Hal Notes".

2025-06-06-15-37-33
- Added calls to xanAutoLogoutCheck in xanDoSave and xanDo.

2025-06-06-14-48-07
- Updated xan.js.js to show its Minified Timestamp.
- Updated xanAutoLogoutCheck in page-resp.php and xan.js.js.
- Removed all router redundant calls to \aloe\session_init in favor of one call.

2025-06-05-15-41-34
- Updated do-print.php to pass a table instead of values.

2025-06-05-12-45-01
- Removed $addBottomBorder and $backgroundColor from the TAGS_CELL_* functions. Was used in one function.

2025-06-05-11-15-43
- Fixed a bug in xan.js.js xanDoSave.
- Updated pdf-default to share a style.css file.
- Updated do-print.php files to use the shared style.css file.
- Updated pdf-default to no longer use a default header, instead replacing "[[HEADER]]".
- Added a new element recCol_StringInlineMPDF that calls recCol_StringInline and removes all uses of "!important" which has issues in mPDF.
- Updated Projects do-print.php.

2025-05-31-15-49-46
- Updated ProjectsTasks recColFormattingTags.

2025-05-31-15-11-36
- Added function xanStrPatternCount to xan.js.js.
- Added resp->jsSelectorTriggerChange.
- Added xanDoSave option with default to only update the Saved Column.
- Fixed a bug in eleTable.php setting \xan\tags->extrasD.
- Change the function order in \xan\modules to group recColFormattingTags with recMassage and recSaveAfter with tableTriggersInstall.

2025-05-29-12-16-25
- Updated recCol Portal function parameters to be in the same general order as Non Portal functions.

2025-05-29-11-49-59
- Fixed a bug in xan.js.js to check for null on xanTimeTotal.
- Fixed a bug in eleTable.php that was putting out one "<>" for each record - 1.
- Updated Projects.

2025-05-27-16-18-25
- NOTE: Been tracking load time of Xanadu and was getting worried that it's taking around 1.5 sec to load the page in Safari. Chrome and Firefox both load in HALF the time.
- Updated doSave to display 4 decimials rather than 3.
- Updated Projects Module.

2025-05-25-13-01-05
- Replaced the longer Message Names.

2025-05-24-15-10-31
- Updated xan.js.js to now show the xanMessageDisplayQueue serially with a message count. This prevents the Queue from wrapping to multiple lines.

2025-05-23-17-47-01
- Updated xanDoSave to handle regular inputs and hidden/select inputs.
- Updated \xan\recs recordInsert and recordUpdate to be more efficent and correct.
- Updated init.php to set session clean up.
- Updated ProjectsTasks to by default set the Status to "Not Started" and SortOrder to count of existing recs + 1.

2025-05-22-14-28-18
- Added in page-resp.php, the AutoLogout code page-resp.php after taking it out recently.
- Added in init.php, PHP INI values for session.cookie_lifetime set to APP_COOKIE_SESSION_SECONDS [2 hours] and session.gc_maxlifetime set to APP_COOKIE_SESSION_SECONDS_MAX [12 hours]. This may fix the AutoLogout issue of random logouts.

2025-05-21-18-03-01
- Commiting Again

2025-05-21-18-03-01
- Updated the Selected Record Checkboxes titles. That caused a bug reading the xan.js function xanSelectionLoad_Checkboxes.
- Updated Icons for the Print Menu.
- Updated Icons for Actions Running Man to FI_ACTION_DB.
- Added IDs to List and Portal Checkboxes to reduce warnings in FireFox and Chrome. DatePickr still spawn warnings...
- Updated init.php Include URL and Path and NGINX to use a shared local "includes" folder.
- Updated \xan\modules->cardPortal Selection Checkboxes to set the ID.
- Fixed ProjectsTasks New Record from ProjectsItems New Item Button.
- Deleted from Comms Portal the Addresses code from when Comms and Addresses were split.

2025-05-19-13-11-08
- Fixed bug with List Selection Checkboxes clicks going to the record instead of ticking.

2025-05-19-10-45-11
- Updated page-resp.php to use JS Navigation Timing.
- Updated xan.js.js xanDoSave, xanDo, xanDoProgress, and xanDoResponse to include Browser and PHP timing like: BrowserTime [ServerTime].
- Moved setting $pageload_begin = \microtime( true ); from init.php to index.php and now setting a Response Header for "xanTimeTotal".

2025-05-17-17-57-45
- Updated \xan\module->recColRenderAs to encode the value as the first step rather than after tags are applied.
- Updated \xan\module->recColRenderAs and Updated \xan\module->recCol_StringInline to pass $subValuePairsD to run a substitute on the value and keeping its \xan\module->recColFormattingTags. An example is Active: Yes => Active, No => Inactive.
- Added \xan\strSubstituteValuePairsD. Can pass a string to substitute an array of value pairs.
- Modified \xan\eleLabel from span to div.
- Added constants QS and QD for Single Quotes and Double Quotes.
- Updated Contacts module to use the updated \xan\module->recCol_StringInline with $subValuePairsD.

2025-05-17-16-06-46
- Updated modules content-page.php to no longer show an error if a detail record does not exist.

2025-05-17-14-45-33
- Fixed a bug with UUIDContactsTagsJoin where they keyname in the database had Join captialized.
- Removed an unused parameter on \xan\module->recCol_Picker_Content.

2025-05-16-14-56-24
- Fixed a bug in eleDate, eleDateTime, and eleTime where the selectors were using a class, not an ID.

2025-05-16-12-20-42
- Updated and Removed the caching of some Module function "Chunks" like recImage, recTitleBrief, recTitleMore.
- Updated the function "Chunks" to no longer pass the Table KeyName.

2025-05-13-16-40-35
- Removed an extra call to \xan\eleMeta.
- Renamed \xan\modules->recTitleBriefHeader to \xan\modules->recTitleHeader.
- Renamed \xan\modules->recTitleBriefMore to \xan\modules->recTitleMore.
- Updated \xan\modules->recTitleBrief and \xan\modules->recTitleMore value comparisons like ( $recs->colValue( 'Active' ) === "Yes" ? "Active" : "Inactive" ) ).

2025-05-13-14-27-37
- Removed xan.js.php and moved the code to init.php.
- Updated init.php to read xan.js.js and minify to xan.js.
- Updated init.php to read xan.css.css and minify to xan.css.
- Moved the SearchBar Filter Tooltip from the Find Button to the Clear Button.
- Updated DB_LIMIT from 100 to 50.

2025-05-11-15-55-08
- Moved functions recID and recCount from \xan\modules to \xan\recs.
- Renamed \xan\recs colNamesToMassageA to massageColNamesA and massageRowForGUI to massageColsForGUI.

2025-05-11-15-02-24
- Updated all \xan\module instances function order for the main functions.
- Updated several \xan\modules Conditional Formatting.

2025-05-10-16-40-19
- Removed \xan\recs->massageColForEcho and replaced with \xan\module->recCol_StringInline. This makes column values work like other elements with \xan\modules->recColFormattingTags.
- Changed Label html tag from div to span.

2025-05-08-13-27-51
- Updated content-page.php pages to init $recsDetail before the if.
- Added Modules for Tickets and TicketsMessages.

2025-04-29-18-01-29
- Updated xan.js.php to break the JS out into it's own file xan.js.js. Now the JS can be code formatted.

2025-04-29-16-47-33
- Updated xan.js xanMessageDisplay to optionally pass idSet to add an ID to the Message and idRemove to remove and ID. Now shows "Foo..." with an ID Set. Then when the completion time is displayed the ID that was set is removed.
- Updated xan.css --xan-bg-color-active color from Teal to LightCyan. Added --xan-bg-color-message as LightCyan.
- Updated \xan\response constructor to minimize repeated code in the module content-page.php.
- Removed \xan\eleInputsMeta everywhere. Not obsfucating anymore. Added Table Name to each DB Element and passed to doSave.php.
- Renamed FORM_OBFUSCATE_KEY to ENCRYPTION_KEY.
- Renamed FORM_META "Meta" to "meta".
- Updated content-page.php metaSet by adding \xan\module->metaSet function on individual Modules and then calling \xan\response->metaSet.

2025-04-27-12-20-09
- Changed Active Background Color from teal to lightcyan to no longer need to use dark mode colors on text.
- Updated \xan\module->recColRenderAs to include the now removed \xan\module->recColRender.
- Updated Khan and generated CalendarEventsMT.
- Updated Calendar to now be 100% wide so it can auto size.

2025-04-20-17-13-24
- Renamed do-tasks-monthly to do-tasks-weekly.
- Added Calendar Events Auto Update for ModFlag = DEMO Events.

2025-04-20-11-38-46
- Updated module->cardActionsDetail Buttons to be a Print Dropdown and a Database Record Dropdown with Duplicate, Delete, and View Access log.

2025-04-19-17-28-27
- Added Constant for APP_RIGHT_CLICK_DISABLE.
- Added a Response var $contentHeaderEnd for Module Buttons.
- Updated Modules to move Buttons from the First Card to $contentHeaderEnd.

2025-04-19-15-01-26
- Removed eleCard.php float-start. Not needed with d-flex flex-wrap w-100.
- Updated Portal Selectors to be under the index.

2025-04-19-13-19-13
- Updated \xan\module->cardListItemTable so the Selector is under the index.

2025-04-18-17-10-14
- Updated \xan\module->cardListItemTable to move the Selector right.

2025-04-17-14-19-16
- Updated all Module Portals to move the Selector to the end, before the Index.

2025-04-15-16-36-49
- Updated xanAutoLogoutCheck messages to the Console and logout cookie.

2025-04-15-14-03-20
- Added function redirectNow to \aloe\response that uses an http 302 location header.
- Moved \xan\UsersMT->pathLastSet storage from Cookies to text column Users::PathLastModules as json.
- updated \xan\UsersMT->pathLastSet redirect method from window.location.href to http 302
- Replaced the loading.php spinner with a green spinner. Added an optional $_GET[ "redirect" ].
- Updated Bootstrap from 5.3.3 to 5.3.5.
- Updated FontAwesome from 6.5.2 to 6.7.2.

2025-04-03-13-27-09
- Removed Login RememberMe.
- Removed Function isXanWorker.

2025-03-29-17-51-16
- Updated Card Functions from "Foo Ran" to "Ran Foo".

2025-03-29-15-33-14
- Renamed many of the get* functions in module.php for clarity.

2025-03-29-17-00-01
- Renamed recColRenderTypeAs to recColRenderAs.

2025-03-29-17-34-34
- Removed Selectors as Date, DateTime, and Time have selectors follow the input.
- Renamed db* functions to table*.

2025-03-29-16-54-02
- Started to replace the need to pass \xan\response and \xan\recs, but rolled back.

2025-03-28-17-57-52
- Added PHP Constant COLOR_BG_RGB for JS Signature Background.
- Renamed PHP Constant COLOR_ACTIVE_BG to COLOR_BG_ACTIVE to match.
- Updated xan.js.php with PHP Constant Tags like {php:FI_PSOS_CLOUD}.

2025-03-25-16-24-16
- Deleted xan.js.workerSafe.js and xan.js.
- Added xan.js.php which merges PHP Global values into the JS.
- Moved Global Vars, xanDoSave, and JS Helpers into xan.js.php.

2025-03-23-16-08-49
- Added ELE_TYPE_SIGNATURE_DB that saves as a Data URL.
- Moved xanDo, xanDoProgress, and xanDoResponse from page-resp.php to xan.js.

2025-03-16-16-23-01
- Updated \xan\recs and \xan\recsPDO bind types and replaced $sqlIsSelect with $ps->columnCount() > 0.

2025-03-16-14-55-13
- Removed doProgress.php example. Best Example is Schema Update.
- Removed xanDoProgress alert.

2025-03-16-14-32-10
- Looked into replacing xanDo with xanDoProgress.
- Updated native php commands with a leading backslash.
- Updated xanDoProgress to simplify and xanDoProgressMsg by checking for !connection_aborted() in the function.
- Removed old Actions button from Products content-page.php.

2025-03-13-14-35-29
- Big update again. Forgot to Commit!
- Renamed JS functions to prefix with 'xan'.
- Added functions to highlight search terms.
- Added xanDoProgress which is like xanDo but sends progress info back the browser.
- Reworked xanDoSave elements to remove redundant element data.
- Added router.php Rejections of some common path text.
- Added response.php $scriptsElementsA for a common script section.
- Deleted page-resp-jsWorkers.php to fouc on xanDoProgress.
- Updated xanToast to appear at the top in the same space as xanDoProgress.
- Added the beginnings of using search operators in the Module Search.
- Updated logEventToSQL to optionally skip logging UptimeRobot or other Events.
- Updated filesDeleteRecursive with an optional $timestamp param to delete files order than the $timestamp.
- Fixed codeContentAndScripts that was adding prior items again several times due to not resetting array vars in Modules->cardPortal.
- Added function sslCertDateExpires.
- Updated functio strFunctionNameJS to add an underscore like: fn_1234.
- Updated do-tasks-weekly-logDumpSQL.php to handle large record sets.
- Updated do-backup.php to backup PATH_ROOT_XANAPP instead of only PATH_ROOT_APP.

2025-02-11-14-42-14
- Renamed and Reordered Card functions for clarity.

2025-02-11-15-23-21
- Added Card Expand Buttons to All Cards.

2025-02-06-16-06-16
- Updated eleCard to make List and Regular card styles as similar as possible. Both now have the same params and param order. Both now have $contentHeader2 and $contentFooter.
- Removed Portal Cards Header Records Page Nav with a Footer Records Page Button Group.
- Replace all SQL Count(8) with Count(*) since it makes no real difference.
- Fixed a bug in eleSelect. The Selected Item now compares as a string.

2025-01-28-13-25-02
- Updated Contacts Cards.

2025-01-25-16-51-19
- Fixed page-resp.php pageContentColumnsFixedHandler(). Now checks to see if fixedColumn exists before trying to Toggle.

2025-01-25-14-39-01
- Removed eleSearchBarListDB.php and eleSearchBarSimpleDB.php.
- Replaced QueryBuilder with a single field search plus a select to choose All fields or a specific field from \xan\modules->SearchTablesA.
- Removed schema isIndexFullText for now. Reverted to using LIKE which is fast enough, for now.
- Updated page-resp.php to use CSS vars to track the height of the nav and Header to place the pageContentColumns correctly.
  Updated page-resp.php to have a left column for lists \xan\response var $contentLeftA was added. If the array has no elements, the left column and button to toggle are not displayed.
- Added a body background color to make the page be less bright.
- Added Module vars for the new search: SearchTerm, SearchSort, SearchFilter, SearchWhere, SearchBindValuesA.
- Updated eleSelect to support Disabled and Checked.
- Updated eleCard to have min-width and min-height so they cannot be undersized.

2025-01-14-16-03-23
- Renamed the page-resp.php backup to page-resp-jsWorkers.php for future use.
- Added code and classes for Web Awesome.
- Removed code and classes for Web Awesome. It's nice but not a huge benefit over Bootstrap.
- Updated xan.php to have an eleHash function used for Web Awesome Ajax Save.
- Updated \xan\xan->schemaUpdate() and added properties for isFindable and isIndexFullText.

2024-11-23-17-59-58
- Updated ALM Pages. Still more to do.

2024-11-23-15-58-15
- Removed Fields for Gallons and R12.

2024-11-23-15-39-54
- Updated ALM Cards and Portals.
- Updated ALM Import to Delete Addresses From Comms and Blank Addresses aka Non Addresses from Addresses.

2024-11-21-15-21-52
- Cleaned more Cards and Portals.
- Updated eleCard->renderCardWithDiv to support passing the Paged Records Buttons.

2024-11-17-17-04-13
- Updated functions-importALM.php function fmValuesToJoinTables to be easier to understand and validate the join table.

2024-11-17-13-17-24
- Added Users field EmailSendMethod with Select values SMTP, MailTo.
- Moved Constants for Selects to /xan/constants-arrays.php for once place to define the Arrays including query based.
- Addex Settings Companies back to the Admin menu.

2024-11-16-15-47-34
- Added Payments content-page.php.
- Fixed \xan\recs->query by looking for "SELECT" from "Word 1" to "Left 6".
- Removed \xan\module->dbTriggersSQL to spell out the Triggers instead.
- Cleaned up the \xan\module->dbTriggersInstall function.

2024-11-08-18-25-39
- Updated xanDo and xanSave reverted to regular AJAX. Removed Workers, but kept xan.js.worderSafe.js.
- Updated xanDoProgress for Schema Update, Triggers Update, and Massage Update.

2024-11-04-11-37-15
- Removed CalendarTagsJoinMT. Also removed from functions-importALM.php.
- Updated CalendarM and CalendarEvents to use UUIDCalendarTags. Deleted Category column.
- Updated Calendar Edit Event replacing the Category and All Day Text inputs to Drop Downs.

2024-11-03-11-35-37
- Removed qodana.yam from git.

2024-11-02-17-42-36
- Updated functions-importALM.php from functions to a class.
- Renamed Xan_LabsM preventTimeout to preventTimeoutProgressBar.
- Updated Xan_LabsM preventTimeoutProgressBar to no longer add each progress percentage to the console.log.
- Added a constant ELE_WIDTH_DROPDOWN_YES_NO = '2.7rem'.
- Updated ALM FMValues for Comms and Addresses. Used ELE_WIDTH_DROPDOWN_YES_NO. Added Addresses fields for TypeIsBill, TypeIsMail, TypeIsShip.

2024-10-31-14-11-29
- Added a Prevent Timeout example in Xan-LabsM.
- Added a .monospace class to xan.css for a text based progress bar in PRevent Timeout.
- Fixed HomeM and Xan_LabsM Validation.
- Added a function to calculate Pi, for fun.
- Fixed a bug in functions-importALM.php by converting displaying progress in a $table to $resultA.

2024-10-24-18-17-58
- Added functions-importALM.php function fmValuesToJoinTables which creates Xan Join Tables from FM Multi Keys.
- Updated formatting on HomeM->class function cardHome.

2024-10-23-17-58-27
- Replaced calls to \xan\recsGetPDO with \xan\recsGetSQL for most usages with existing Modules so the results use \xan\recs instead of \xan\recsPDO.

2024-10-22-18-10-55
- Renamed recsGet to recsGetPDO.
- Renamed recsGetRelated to recsGetModule. Updated to use \xan\recs instead of \xan\resPDO and to optionally pass $queryColName.
- Updated each \xan\module->getContentImage to accept an optional UUID instead of \xan\recs.
- Updated ContactsMT and ALM_ArtistsMT to share the same getContentTextBrief and getContentImage.

2024-10-18-09-19-42
- Fixed the Photos Uploading in Contacts and Users.
- Fixed the Upload Alert by commenting it out.
- Updated recsGet Function to require BindValues.

2024-10-17-16-26-45
- Updated to have Join Tables for ArtTags, ContactTags, and CalendarTags.
- Updated a few Cards and Portals.
- Moved and Renamed Module Class Files. Example: /xanApp/app/ContactsMT.php is now /xanApp/app/ContactsMT/class.php. This reduces the items in /xanApp/app/ by half.

2024-10-14-13-41-19
- Updated Stripe from v7 to v16.
- Reverted adding Bucket and Pickers within Render. Update Schema will set the Element Types to ELE_TYPE_FILE_BUCKET_DB and ELE_TYPE_PICKER_DB and Generator will use the expected code.

2024-10-12-17-41-23
- Renamed 'Examples' to Xan_Labs.

2024-10-12-17-41-23
- Renamed SettingsExamples to Xan_Labs.
- Renamed Server-404 to Server_404.

2024-10-12-15-56-49
- Updated Khan Class genModule function to automatically use Pickers for 'UUID*' cols and Buckets for '*FN' cols.
- Updated Khan Card with an option for "DeleteKhanBU" to delete older versions of the Module.

2024-10-12-14-00-58
- Misc Cleaning

2024-10-11-15-26-05
- Replaced ALM to use ALM_Artists and ALM_Licensees instead of Contacts just like ALM FM. ALM Modules and Tables now prefixed with "ALM_". Import Tables are now prefixed with "zzImport_ALM_".

2024-09-29-16-29-18
- Added ArtMT's Photo to be the First Related Documents Image.
- Added init.php function appIsActive to check if a App is active.
- Added ArtMT and CollectionsMT Pickers to Documents Related Card. Will show if the App ALM is Active.

2024-09-29-15-44-37
- Added DocumentsMT Image Preview.
- Updated Module Search Term CSS Font Color to go with the Background from color-bg-Yellow to color-bg-text-Yellow.

2024-09-29-15-14-39
- Fixed \xan\eleTimeDB Time Selector.

2024-09-29-14-47-26
- Replaced \xan\module->getEleMeta with new \xan\eleMeta() and removed \xan\module->getEleMeta.
- Renamed \xan\module->getEleMetaRender` to \xan\module->getEleRender.

2024-09-27-17-16-48
- Added $resp->jsAlert to alert when trying to run \xan\PaymentsMT::inst()->recSaveAfter. Will fix during testing.

2024-09-26-17-18-49
- Added $resp->jsAlert to alert when trying to run paymentApprove or paymentDisuburse. Will fix during testing.

2024-09-26-16-05-32
- Looked over the SalesMT and SalesItemsMT do files. Uncommented to test with the rest of the Modules.

2024-09-26-15-33-08
- Fixed router.php path.
- Moved code from SalesItemsMT.php recSaveBefore to recMassage. Removed the now optional recSaveBefore.

2024-09-21-16-41-25
- Updated \xan\module to make record event functions optional rather than just deleting them. Converted recSaveBefore, recNewBefore, recNewAfter, recDuplicateBefore, recDuplicateAfter, recDeleteBefore, recDeleteAfter to be PHP Traits. Those are generally covered by the existing function dbTriggersInstall and recMassage.
- Fixed a bug in /xan/router.php to not load routs where URL Component 1 does not exist.

2024-09-17-15-37-39
- Updated Modules functions dbTriggersInstall and recMassage to be able to ato massage column values on the fly.
- Moved code from onRecsInsertBefore to recMassage.
- Added calls to recMassage into doSave, module->dbMassageAll, recs->recordInsert, and recs->recordUpdate.
- Renamed arrayContainsValue to arrayValueFound and added arrayValueNotFound.
- In do-triggers-update.php, updated to auto loop thru each Module instance to run module->dbTriggersInstall and module->dbMassageAll.

2024-09-05-15-44-38
- Renamed Module StatsMT to StatsM.
- Updated Nav and User Menu to use ModulesD using added function modulesAppWhere.
- Updated all Portals to only be included if included in APP_ACTIVE array.
- Added function moduleIsActive to optionally include non-portal elements based on ModulesD.

2024-09-03-12-04-46
- Added \xan\xan.php functions to cache Modules like Schema.
- Updated functions-misc.php function recsGet to not use the \xan\recs, but similar to make SQL calls before the class is loaded.
- Updated app/SettingsMT/do-backup email to add returns after semicolons to make it easier to read.

2024-09-01-15-39-44
- Added Tables and Modules for ALM.
- Updated Modules cardPortal Function to use If Else. Was using an If for each related table, now uses the Default.
- Updated /router.php to use the First Component as the basis for the sub router.php path. Currently works for the page and do like /contacts/ and /contacts-do/.
- Lots of other bug fixes.

2024-07-27-17-28-55
- Updated eleFileBuckets to allow for one file or many files to be uploaded. Both files upload to the Bucket but only the first file is represented in the database.

2024-07-25-17-45-18
- Updated eleFileBuckets to finish cleaning up.

2024-07-25-16-53-16
- Updated eleFileBuckets to used shared common functions to reduce code duplication on the page.

2024-07-25-15-02-55
- Updated eleFileBuckets to prep for common functions.

2024-07-25-14-48-31
- Updated eleFileBuckets to prep for common functions.

2024-07-24-17-29-12
- Updated Documents List to not show an Image.
- Moved \xan\eleFileBucket javascript function in renderButtonView() to page-resp.php.
- Updated \xan\eleFileBucket to see if a BucketType was already set and checked for URL_ROOT_IMAGES_PLACEHOLDER path first.
- Updated \xan\response jsCallFunction function and xan.js to work with 0 to 9 parameters.
- Updated \xan\module->recCol_BucketEle to remove php styling so js can style. Moved from $code var to a HEREDOC.

2024-07-21-11-34-34
- Updated \xan\module->recCol_ functions to pass \xan\response to make adding scripts easier.
- Updated \xan\recs->queryModule function to no longer need passing \xan\response.
- Updated \xan\dateTimeStrFromString to optionally pass a time offset.
- Added \xan\eleGetID function to replace \xan\module->getEleID.
- Updated page-resp.php to strip html tags from the Page Title.

2024-07-07-17-52-29
- NEED TO FINISH eleFileBucketDB.php to make resizing not hard coded.
- Updated \xan\module organizaion and renamed a few functions.

2024-07-06-17-57-54
- Updated Documents Bucket to show Images, PDFs, and other files. If in a Card, it can be rsized.

2024-06-29-16-31-53
- Updated xanDoSave to use Javascript Workers for the Save Process.
- Updated each Modules \xan\module->recSaveAfter to strip BRs from the header. Uses \xan\module->getContentTextBrief_Header.

2024-06-29-13-21-50
- Updated /login, /passwordreset, /register to not check to see if it's a call from a Worker.

2024-06-27-17-23-41
2024-06-27-17-23-41
- Updated xanDo New Window code to Alert to allow Popup Windows.
- Updated and Renamed some xanDo params.var names. It's a mix of first letter uppercase and lowercase. Goal is camelCase.
- Updated \aloe\response so the header 'Peak' is now 'peak';

2024-06-27-15-42-42
- xanDo now passes the xanID as doID hashed and then validated.
- Updated \xan\peakMemoryUsageGet() to no longer pass a label.
- Updated \aloe\response to set a Response Header for "Peak" the Peak Memory Usage.
- Updated \aloe\session to set a Session SESS_XANID.

2024-06-27-12-15-37
- Updated xanDo to use JS Workers.
- Updated Stats to use a JS Worker to load the Access Log Stats.

2024-06-24-17-55-03
- Updated Stats to not show the Access Log Stats by default with an ugly Show / Hide Button.
- Updated Notes in Khan for clarity.

2024-06-23-16-12-22
- Updated all Portals and Cards with Notes to use a \xan\module->cardExpandButton function for the Expand Button.
- Updated \xan\module->recCol_Note, removing the Card Height Parameter. Now set to 100% Height.
- Updated Khan to generate a Documents Module.
- Updated xan.js to now be two files ( xan.js and xan.js.workerSafe.js ) to separate functions that can be used in Workers.
- Updated AutoLogout to use a JS Worker to watch the Current Time for lapses in Time which indicates the Connection was Lost.

2024-06-18-15-07-23
- Updated FontAwesome from 6.5.1 to 6.5.2.

2024-06-18-14-55-48
- Fixed Modules with missing functions.
- Updated Routers to no longer change the Session ID on each reload except for login and change password.
- Added jsConsoleLog function in \xan\response.
- Separated Stats from Settings as loading Stats is slow.
- Renamed ELE_TYPE_FILE_BUCKET_IMAGE_DB to ELE_TYPE_FILE_BUCKET_DB.
- Updated the eleFileBucketDB to load files using the embed tag for files that can be displayed, otherwise a file icon.

2024-05-04-15-41-36
- Decided to reenable right click prevention.
- Fixed the \xan\module\getListCard class name for the selected records.

2024-04-30-17-52-35
- Fixed the Password Strength Meter on /register, User Menu Change Password, and /users Replace Password Button.

2024-04-30-16-23-52
- Disabled the User Registration page and do.

2024-04-30-16-08-51
- Fixed Picker constant Parameter PICKER_SHOW_GO_BUTTON postion and added PICKER_DATA_AS_GO_BUTTON.

2024-04-30-14-18-44
- Updated modules->cardActionsDetail and modules->cardActionsList to return a string rather than as a value in $resp->extrasD.
- Updated \xan\respAToString to include \n instead of \n\r to remove the double "returns".

2024-04-25-16-03-54
- Moved the functions cardActionsList and cardActionsDetail from individual modules to module.php.
- Added in AccessPermissionsMT.php a cardActionsModal that adds itself using module->cardActionsList.
- Added in functions-dataMassage.php functions arrayCount( array $arrayA ): int and arrayInsert( array $arrayA, int $index, mixed $value ): array.
- Replaced in xan.js the functions xanActionInitList and xanActionInitDetail with xanActionsModalShow.

2024-04-16-16-39-37
- Updated \xan\UsersMT::inst()->pathLastSet to redirect to the last path set.

2024-04-13-17-42-38
- Moved /include/ to https://xanweb.app/xanApp/include/ to be shared between Xanadu Web Apps.
- Deleted /include/. Will need to create another GitHub Project.

2024-04-11-16-23-30
- Added Access Roles and Permissions. Users can be included in many Roles.
- Update eleCard to pass $cardHeaderContentRight for buttons so that the Left side wraps around the buttons.
- Updated Settings and Users Cards to consolidate.
- Updated User Menu to now have User related items and moved Dev items to a Dev Menu.
- Added xan.php function hasAccess( $permName, $UUIDUsers = '' ):bool.
- Updated module.php function getPicker to pass $whereFilterD = [] to be able to pick related records like Dependents.

2024-04-02-18-00-19
- Added Notes from last update.
- Updated QueryBuilder from 2.5.2 to 3.0.0.
- Updated SQL-Parser from 1.3.0 to 1.2.3. Yes, but it was the latest.
- Updated eleSearchBarListDB.php to convert US Dates, Times, and DateTimes to SQL Formats. Allows for user searches in US formats.

2024-03-31-14-13-58
- Added Users Replace Passwords require_once includes for the missing modal.
- Added require_once to UsersMT/do.php: UsersPasswordChange, UsersPasswordReplace, UsersSetPhoneSMSEmail, UsersTBOTPSecretReplace.
- Added Settings Card for Access Log Stats.

2024-03-26-15-33-58
- Updated Home cardHome to use a table.
- Disabled page-resp.php xanDo passing of PHPSTORM debug parameter.

2024-03-23-15-24-50
- Updated xanApp/templates/pdf-default footer files and footers defined in do-print.php files to pass what is in the footer instead of defaults for Printed Date and Page Number.

2024-03-23-14-30-22
- Renamed \xan\recs->massageColForGUI to massageColForEcho
- Removed Constant HTM_BR2.
- Updated Constant HTM_HR to have a height of 1px.
- Added Constant HTM_HR with a height of 2px.
- Updated SettingsMT/do-backup.php to keep 10 backups instead of 20 for disk space savings. Backups should be backed up to another location.
- Updated SettingsMT/do-tasksmonthly_logDumpSQL/php to now save to PATH_ROOT_LOGS instead of PATH_ROOT_BACKUPS as Backups now only keeps the newest 10 files.
- Updated xanApp/templates/pdf-default header and footer files. Using hr height of 2px to separate the header and footer clearly.
- Added functions-dataMassage.php function function strEncodeHTMLEntities so header special char are safe.
- Changed ini_set for error_log so logs filename dates are YYYYMM instead of YYYYMMDD. Daily was create a lot of log files.

2024-03-14-14-31-16
- Updated Khan so only the first detail Card has the Actions Detail.
- Updated Khan to only include the first three columns in QueryOrderBy.
- Updated Contacts getContentTextBrief to use HTML BR to make Lists easier to read.

2024-03-14-13-55-45
- Updated \xan\recs->recordSelect to optionally pass $tableKeyName.
- Removed Nav link to SettingsCompanies since there is portal in Settings.
- Fixed functions-misc.php function dbQueryOrderBy_DropdownItem so dropdown-item text can wrap.
- Removed Settings Phone, Email, Address, Twitter Site/Author.
- Updated constants-and-settings.php to get the Phone, Email, Address, Twitter from the SelectedSettingsCompanies.

2024-03-10-16-44-57
- Updated \xan\Modules getContentText functions to add an options to pass a UUID instead of a \xan\recs.

2024-03-10-14-24-26
- Renamed recsSimple to recsGet.
- Fixed a xan.js so xanScrollToElementInDiv che

2024-03-03-13-54-25
- Changed Portals to use GTRR instead of a Picker.
- Added Logging of PHP Peak Memory Usage in index.php.
- Added Display of PHP Peak Memory Usage to Page Load Time

2024-02-29-15-00-52
- Added Pagination in Portals.

2024-02-17-17-57-20
- Fixed Expand Card for Contacts > Comms.
- Updated Expand Card so the card expands by 50% in width and height in the center of the window.
- Added a Modules > getCardID and ModulesMini > getCardID function to get a consistent name.
- Updated Modules to use the getCardID function.

2024-02-17-14-39-30
- Updated most cards to now have a calculated $cardID with a random at the end.
- Removed the extra New Buttons from Addresses Portal and Comms Portal.
- Removed the extra Modals for New, Dup, Del.

2024-02-16-10-54-35
- Fixed Nav Bar Icons by changing from a Button to just an Icon.
- Updated .btn .fas to 20px.
- Updated Button Gray from WhiteSmoke to Gainsboro to stand out a bit more.
- Updated Button FI size from 2.5rem to 2.0rem.
- Renamed PORTAL_INDEX_WIDTH to INDEX_WIDTH.

2024-02-15-19-10-18
- Updated eleDate, eleDateTime, eleTime.

2024-02-15-17-34-30
- Updated xanDoSave javascript with a semaphore to not save the same table::column and same value rapidly when there are duplicates of the same table::column on the page.
- Updated eleDateDB.php to include the Selector ID as a Class to make resetting when more than one for the same table::column are on the same page.

2024-02-15-12-39-18
- Removed TAGS_ELE_BUTTON_ICON_PORTAL and replaced with TAGS_ELE_BUTTON_ICON to simplify as the size diff was negligable.
- Updated eleDateDB.php to pair the Input and Selector instead of separate. Need to update Time and DateTime.
- Updated element.php to apply the ID also as a Class to make updating an Input with multiple instances.
- Updated xan.js xanEleFlatpickrSetFromString and xanEleFlatpickrSetFromSelect functions to set the value for updating an Input with multiple instances.

2024-02-13-13-22-11
- Refactored Buttons and Colors. No longer using Bootstrap Sizes (SM, RG) and Colors (Primary and Secondary). Now using HTML Named Colors. Goal it to use the same size everywhere with the exception of font size.
- Updated Detail Card Alignment to use TAGS_CELL_RTB and TAGS_CELL_LT.
- Updated z-index for several elements.

2024-02-04-18-37-39
- Updated Portal Cards to no longer have Buttons for Duplicate or Delete. Now part of the Selector Checkboxes and Dropdown Action Button.
- Added a Portal Cards Expand Button that changes the Card from Float Left to Absolute floating above.
- Updated Button Classes to be rounded.
- Updated Modules Content Pages to now have separate Actions for List and Detail. Detail Actions show on the Main Card.
- Moved Modules Content Pages Actions to the Modules Class.
- Moved Modules Content Pages Modals for Duplicate and Delete to the Modules Class.
- Updated eleCard to have a Margin Bottom of 2 to provide more space for the Card Resizer.
- Added Jquery UI to Includes to support Draggable Cards.

2024-01-25-16-23-42
- Updated Modules recNew, recDup, and recDel with an option to Go To the Page on Portals for tables like Contact, but not for tables like SalesItems.
- Updated ELE_CLASS_BUTTON's to remove 'border' as 'border-2' was already added.
- Added User Link Portal on Home.
- Renamed Links UseCount to Visits.
- Updated eleModal to fix the alignment of the Action and Cancel buttons.
- Updated function colValueMassageForGUI to not evaluate a date, time, or datetime if empty. Empty dates were displaying as 1/1/1970.
- Added functions-internet.php function urlHref to make creating links easier.
- Updated module functions getButtonGTRR, getPicker and getPickerContent to fix confusion with the Picker Key ( For the Picker Element ) and Selected Key ( For the Key Selected in the Column.
- Added router.php routes for PlansItems and PurchasesItems.

2024-01-21-15-35-23
- Renamed $elementRendered and $labelRendered to $colCode for cleaner code. Goal is to make Cards and Portals code similar.
- Added /xan/cmdCheck.sh and cmdDo.sh as a way to run shell script. Just create a file in /xan/cmdDoPermissions.do. The script will run when the file is seen, auto delete the do file, update permissions, then log the action.
- Added in Settings a cmdDo Log Card. Shows the current PID, the command to stop, and the most recent 50 log rows.
- Added function fileReadReverse( $path, $rowCount ). Reads a file returning the last $rowCount in reverse order with the last line first.
- Updated Khan and recreated Plans and Purchases to test. Also updated Disbursements, SettingsCompanies, and Users. Removed old Card and Portal files after moving to their respective Module files.
- Updated Auto Logout to write to the console showing the Event and document.visibilityState.
- Added Contants: CARD_WIDTH_0125, FI_CMD, and FI_FILE_TEXT.
- Updated eleTable cellSet so $colSpan is before $rowSpan since col span is used more.
- Added Modules function setURLs() to set the four URL values using the Module Name: "Contacts" becomes "/contacts/".
- Updated page-resp.php by wrapping the Resizeable Observer javascript in a PHP if instead of a JS if. It now does not appear on the Browser Source.

2024-01-15-16-10-19
- Updated Modules recNew to check for $relatedNameKey and $relatedKey.
- Replaced $xanDoNew, $xanDoDup, $xanDoDel with inline strings.
- Replaced JS var names "window.RecDup_UUID" and "window.RecDel_UUID" with "window.recID".
- Updated xan.js to now use the Hand Cursor on the Action Menu Items.

2024-01-15-14-24-07
- Renamed Modules NameTableKey to NameKey.
- Replaced Modules NameTableParam with NameTable.
- Replaced Modules URL setting with a Function.
- Replaced Disbursements module with Khan Generated version.
- Renamed STR_NBSP to HTM_NBSP.
- Added Xdebug Info page.
- Added PHPStorm Xdebug content.
- Changed URL for SettingsCompaniesMT.php from settings-companies to settingscompanies.
- Updated Router to Redirect to /logout/ if not logged in during xanDoSave.
- Updated each Module instance to set the Related Key if set rather than checking for a Related Module name.
- Updated ProjectsTasks to set the ProjectsItems Related Key instead of the Project Key.

2024-01-07-17-51-09
- More cleanup.
- Renamed app folders and classes from "ContactsMT" to "ContactsMT".

2024-01-02-15-29-18
- Fixed Address Zip Lookup, Address Standardize, and Address Correct filenames as they did not match the router.
- Fixed Contacts Print to Word. Was missing some table tags.

2024-01-02-14-12-47
- UPDATING PORTALS is now considered complete. There are a few exceptions for now like Xan_Labs and users.
- Updated jQuery to 3.7.1.
- Updated by renaming from "mmContactsT" to "ContactsMT". Moved all Modules from "modules" to "app". Non Table Modules like "mmHome" is now "homeM".
- Renamed the folders to the same as the Modules.
- Updated Router to use the correct folders. Did not change the URL Component 1 like "contacts" which now routes to ContactsMT.php.

2023-12-31-16-59-50
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated FontAwesome Free version to 6.5.1.
- Updated Recs, Portals, and Module List New to have a specific Modal name like 'RecDupContacts' but all use Action names like RecNew, RecDup, or RecDel.
- Updated Routers with shared 'do.php' files for related tables to now use their own folders with their own do.php and router.php files.
- Moved API files to the APIRequests folder.
- Renamed all printing files to be "do-print.php". Additional printing files can be called "do-print-foo.php".

2023-12-30-14-20-16
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Changed SettingsCompanies Icon to be fa-bell-concierge.
- Added a class moduleMini that is like module, but minimal.
- Updated mmHome and mmCalendar, mmCheckout to no longer extend as a module but as a moduleMini. Kept since the are substantial. Didn't add back UsersLogin, UsersLogout, UsersPasswordReset, UsersRegister, or Xan_Labs since they are minimally accessed.
- Updated mmHome and mmCalendar by moving the Card to their moduleMini file.

2023-12-29-17-36-41
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated each router file require_once statements to use relative paths.

2023-12-29-17-24-14
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Renamed ContactsAddresses to Addresses.
- Renamed ContactsCommsto Comms.

2023-12-29-16-00-52
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated all $aloe_response->content_set( require_once( PATH_PAGE_RESP ) ); to use require.
- Renamed urlShortener to linkShortener.
- Moved "Link Shortener" form form Home to the Menu Dropdown.
- Added a php function getEleID to return a database input ID.
- Renamed Link Shortener New from "lNew" to "linkNew". Go to link "l" remains the same.
- Updated Javascript "arrow functions" to use "function" for simplicity.

2023-12-28-17-49-10
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Removed Module xan_labs since it's not really a Module.

2023-12-28-16-56-43
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Removed Modules: UsersLogin, UsersLogout, UsersPasswordReset, UsersRegister, ServerStats
- Moved Folders for UsersLogin, UsersLogout, UsersPasswordReset, UsersRegister folders to app/users/logins as login, logout, passwordreset, register.
- Updated app/users/logins Pages and do Files to no longer rely on a Module as they don't actually have a Module but are parts of Users.

2023-12-27-14-13-19
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Added router.php files for each Module and the main router.php to mostly use a switch by component 1 character 1 rather than many, many ifs.
- Replaced the File Browser as the prior library would not work in PHP 8. Needed to download the include files and fix the FontAwesome Icon Names.
- Updated \xan\fontIcon calls in each modules Action Menu to be wrapped in \xan\fontIconButton so each is the same width.
- Updated do-record-print.php pages to use NameSignular for the Page Title and Doc Title.

2023-12-24-17-53-01
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Added TODO: Settings Example IMAP was not connecting. Added a note.
- Added TODO: Settings Example Stripe was not working. Needs to be updsted to PHP 8.2.
- Removed the Includes for EDI X11.
- Removed the Exception Handler in the Xan Class Autoloader. It was preventing the AWS Textractor from performing its Autoloader.
- Moved the DB Compare code from Home to Settings Examples.
- Updated calls to \xan\sendSMSDebug to \xan\sendEmailDebug.

2023-12-21-18-04-27
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated urlShortener "URLs" Table Name to be "Links".
- Updated Router so the Links API calls could be saved in app/links as a second router file. Added at the top of router.php for speed.

2023-12-21-17-16-01
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated page-resp.php Menus placing Logout at the end.

2023-12-21-16-30-57
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated git files that were not pushing. Added special files to ignore.

2023-12-21-16-04-08
- STILL IN THE MIDDLE OF UPDATING PORTALS: Need update other tables Portals to match.
- Updated Settings Inputs to be Reveals.
- Added Schema column InputMode for mobile. Default is none or "decimal" for numbers columns.
- Renamed colMeta to eleMeta.
- Renamed functions.php to constants-and-settings.php.
- Renamed functions-schema.php to functions-eleDB.php.
- Updated xanSchedAutoLogout check interval from 5 min to 1 min. Updated to show its status on load.
- Updated AutoLogout to use the Settings AutoLogoutSeconds. There were two contants with similar names. Removed the one set to one hour and replaced with Settings AutoLogoutSeconds.

2023-12-07-18-39-09
- STILL IN THE MIDDLE OF UPDATING PORTALS: Contacts and Khan are inline. Plan is to keep them in sync. Need update other tables Portals to match.
- Lots and lots of changes to get Khan working based on Contacts Portals.
- Now looking for bugs...

2023-11-14-17-27-46
- STILL IN THE MIDDLE OF UPDATING PORTALS
- Many Modules now have their Cards and Portals defined. Need to update the remaining modules and then replace Khan.

2023-11-09-17-23-08
- STILL IN THE MIDDLE OF UPDATING PORTALS
- Removed GLOBALS in favor of Singleton. $xan and $dbSchema are now accessed via \xan\xan::inst();

2023-11-07-16-08-32
- STILL IN THE MIDDLE OF UPDATING PORTALS
- Refactored Modules to Singleton. Can instantiate anywhere: $mmSalesT = \xan\salesMT::inst();

2023-11-05-14-37-49
- STILL IN THE MIDDLE OF UPDATING PORTALS

2023-09-24-14-47-24
- IN THE MIDDLE OF UPDATING PORTALS.
- Updated Ajax calls for Products Prices.

2023-09-16-18-12-20
- Pickers now have a border like XanControl.

2023-09-16-17-37-45
- Huge updates from PHP 7.4.x for prior commits. Now PHP 8.2.x.

2023-04-20-17-42-45
- Added Setting for the Default UUIDSettingsCompanies.
- Added Settings Constants for several that were missing.
- Added Settings Constant APP_UUID_SETTINGSCOMPANIES to be auto assigned on Sales Records.
- Updated \xan\module Search to Limit to DB_LIMIT.
- Updated \xan\module->QueryOrderByDefault uses of 'Active ASC' to 'Active DESC' so 'Yes' will appear before 'No'.
- Updated the in progress Sales Module.

2023-04-20-15-07-01
- Added xan.js xanDoJS option for triggeringEvents. Using to update a column and save.
- Added xan.php ARRAY_PAYMENTS_FORM Constant.
- Updated xan-do-save.php to get the values before updating and then use to compare to changes.
- Updated all uses of "xf_" to the FORM_PREFIX Constant.
- Renamed \xan\recs->moduleMeta to \xan\recs->module.
- Updated \xan\recs function recordInsert to aut insert the passed rowD, then apply the \xan\module onInsertColValues, then build the SQL statement.
- Added xan-functions-dataMassage.php function strToNum( $text ) which will convert text to a number by filtering non-numeric chars and then cohersing into either an int or float.
- Added xan-module.php getCol functions for Notes FileNameImage, and FileNameLabelWButtons.
- Updated xan-module.php getCol functions Input and Input_Portal to be display: inline-block;
- Updated defined modules to use Font Icon Constants for easy reuse.
- Updated defined modules function onInsertColValues to pass \xan\recs instead of $rowD. The function uses $recs->rowsD.
- Updated defined modules function onSaveColCalcs to use the updated tooltip functions.
- Updated \xan\tags functions tooltipTagsString and tooltipExtraD to add the 'data-bs-trigger' = 'hover' to have tooltips auto hide for Selects and Buttons.
- Updated page-resp.php xanInit Tooltip Init to use jquery and set onMouseLeave to blur to to have tooltips auto hide for Selects and Buttons.

2023-04-15-16-51-59
- Renamed \xan\tagExtraToolTip to \xan\tooltipTagsString. Added \xan\tooltimExtraD.

2023-04-15-14-55-33
- Added IMAP Settings
- Renamed SMTP Settings.
- Added IPStackKey Setting.
- Added IMAP Settings to Users.
- Renamed the SMTP Constants. Removed "_MAILGUN" from the end.
- Fixed a few uses of \xan\eleMeta->eleFormatAs.
- Removed setting of the attributes on eleDB: data-format, data-key, and name. Each was redundant.
- Updated all uses of data-format, data-key, and name.
- Renamed \xan\formTag to \xan\inputsMeta and moved the class to its own file.
- Renamed all uses of $formTag to $inputsMeta.
- Added the function urlEncodeComponent to encode spaces and such in urls.
- Updated xan-imap.php to use the new Users IMAP Settings.
- Removed IMAP and IPSTACK Constants from the init files.

2023-04-13-13-50-30
- Updated \xan\tags to convert extrasA array to extrasD dict. Changed string extras to dict values.
- Updated xan.css .xanControl to include read-only for flatpickr elements.
- Removed tag variables from \xan\eleMeta.
- Updated \xan\recs to have query() and queryModule(). The latter would query and store a reference to the \xan\response and \xan\formTag.

2023-04-02-17-22-41
- Added xan.css style .tooltip to prevent the pointer from changing which stops the flicker.
- Added xan.css styles .xanCheckbox100 to .xanCheckbox300 to scale checkboxes size.
- Updated xan.js and xan-response.php to replace Dict Values with Vars to make it easier to read. Added functions for jsRemove, jsBlink, jsSetValFlatpickerDate, jsSetValFlatpickerDateTime, jsSetValFlatpickerTime, and jsSetScrollTop.
- Added xan.php Constant COLOR_TABLE_HEADER_BG for Headers.
- Updated \xan\fontIcon function to remove unneeded classes.
- Updated \xan\eleTable to fix bug in ColMax where RowGroup and IsSticky values were treated as a Col Value. Now defaults to Col = 0.
- Updated \xan\TAG_CELL functions so $classA, $styleD, and $extrasD can be passed.
- Added /app/home/ Contacts Portal Selection Check Boxes to select one or many contacts. Clicking View will show an Alert of the Contact IDs.
- Added /apps/server-stats contentCard-stats-diskRam.php PHP version to also show the User Name that is running PHP using exec('whoami').
- Updated /app/projects content-portal-projectstasks-table.php to have a floating header for the Title/Desc and a Leading Break on Project Item Title.

2023-03-12-17-27-13
- Removed TAGS_ELE_INPUT_PORTAL default height as it was not needed.
- Added function \xan\cssSizeAdjust( $sizeUnit, $adjAmount ) which does math like 10rem, -2: 8rem; 10rem 2: 12rem.
- Updated \xan\eleTextAraDB to automatically set its height to 100% if there is not a height already set as most cases the TextArea's cell is set to a specific size.
- Updated Contacts Notes, Projects Portal ProjectTasks Table, User Privs.

2023-03-11-16-44-48
- Updated Content Records to now set its $colName rather than repeat the column name text.
- Updated Portal Comment for the Table Index Header.

2023-03-11-14-58-35
- Renamed $tableRowIndex to $rowIndex.
- Updated /apps/projects/content-portal-contacts-table.php as it needed two Row Indexes to build the main table and sub tables: $rowIndex and $rowIndexSub.

2023-03-11-14-07-58
- Renamed \xan\module "getColEleRendered" to "getCol". Added recCol_LabelBlock, recCol_LabelInline, recCol_Input, recCol_Selector, recCol_LabelBlock_Portal, recCol_LabelInline_Portal, recCol_Input_Portal.
- Renamed \xan\tags get helpers TAGS_CELL_LEFT_TOP, TAGS_CELL_LEFT_MIDDLE, etc to TAGS_CELL_LT, TAGS_CELL_LM, etc.

2023-03-08-17-49-06
- Renamed ELE_AS_LABEL to ELE_AS_LABEL_BLOCK and added ELE_AS_LABEL_INLINE to be able to use line-height for Labels.
- Updated all uses of ELE_AS_LABEL to either ELE_AS_LABEL_BLOCK or ELE_AS_LABEL_INLINE. Portal Tables tend to use ELE_AS_LABEL_INLINE.

2023-03-02-17-35-59
- Removed the Menu Item to "Reset Page Card Sizes".
- Updated Portal Tables from TAGS_DIV to TAGS_CELL_ and set to be either thead or tbody.

2023-02-28-22-06-13
- Updated Portal Ajax in Comms on Khan's zzTableTemplate Portal.
- Now uses the CardID so Grid and Table versions can both work at the same time.

2023-02-28-16-16-22
- Added functions to xan.js: xanFadeOut, xanFadeIn, xanFadeOutAndIn.
- Added functions to response.php: xanFadeOut, xanFadeIn, xanFadeOutAndIn, and jsSetScrollTop.
- Renamed response.php function "jsOnLoadSelectorFocus" to "jsSetFocus_OnLoad".
- Added in xan-element-card.php an optional parameter $contentBodyEnd in renderCardWithDiv.
- Updated /app/contacts/ files so Comms Grid New, Delete, and Duplicate replace the Card Body Contents and update the record count in Card Body Header.

2023-02-23-17-42-26
- Added a xan.js XanToggleDisplay object parameter to be able to access the ele.style.display back to the calling function.
- Updated app/contacts/do.php to add do-contactscommms-urlGet.php back in. Found that the Comms url buttons were not working. Like lost it when generating Contacts module via Khan.

2023-02-20-10-41-08
- Removed DataTables includes. Now using tableDnD and TableFilter.
- Renamed \xan\response js action 'setFocus' to 'setFocusOnReturn'.
- Disabled Resizeable Observer automatic Card resizing as the behavior is off. Planning to add back in the future where the user chooses to save Card default sizes.
- Updated /app/sales/content-portal-salesitems-table.php Card to be wider.
- Updated Portals to init the \xan\formTag before loops as some comments needed to access the values.
- Updated Contacts Cards to be taller via $resp->cardHeight.

2023-02-19-14-58-28
- Updated \xan\eleTable to add a $tableStyleWidthMax setable via the Constructor. Defaults to 99%.
- Added a Contacts Card for 'Associations'. Removed two columns on 'Associations' from 'Other'.

2023-02-19-13-27-59
- Updated use of \xan\module->getColEleRender[ed] and getPicker, module instances, record cards, and portal cards to remove the params \xan\recs $recs, \xan\formTag $inputsMeta, \xan\response $resp to reduce duplication as they can be passed using the set Functions.
- Removed \xan\module->getColEleRenderLabel, getColEleRenderInput, getColLabel, getColLableEle replaced with the longer functions as they were not used in many instances.
- Added xanDo js function to add commpent with ideass for swapping elements on returning the response.
- In app/contacts/content-record-contacts.php, experimented by adding labels and inputs in a loop of a column name array.

2023-01-26-18-28-12
- Removed eleTable DataTables which were a bit complicated due to working with data and rendered.
- Added eleTable TableFilter and TableDnD to replaced DataTables functionality.
- Updated eleTable->rowSet to pass an ID for the row.
- Updated eleLabel from using div to span so eleTable TableFilter can place the sort indicator properly.
- Added Contants for INDEX_WIDTH, ZINDEX_THEAD_TFOOT, TOOLTIP_TABLE_FILTER.
- Added xan.js xanScrollTo, xanToggleDisplay, and xanToggleVisible.
- Added xan.css trdrag, nodrag, nodrop.

2023-01-05-16-23-17
- Added function numDisplayCurrency( $num, $dec = 2, $currencySymbol = APP_CURRENCY ).
- Added Total Sums to Portals: Sales, Purchases, SalesItems.
- Modified from using Grids to Tables for the most part. Grids tend to create tall content but stack data nicely.
- Modifed Home to use Tables for Projects, Sales, and Purchases.

2023-01-05-12-39-46
- Updated \xan\eleTable to set cell 0, 0 to "" to avoid error when no cells are set.
- Removed queries on zzTemplate on content-portal-related.
- Updated Contacts Projects and Sales to show as a portal. Added a Picker as a GTRR.

2023-01-04-19-06-06
- Updated Projects by generating using Khan, then moved card contents.

2023-01-03-18-51-19
- Renamed function \xan\arrayContainsString to \xan\arrayContainsValue.
- Added first version of Module onInsertColValues. Needs testing.

2023-01-03-14-24-30
- Renamed xan files to remove "adu" from the filename. Also renamed "fns" to "functions".

2023-01-03-14-07-25
- Added \xan\module variable $FocusColName. Added in each module and in each do file.

2023-01-02-17-16-38
- Added a quote parameter to function tagExtraTooltip.
- Added \xan\response "jsSelectorTriggerChange_OnLoad" to trigger a change on an array of selectors via a php session array.
- Renamed \xan\response function name from "jsSetFocusOnPageLoad" to "jsSetFocus_OnLoad".

2023-01-02-13-19-22
- Added \xan\module->getPortalCard to separate it from getListCard. There were enough differences that it should be its own function.
- Updated each \xan\module->getContentTextBrief to return '[ New ' . $this->nameSingular . ' ]'. No longer need to set a column value to show in Lists.
- Updated each app/module do-record-new and do-portal-new/dup/del files to support passing $doParam[ 'ColVals' ].

2022-12-31-15-42-26
- Fixed Portal Delete Buttons from $xanDoDelete to $xanDoDel.

2022-12-31-13-37-41
- Updated Contacts and Sales to work like the Khan changes.
- Updated each \xan\module->onSaveJSActions to add an underscore before "Label".

2022-12-31-13-37-41
- Updated Products, Purchases, SettingsCompanies, Vendors to work like the Khan changes.

2022-12-30-16-05-05
- Khan ran for Contacts, Products, Sales, Purchases, SettingsCompanies, Vendors. Made the Kan Module the default for all but Contacts and Sales.

2022-12-29-16-24-07
- Updated Khan. Renamed files and updated code to make records vs portals clear.
- Updated \xan\filenameClean to have a default but overridable space char set to " ".

2022-12-29-13-52-43
- Updated Khan with new module file names.
- Updated \xan\filenameClean to remove "#" and replace "",-" with ",".

2022-12-28-11-02-50
- Updated Products ProductsPricing Portal so it can be used on Products and Contacts.
- Updated Khan to optionally include a Portal for the Module Table for ease of adding to other modules.
- Updated Khan to add a suffix "khan" to prevent overwriting existing modules. Module folders are suffixed and Module files are prefixed.
- Updated Khan Portals and do-New/Dup/Del so they can be used on other Modules.

2022-12-26-17-51-27
- Modified Contacts Pinned Icon. Moved from getContentTextBrief to getContentList Text.
- Modified Card Header font-size from default to "larger".

2022-12-26-17-24-15
- Modified Card File Names to begin with "z-" for unused cards. Removed the commented out uses.
- Modified Primary Card require_once to use the lower case table name rather than a calcuated name.

2022-12-26-16-34-25
- Added \xan\module->getColLabelEle to return a Label with Alignment.
- Removed \xan\eleLabel Render parameter $isPortal as the tags are now passed.
- Updated each card with the five line code for labels down to two lines by calling \xan\module->getColLabelEle.

2022-12-22-17-49-08
- Found a bug in js xanResizeableSave. Card width would get narrow. Found that each reload would take 10px off the width. Fixed by no longer using ResizeObserver entry various width and height and replaced using jquery width and height which is used to set the values.

2022-12-22-16-13-26
- Removed New Record Modal from each content-page.php since the List Card includes the Modal definition.
- Changed all uses of "= /** @lang JavaScript */" to use "/** @lang JavaScript */ = " so the code will be on the same line.

2022-12-22-14-27-09
- Updated Contacts with a Pinned = Yes/No column.
- Updated the sort on Contacts List and Home Recent Contacts so Pinned Contacts appear at the top.
- Updated mmContactT.php onSaveColCalcs to automatically set blank or null values for Active and Pinned columns to 'No'.

2022-12-20-17-53-30
- Added \xan\Module\getListCard to create a Card List with Search as a function.
- Updated Each List Card with \xan\Module\getListCard. Removed a ton of repeated code.
- Updated \xan\element\eleSearchBarListDB to pass optional params to make reuse of List Cards possible.
- Moved \xan\element\eleSearchBarSimpleDB below \xan\element\eleSearchBarListDB.

2022-12-18-15-28-00
- Updated Products to use the Attr Labels from Settings.
- Updated mmSalesItemsT.php onSaveColCalcs to support a Code col as a typeahead field. Editing replaces the selected Product using the Code.
- Updated mmSalesT.php header and picker to show like: Invoice #100, 11/16/2022, $120.
- Updated \xan\eleMeta so choices can use a Constant that ends with "_CHOICES_SQL" which is an array with the Table Name and an SQL Statement.
- Updated \xan\modules so Pickers use the shorter Header Text over the longer List Text.

2022-12-15-17-56-59
- Renamed DB Columns "Desc" to "Description".
- Renamed Products "Title" to "Name".
- Removed addtional ELE_AS_INPUT_TEXTHIDDEN from Cards that use Picker since the Picker adds it own ELE_AS_INPUT_TEXTHIDDEN.
- Decided on Grid vs Wide table for Products Pricing, Vendors Products, Sales Items.
- Updated Picker to include an optional Image along with the text.
- Updated Picker to include a Clear Button when the Search Button is displayed.
- Updated the $mm module var to $GLOBALS[ 'mm' ] so modules can be available within functions.
- Updated AutoLogout to check on the browser tab focus to see if the user should be logged out.
- Renamed the xan-save.php to xan-do-save.php to group with future global do files.
- Updated xan-do-save.php to pass the changed columns onto \xan\Module->onSaveColCalcs to know what calculation to apply.

2022-12-08-17-37-00
- Added a new ELE_TYPE_FILE_BUCKET_DB Render ELE_AS_LABEL_AND_BUTTONS used to create the Label, Upload Button, and Clear button. Also added ELE_AS_FILE_BUTTON_UPLOAD and ELE_AS_FILE_BUTTON_CLEAR.
- Added a Module doFileBucketSetURL function to make easier use in do.php.
- Added a PhotoFN for Users table. Added the Photo to Users Detail with a Gravatar Set Button. Added the Photo to the List Table.
- Added Constant STR_GRAVATAR_SET_PHOTO for the text on the "Set Photo to Gravatar" button.
- Added Constants IMAGE_HEIGHT_LIST, IMAGE_HEIGHT_INPUT, IMAGE_HEIGHT_LARGE for Image Size consistancy.

2022-12-04-17-42-28
- Removed Contacts standalone picker. Will replace using a version of the existing picker when needed.
- Modified \xan\Module->getContentImage to return a rendered string instead of the object.
- Modified \xan\Module to add a $tagsCellImage property for the image cell size.
- Removed \xan\Module->getListItemTableForPicker now using \xan\Module->getListItemTable everywhere.
- Removed \xan\Module->getListItemTable_Text and \xan\Module->getListItemTable_ImageAndText. Now can call \xan\Module->getListItemTable include the image automatically, if defined.

2022-12-04-12-36-36
- Modified xan.php into 25 separate php files, each required in init.php.
- Removed Module->getContent and replaced with calling the content types directly like Module->getContentTextBrief.
- Renamed eleURLImage to eleImage as the URL is a parameter.
- Renamed Module->doPicker to Module->getPickerContent.
- Renamed Module->getListItem to Module->getListItemTable.
- Renamed Module->getListItemWImage to Module->getListItemTableWImage.
- Renamed \xan\phpFileInfo to \xan\logEventPhpFileInfo to make it part of the log functions.

2022-12-01-15-38-40
- Updated Picker to use the Column Name passed instead of the default Table Key Name to support using fields like ReferredUUIDContacts.
- Updated Picker to use the cell instead of the text for the onclick. Using the text result areas not being clickable.
- Added to Contacts: Picker for Salesperson Staff and Picker for Referred By Contact.
- Updated app/module/content-page.php to not define an image. Inead now calls the Module->getListItem function or getListItemWImage.
- Added Module->getContentImage.
- Updated xan.js xanMessageDisplay to remove the Saved Column Name from being displayed in the menubar. Now states "Saved". The Column Name is included in the Browser Console.
- Added xan.js functions for xanStrSubstitute and xanStrBetweenNeedles. Using same names as php functions when possible.

2022-12-01-11-14-39
- Updated \xan\Module->getPicker. Was using the page Record Key and now using the Module Record Key. This make it possible to work with Portals.
- Updated all Modules->getListItemTableForPicker so the Module ListRow content can be reused.
- Added PICKER_SHOW_GO_BUTTON Constant for a default to show a Go Button for Pickers. Default is false as the ListRow data is a button itself.

2022-11-28-09-07-58
- Updated the order of the Menus to move Projects before Sales.
- Updated File Browser menu item to open in a New Window.
- Updated the background color of Picker data.

2022-11-27-17-52-04
- Updated Column Value Massaging. Now optionally Massages all Detail values, post query. List values Massaged as specified in the Module getContentListRow and getContentHeader.
- Renamed massageColsForGUI to massageRowForGUI.
- Added massageColForEcho to massage one value.
- Added examples to getContentListRow and getContentHeader for getting the Actual or Massaged value.
- Added a Clone function in \xan\recs. Experimented with Cloning Recs.
- Added a function \xan\arrayClone for Cloning Arrays.
- Added a function \xan\objectCloneDeep for Cloning Objects.
- Added Khan to the User Menu for Admins.

2022-11-23-19-14-29
- Added \xan\xan\products, \xan\xan\purchases, \xan\xan\settingscompanies, \xan\xan\vendors. Some were not added to git.
- Added Settings Columns for the three Product Attribute Labels.
- Changed Products Cards to use the Settings Product Attribute Labels. Need to use as labels everywhere.
- Renamed Settings Cards numbers for grouping.

2022-11-22-17-48-15
- Updated Khan Module Header to break each column into its own append so commas will be presented correctly. Auto adds the first four columns.
- Added Vendors Module using Khan.

2022-11-22-15-53-30
- Updated \xan\modules->getContentHeader and \xan\modules->getContentListRow to be in that order and to call \xan\recs->massageColsForGUI only one time.
- Updated the new modules ( SettingsCompanies, Vendors, Products, Products Pricing, and zzTemplateModule ) to define columns for the Header and ListRow.

2022-11-22-12-28-27
- Added Module Settings for SettingsCompanies, Vendors, Products, and Products Pricing.
- Added SettingsCompanies Module generated with Khan and fixed Khan issues.
- Fixed \xan\module->getListItem to set the cell to 0, 0 instead of 0, 1.

2022-11-21-11-26-18
- Renamed Module and Table Events to CalendarEvents.
- Renamed Module and Table Trans and TransItems to Sales and SalesItems.
- Added Module and Table Purchases and PurchasesItems.

2022-11-15-14-34-07
- Renamed Root folders to xanApp, xanCache, and xanStorage with constants PATH_ROOT_APP, PATH_ROOT_XANCACHE, and PATH_ROOT_XANSTORAGE as App conflicted with PATH_ROOT_APP.
- Updated Settings and Stats to use the new paths for xanApp and xanStorage.
- Added /xanApp/xan/xan-mysqlReports.php for creating FileMaker like sub summary reports with an example.

2022-10-18-16-14-51
- Set All Cards to default to a height = $resp->cardHeight which defaults to CARD_HEIGHT_0100. Settings > Users overridden to CARD_HEIGHT_0125, a newly added card height.

2022-10-02-16-44-08
- Updated Contacts Comms spacing.
- Updated Projects > ProjectsTasks with Dividers only below records and not after ProjectsTasks.
- Disabled Loading the last record if no record is loaded. Can be enabled again.
- Updated in xan.css the xan-font-size-portal from 0.7rem to 0.8rem.
- Removed Constant PORTAL_LABEL_FONT_SIZE.
- Added Constant PORTAL_HEADER_HEIGHT.

2022-10-01-18-10-12
- Added Module automatic last record reload if going to the Module without a record selected, mimicing FM selected record. The Found Set is NOT restored, only the last record viewed.
- Updated Pickers to use DB_LIMIT.
- Updated Projects > Print like our old FileMaker database.
- Updated Projects > Print can receive a comma delimited list of ProjectsTasks IDs to print only those ProjectsTasks to the Ballpark Estimate.
- Updated templates/pdf-default Footer to use the Printed Date by replacing [[DATE-PRINTED]] to show localized dates. The wkHTMLtoPDF dates were in non-US formats.

2022-10-01-13-26-37
- Added an ID to each instantiated \xan\eleCard to auto save and restore its width and height.
- Added a User Menu Item to "Reset Card Sizes". This will clear the saved Card width and height values for the current page.

2022-09-29-16-15-41
- Added DisplayedShortcut Keys to Print PDF and the SearchTerm.
- Added in Projects Checkboxes to Select ProjectsTasks that remember their Ticked State in the Browser Local data.
- Added in Projects on ProjectsItems and ProjectsTasks Cards that remember their width and height in the Browser Local data.
- Added in Projects the ability to select a ProjectsItem to see only the related ProjectsTasks.
- Updated Projects Print to match our Ballpark Estimate format. Need to finish.
- Added to Modules the getColEleRender function that can be used for Conditional formatting of data using style and color classes.
- Added templates/pdf-default CSS includeds for the Color Classes and Font Awesome. Added to the Header, Body, and Footer.
- Added FontIcon Constants for Modifier Keys. Also added a version with simple chars for where Font Icons cannot be used like Input Placeholders.
- Fixed \xan\xan-printer.php so the Headers and Footers work. Was checking the Header replacements as a string, but needed to be an Array Count.

2022-09-18-15-48-14
- Added a Query Limit of 100 when doing a Find with an Empty Search Term.
- Added an Asterisk Button to the SearchBar to Find All with no Limit.
- Added the Total Record Count to the Card Title with the Found Record Count like "100 of 487".

2022-09-18-15-00-27
- Added a link to CHANGELOG.md in README.md.

2022-09-18-14-56-09
- Fixed Bug in \xan\paramDecodeQuotes used in QueryBuilder. Spaces ended up around the ampersand in &quot.

2022-09-18-14-26-17
- Renamed \xan\module->getDisplayHeader to \xan\module->getContentHeader.
- Renamed \xan\module->getDisplayList to \xan\module->getContentListRow.
- Replaced calls to \xan\module->getContentHeader with \xan\module->getContent which acts as a mini router for table calcs. Can pass already queried \xan\recs or an ID to perform a fresh query.
- Added \xan\cacheGet and \xan\cacheSet to be used with \xan\module->getContent but the small bits of data read from disk was slow. Keeping for future use.
- Updated xan.js xanGoURL to support using the alt/option key to open links in a new window.

2022-09-13-14-26-41
- Updated \xan\module->getPicker so the Search and Go buttons are optional.

2022-09-13-13-23-14
- Fixed Contacts > Comms switching between Comm Types.
- Renamed Projects Cards to use the standard naming.
- Updated Projects to show the Sum of Hours for Estimated and Actual.
- Fixed eleGrid Margins and Padding.
- Updated Tooltips in xan.css so Tooltips can be be as wide as needed. Use <br /> to force breaks.
- Added xanModifiers in xan.js can now check xanModifiers.altKey to see if alt/option is pressed.

2022-09-08-18-55-05
- Updated Projects Tasks element placement.
- Added in xan.css ".row.active" so the selected Grid Row is highlighted.
- Added a white border to the standard buttons for contrast on a selected Grid Row.
- Added to HTML_DIV_DIVDER the class "m-1" to add a slight space between rows.
- Updated all uses of Tooltips to use \xan\tagExtraTooltip function.
- Added Projects > ProjectsItems Tooltip on Status Label. Shows Sum of Related ProjectsTasks HoursEstimated and HoursActual.

2022-09-08-16-13-18
- Looked at removing JQuery where possible, but we're using a few libraries that use it heavily. Doesn't seem worth the time right now.
- Changed xan.js use of "bind" to now use "on".
- Fixed Settings > LoginWith2FA as the wrong field was used.
- Changed the User Menu divider groupings.
- Added Constant STR_URL_SEP. Already had STR_DIR_SEP and STR_SEP.
- Updated Projects > ProjectsTasks Duplicate and Delete to reload with the ProjectsItems ID in the URL.
- Renamed in \xan\response  jsSetFocus to jsSetFocusOnReturn which will set the Focus on xanDo Return.
- Added in \xan\response jsSetFocusOnPageLoad which will set the Focus the next time a Page Loads.
- Updated Projects > Tasks Duplicate and Delete so when the Page Loads to include the ProjectItems ID.
- Updated Projects > Tasks Duplicate to set the Focus to the ProjectsTasks Title after the Page Loads.
- Added Calling Examples to \xan\timeDiffInSeconds and \xan\timeDiffInHours.

2022-09-06-16-02-32
- Added Form for Projects > Items > New Task Dialog to enter Title, Desc, Hours, or a 'Formatted' Task.

2022-09-06-14-02-32
- Added eleGridArticles element that can show floating Articles, similar ot floating Cards but with no borders.
- Added eleGridOfRows that behaves like the existing eleGrid, but less complex.
- Removed eleGrid and eleGridRow after updating to eleGridOfRows.
- Updated \xan\eleMeta columns to use the Column Name if the Label is not set.

2022-09-05-14-17-47
- Added Settings > Features LoginWith2FA.
- Updated Settings > Features Auto Logout Seconds to have a Tooltip: -1 to Disable; 3600 for 1 day; 25200 for 7 days;
- Updated navItemDropdownModule and navItemDropdownCustom FontIcons to be the same width and centered. Previously, each icon was left justified, but Icon widths varied.

2022-08-23-16-51-01
- Added Contact fields EmailTo, RateHourly, DriveMiles, DriveHours.
- Added /xan/Module function getListItemTableForPicker and added function to each class instance.
- Added /xan/Module functions getPicker that renders a picker and doPicker that handles the picker search results.
- Added Projects field pickers for Contact and Staff.
- Added Tooltip Underlines to objects that can show underlines. FontAweseome buttons do not underline.
- Added class to xan.css xanControlBackground so picker value text have the background but not a border like regular controls.
- Added ElementAs Type ELE_AS_INPUT_TEXTHIDDEN for the UUID Input for the picker.
- Added Schema LabelENTooltip to be able to have system wide Field Tooltips like Contacts 'EmailTo'.

2022-08-16-15-13-12
- Continued on Projects...
- Added Note about how to generate an in file password in /xan/xan-file-browser.php.
- Added TAGS_ELE_LABEL_PORTAL for Labels not in the Header.
- Updated /xan/xan-save.php to enclose Column Names in backticks. Updated to skip updating values if the Element Value = '' and the DB Value = NULL.

2022-08-13-17-40-17
- Started to edit Projects.
- Removed old File Editor, PHEditor.
- Added Files Browser available from Setting Actions menu. Connected to the session and will log out when the user logs out.

2022-08-09-18-08-42
- Added Module files for Disbursements, Projects, ProjectItems, ProjectTasks, Trans, TransItems.
- Added \xan\Response variables req1 thru 5.
- Updated Projects to Show ProjectsTasks from ProjectsItems. Added New ProjectsTasks button that works even if the Item is not selected.

2022-08-09-15-37-13
- Added Khan Generated Projects and Transactions to Git.

2022-08-08-10-02-15
- Removed Khan Transactions and Projects. Added Demo for Plans based on Projects, but renamed. Plans will be kept as an example for Khan.

2022-08-07-15-38-03
- Added a Schema Update Menu Item in Settings Actions which loads and saves a JSON file as a cache stored at PATH_ROOT_XAN . FILENAME_SCHEMA.

2022-08-07-15-03-18
- Moved Examples from Home to Settings Examples.
- Added Examples to Users Menu in the Admin only section.
- Renamed URL_BASE to URL_ROOT for older pages with commented out usages.

2022-08-07-13-15-15
- Tested Backups after the refactoring of Root Web and Root Other.
- Updated Settings Backups to show the percentage free along with teh free space. Both Root Web and Root Other will be shown if the free space differs.

2022-08-06-13-21-23
- Refactored web root to a folder "rootWeb".
- Refactored files and backups from external drive to a folder "rootOther".

2022-08-04-16-02-44
- Updated Settings Backups to only show zip files.

2022-08-04-15-36-52
- Tested APIRequests by running a 'Random Amount' request and 'Process Queue' request but an error occured and the entire queue was not processed. Updated so each request in the queue gets its own response and a summary if responses are returned.

2022-08-02-17-44-17
- Added Constants for FM_USE_FMREST and FM_FIELDS_KEY, used with class \xan\fmResponse.
- Added class \xan\fmResponse, used with class \xan\fmDB. fmResponse normalizes the data from either FileMaker XML Web Publishing convered to JSON or from FileMaker Data API using fmRest.
- Updated class \xan\fmDB to support offset, script, scriptParam, scriptPreRequest, scriptPreRequestParam, scriptPreSort, scriptPreSortParam.
- Updated class \xan\fmDB notes about Portals, Omit, and Sort.

2022-08-02-17-05-28
- Added /init_foo.xanweb.app.php called in init.php as an example.

2022-08-02-16-33-03
- Added /include/pheditor File Manager and implemented in /fileManager.php.

2022-07-22-17-32-56
- Added Settings Tasks Monthly to Router and Crontab to run on the first of the month.
- Added do-tasks-weekly-logDumpSQL to 'Settings Tasks Monthly' to dump records older than 90 days from LogAudit and LogEvent to the Backups folder along with regular backups.
- Added tableName parameter to \xan\recordsExport to bypass the need for the metaMoule.

2022-07-21-15-34-39
- Added sample code to init.php for opcache static + preload.
- Added an Audit Log Viewer to Contacts, Comms, Settings, Users, APIRequests with a shared Modal instantiated on page-resp.php.
- Added a xan.php function to create a Table for the Audit Log Modal.
- Added Settings do-modal-logAudit.php file to populate the Modal with the Audit Log.

2022-07-14-18-23-06
- Updated Aloe Session to only set the Session ID Name if not already set in order to set the session in Router, explained below.
- Updated Router to Init the Session without regenerating the Session ID to be able to Log the Request. Had to update Aloe Session to not re-set teh Session ID Name if it was already set.
- Added Xan phpFileInfo function to create a clean way to see where an event occurred with the File Name, Line Number, Namespace, Class, Function, and Path
- Updated Send SMS and Email to log what was sent but with the exception of the message body HTML and Text.
- Updated Log calls to use the phpFileInfo function.

2022-07-12-18-30-38
- Updated calls to logEventToFile to logEventToSQL. Passed __NAMESPACE__ . '_' . __CLASS__ . '_' . __FUNCTION__ in Desc1 when possible.

2022-07-12-15-37-16
- Added to Setting Tasks Often, Auto Deletion of Users that have not clicked the Registration Link within 3 days.

2022-07-11-18-12-05
- Updated Router Login and Router Logout to terminate the session on load.
- Updated Status Session to show a list of User Session and Path Sessions. Empty Sessions are not shown, but the count is shown.
- Added Settings Tasks Often that purges 'sess_' and 'CURLCOOKIE' files.
- Updated Crontab to run Settings Tasks Often.
- Updated Settings Backup to prefix the file with the APP_NAME.
- Updated to keep 20 backups and must be less than thirty days old.
- Renamed \xan\dateStrFromString to \xan\dateTimeStrFromString.
- Updated Stats Sessions to show sessions with an email address first. Then with a Path, then the remaining sessions.

2022-07-09-16-52-19
- Updated abstract class module functions 'getListItem' and 'getListItemWImage' to highlight the search term, if passed.
- Added Xan functions for strSubstituteCaseInsensitive and strSubstituteCaseMatching.

2022-07-09-15-05-02
- Updated Settings Backups table padding and changed the zip icon to a new icon.
- Updated Settings Backups to auto delete backups older than 30 days but only the most recent 5 backups.
- Update eleTable, removing right and bottom padding from table but keeping left and top padding.

2022-07-09-13-00-34
- Replaced zip functions with zipfile class. Previous addDir did not work. Now it does!
- Fixed xanDo function timeBegin and timeEnd math to use valueOf instead of getMilliseconds. Was always less than a second but now accurate.
- Updated Settings Backups to zip SQL, Code, and Files into one zip file. Auto deletes after 15 days. Sends text message with time spent, total size of backup, and a link to the backup for easy downloading.
- Updated Moment from 2.29.2 to 2.29.4.

2022-07-05-17-36-31
- Removed use of xan.js date function in favor of Moment. Added a comment: "Use moment.js like in xanEleFlatpickrSetFromSelect function in this file."

2022-07-05-17-23-26
- Updated colValueMassageForGUI to handle Currency from SettingsSchema Table EleFormatAs Column. Works on Contacts Detail and Print.

2022-07-05-16-27-24
- Added Calendar Module. Moved Calendar from Home to the Module.
- Enabled Delete Button.
- Changed Month View to be the default.
- Added Category field in Calendar Edit Dialog.
- Added 2 second delay in refetching events after Save and Delete.

2022-07-04-17-14-50
- Changed ChangeLog location in README.md.

2022-07-04-17-08-48
- Updated Home adding Button for APIs, Calendar, IMAP, Khan, Stripe, and Tests. These were hidden but available as home/apis... Now exposed.

2022-07-04-16-09-14
- Updated Khan module generator to work with the Schema Table.

2022-07-02-17-17-54
- Removed Moment 2.24.0.

2022-07-02-17-12-58
- Updated Moment 2.24.0 to 2.29.2.

2022-07-02-17-02-55
- Removed eleMeta details from Module files. Set Non Table Module files like Table Module files.
- Updated templates/calendar.js.

2022-07-02-16-06-33
- Removed Google Fonts in the PDF-Default Template.
- Removed Bootstrap Icons, removed DayPilot in favor of FullCalendar.
- Updated to DataTables 1.12.1, FontAwesome 6.1.1, FullCalendar 5.10.2/free.
- Removed Dark Mode. For Dark Mode in Browser, consider https://darkreader.org.
- Moved source of eleMeta details from Module files to an SQL Table, populated and updateable using information_schema.columns.
- Renamed ELE_AS_DEFINED to ELE_AS_INPUT.
- Added app/settings/do-certbot-log-email.php called from crontab.

2022-02-15-16-12-41
- Added FontAwesome 6.0.0. Updated PSoS icons to fa-beat-fade.
- Added DayPilot Lite 2022.1.362.

2022-02-15-14-14-51
- Khan can now generate a new project from database tables and some info about the tables. Cleaned code during the creation of Khan.
- Added Modules for Projects and Transactions. Need to customize for FMSB like functionality.
- Added Module property for colNamesToMassageA to set a list of columns to be massaged. If not set, column types date, time, datetime, decimal, and integers are massaged.
- Changed how row massaging works. Now called only when needed for headers, printing to html/pdf, etc.
- Added filenameClean function to clean up filenames for printing to html/pdf.
- Added DATETIME_FORMATS for US Dates.
- Rewrote xan.js xanDateTimeStrToStr. Now uses PHO formats like n/j/Y
- Updated xan.css dividers for less white space.

2022-01-18-17-00-25
- Khan dev began. Khan is a Module Generator. Just add SQL tables and columns, write a little php to describe the module, and generate!
- Khan needs the files for printing, rec delete, rec duplocate, and rec create.
- Moved fm-example-1 module from BRG our of the project and into "z fmRest" folder.

2021-12-21-14-54-20
- Added fm-example-1 module from BRG.
- Renamed date, dateTime, and time functions.
- Updated xan.css.

2021-12-21-13-23-43
- Added BingMapsKey to Settings.
- Added DATETIME_FORMAT_USDATE.
- Remvoed BRG Test

2021-12-07-14-42-13
- Added ID and Name attributes to Cards, Card Header, and Card Body. Header and Body will be the Card ID or Name with an underscore suffix.
- Upated Settings > Backups buttons to return the Card Content via Ajax.

2021-12-07-12-56-24
- Removed 'content-cards.php' and moved code to 'content-page.php'.
- Added PATH_ROOT_ALT for Backups and Files.
- Added Font Icons for Database, Code, Files, and Download.
- Added Settings > Backup Card with ability to backup SQL, Files, and Code with Delete All and individual Delete buttons.

2021-11-28-17-25-22
- Updated Buttons from Secondary to Primary
- Updated content-cards.php to use $mmTable.
- Updated all do.php files to use a switch statement instead of a series of if statements.
- Updated router.php to use a switch statement instead of a series of if statements.
- Set the Card min-height to CARD_HEIGHT_0100.

2021-11-28-15-06-58
- Added Access Keys for Print, Search, and Records First, Last, Previous, and Next.
- Added Gravatars in Comms Email with button to "Set Photo".
- Added a Photo button to Clear the Photo.
- Added Address County, Country, Latitude, Longitude with Labels.
- Added Address Buttons for Zip Lookup, Street Standardization, and Address Correction.
- Cleaned Contacts Comms code.
- Updated Nginx and page-resp.php Content-Security-Policy to allow Gravatar.
- Renamed recsSquerySimple to recsGet.
- Renamed STR_BR to HTML_BR. Added STR_DIV_DIVIDER.
- Added Comms do.php.
- Cleaned do.php to use a case statement.
- Added a Tiny Button: ELE_CLASS_BUTTON_SET . STR_SP . TEXTSM and SECONDARY.
- Renamed \xan\ 'dir' funtions to 'path' functions.
- Renamed \xan\urlContent to \xan\urlTextContent.
- Added \xan\urlDownloadToPath to download a url file to a path.

2021-11-20-16-15-05
- Updated CSS Vars to be based on bootstrap grays.
- Moved CSS from page-resp.php to /xan/xan.css.

2021-11-16-15-45-14
- Added Optional Bootstrap Tooltips to Buttons.
- Removed ContactsNameUpdate and UsersNameUpdate from the Contacts and Users content-pages.php files and deleted the Contacts and Users do-*-nameUpdate.php.
- Renamed setColCalcs to onSaveColCalcs in metaModules.
- Added onSaveJSActions in metaModules.
- Updated onSaveColCalcs and onSaveJSFunctions in mmAPIRequestsT.php, mmContactsT.php.

2021-11-12-18-04-35
- Moved js function xanDoJS from page-resp.php to /xan/xan.js to use it in xanDo and xanSave.
- Updated xan-save.php to reply with rowsD and jsActionsA.
- Added mm abstract function setColCalcs.
- Updated /contacts/content-cards.php content header to have a specific ID for the selected contact so xanSave can update via jsActionsA.

2021-11-09-21-04-29
- Renamed mm->getDisplayName to mm->getDisplayTitle.
- Removed NameUpdate of Header and List Item from Contacts and Users. Working to replace with Calulations.
- Reworked /xan/xan-save.php.

2021-11-05-11-38-00
- Removed an extra space in the page header before the colon.
- Added a Tooltip to the Image Upload button.

2021-11-04-15-01-27
- Added class and instance for $xan->get( '123' ) to make adding PHP to JS via {}.
- Renamed Tags to make more sense.

2021-10-19-19-06-35
- Added Functions \xan\strChr.
- Changed User Menu Items Order.
- Added Stats Process Pools Count.
- Renamed and rearanged constants for Heights and Widths. Removed some unused contants. Changed size number to be based on percentages starting with 100% = 0100.

2021-10-02-18-11-41
- Added xan-mysqlTools.php for MySQL Backup and Restore.
- Added Home Examples for MySQL Backup and Restore.
- Added Home Examples for FileWrite, Gzip, UnGzip, Read, Delete.
- Added \xan\ functions for fileGzip, fileUngzip, fileDelete.

2021-09-21-22-50-15
- Updated Bootstrap 4.5.0 to 5.1.1. Need to update Buttons that use FontIcons.
- Fixed Contacts Picker Clear Button which was adding WHERE when finding all records.
- Added function \xan\eleTable->generateDemoData.
- Added Colors for Heat Map to xan.php constants from https://www.schemecolor.com/hot-and-cold.php
- Added a param in \xan\eleTable->generateDemoData to display as a Heatmap.
- Added functions \xan\arrayValuesUnique, \xan\arrayValuesRemove.
- Separated Array and Dict functions to be named like arrayImplode or arrayDImplode. Both ar arrays, but these names help to separate how they work.

2021-09-21-15-38-55
- Renamed $tableEle->dataTableScriptOnLoad to $tableEle->dataTableInit
- Updated calls of strtolower to \xan\strCaseLower.
- Update DataTable CSS.
- Added DataTable FI_ORDER for row reordering.
- Added DataTable params so Buttons and Filter can be placed at the top/bottom let/right.

2021-09-09-14-21-51
- Removed the function strTagsRemoveScript and all calls to it.
- Removed most uses of ob_start to HEREDOC JS/HTML. Keeping ob_start when PHP looping is needed.
- Fixed Contacts Comms 'go' buttons showing and hiding. Renamed CallPhoneLink to PhoneCallLink to match PhoneSMSLink.
- Renamed \xan\strFilterKeep functions to remove the 'Keep'.
- Fixed \xan\eleTable->render loop that gets the rowMax and colMax. Was using the last row's col count rather than the using the largest colMax.

2021-09-07-11-45-02
- Fixed APIRequest Printing.
- Removed one use of ob_start to HEREDOC JS/HTML.
- Added Card Widths 4x to 9x.
- Updated each page to Load Content Immediately rather than optionally via AJAX after page load.
- Added functions for numRound, cssSizeFactor.
- Updated functions strFilterKeepNumbers and strFilterKeepAlphanumeric to also include decimal point and dash.
- Updated Cards to be Resizeable by default.

2021-09-06-14-20-21
- Removed page-resp.php head meta logout. Using setTimeout redirect instead.
- Added page-resp.php XSS Headers was missing.

2021-09-05-17-08-25
- Updated Contacts to no longer have a content load now or later making now be the only choice.
- Updated Table Constructor to only add an ID if the ID is not empty.
- Updated page-resp.php JS to be in functions. Reordered too.

2021-09-05-15-10-04
- Updated DataTables example on Home.

2021-09-02-15-59-10
- Added DataTables.net 1.11.0 to Includes and an example on Home in the Table Card.
- Changed colors in datatables.min.css from Green: #31b131 to gray and Red: #d33333 to gray.
- Added 4 Font Icons: Filter, Excel, PDF, and Clipboard. Already had Print.

2021-08-26-16-24-56
- Removed Stacktable.js as it was not used.

2021-08-26-14-19-38
- Added Note in init.php regarding MySQL Sort Buffer Size for version > 8.0.17
- Verified that all SQL calls use binding when using WHERE. Updated one SQL call.

2021-08-24-18-46-07
- Fixed SearchBar. Was missing the D in public $resp->reqPostD.
- Updated Home URL check for 'more', 'more2', 'morepurge' for demo purposes.
- Updated GPS to be 10 seconds.
- Added an IP Geolocation to Home via xanDo.

2021-08-19-13-35-55
- Updated Readme.
- Added IP Geocode function \xan\ipGeocode using https://ipstack.com/.

2021-08-19-12-51-36
- Updated \xan\urlContent.

2021-08-17-17-16-27
- Fixed backticks in Contacts List Images to show, Contact Picker, and Select 'Other...'.
- Updated Comms Portal to use \xan\get::TAGS_ELE_BUTTON_ONCLICK and added mr-1.
- Updated page-resp.php so the navbar, header, and content align.

2021-08-17-13-37-14
- Added ddeboer-imap to includes along with xan/imap class.
- Added IMAP Example to Home.
- Updated Home to put each Example in a Card.

2021-08-17-12-10-33
- Replaced \recs\recsDumpSQL with \recs\recordsExport

2021-07-18-17-02-13
- Merged xan-utility.php into xan.php. Removed xan-utility.php.
- Replaced all calls to \xan\tags to use \xan\get.

2021-07-15-17-34-47
- Added \xan\recs $idSelected to store the selected ID on the recs object.
- Added \xan\get TAG functions. Need to replace individual $tag calls.
- Renamed \xan\response $reqPathComponentsD back to $reqPathComponentsA since it's an array not dictionary.
- Renamed \xan\response functions so the suffix is Get or Set. NounVerb is the goal.
- Added \xan\tags property for $otherD for 'other' values. Used to pass file upload JS on Success or Problem.
- Added xan-utility.php function require_once_recursive.
- Updated \xan\filenameClean to work on filenames and no longer considers the path.

2021-07-05-13-26-29
- Renamed 'moduleMeta' to 'module'. Removed 'meta' from each subclass. Enclosing folder moved to root and named 'modules'.
- Renamed \xan\response $reqPostD, $reqPathComponentsD to append a D.
- Added \xan\response $reqIDsD to replace individual $reqIDs.

2021-07-01-17-28-45
- Organized the Loading Scripts including renaming files in /xan.
- Removed Setting Headers and a Metatag as it's now handled in NGINX.

2021-06-27-16-35-58
- Added functions for pathGetFileNameFull, pathGetFileNameNoExtension, pathGetExtension, pathGetPath, and filenameClean.

2021-06-26-15-43-01
- Added CURL timeout options in the API calls.
- Removed APIRequests Name Update.
- Removed APIRequests ContactPicker and New Button.
- Removed APIRequests Actions options Duplicate and Delete.
- Updated \xan\fileWrite to separate the Path and Filename. Path is created if it doesn't exist. File is written if Path exists.
- Updated calls to \xan\fileWrite to separate the Path and Filename.

2021-06-24-17-22-01
- Rolled back and reappied these changes.
- Changed Constants order in class-xan.php.
- Added \xan\get class for getting a class instance liek: \xan\get::TAGS_CELL_LEFT_MIDDLE().
- Replaced $tagsCell... variables with a new \xan\get class with static functions.

2021-06-22-14-55-13
- Added a meta tag for theme-color and set to the same color as the Nav Bar.
- Added a border-top to the Nav Bar.

2021-06-22-14-40-24
- Added /postit.php which lets GET requests be POSTed.
- Deprecated metaModule->getListRow to refactor a replacement. Started on the replacement on /app/apirequests/content-cards.php.
- Updated eleTable->cellset to add params for $rowGroup (thead|tbody|tfoot) and $isSticky.
- Updated eleTable->render to use cellset params $rowGroup and $isSticky.
- Updated eleTable->__construct to remove the $tagCellsEmpty param. Now sets in constuct and can still be overridden.
- Renamed eleMeta->widthForTable to eleMeta->eleWidthTable.
- Added eleMeta properties $valueHeader, $valueRow, $valueFooter for setting table values temporarily.
- Updated eleMeta->eleAlign to now accepts TEXT_ALIGN_LEFT, TEXT_ALIGN_RIGHT, TEXT_ALIGN_CENTER, TEXT_ALIGN_JUSTIFY.
- Added and Renamed CARD_HEIGHT_x Constants for easier access to quarters and thirds.
- Using Microsoft Edge for Mac, started fixing its suggestions.
    - Added a header for 'X-Content-Type-Options', "nosniff"
    - Added a title tag to the nav Dropdown.

2021-06-14-17-42-18
- Moved Files to another different dir than the app. This allows for putting files on another disk.
    - Moved upload.php to the app root. Need to refactor.
    - Updated PATH_ROOT and URL_ROOT var names to be consistent.
    - Moved upload to the root.
    - Fixed Contacts List Card Image ID.
- Fixed a bug with getListItemWImage and getListItem where on row x, x-1 extra html tr tags were added.

2021-06-12-18-02-11
- XanPro Commit Test

2021-06-12-15-47-52
- Added \xan\microsecsTracker class for millisecond level time tracking of code and loops.

2021-06-10-16-22-27
- Added a Constant TWOFACTORAUTH_ENABLED to enable or disable 2FA.
- Added getEleMetaRender ELE_AS_STRING.
- Added User table columns for '2FA via Phone' and '2FA via Email' to allow options for receiving the code.
- Updated the Password Meter to check for Password Length and spread out the Levels ( Weak, Moderate, Strong ).
- Register and Change Passwords now require a Strong password based on the Password Meter.

2021-06-08-16-21-56
- Removed setting $_SESSION[ SESS_USER ] from init.php Session was not started yet. It's set in mmUsersT->doLogin.
- Moved setting $_SESSION[ SESS_URL ] to aloe/framework/session.php.
- Added a mb-1 to the button classes, ELE_CLASS_BUTTON_BLUE, ELE_CLASS_BUTTON_BLUE, ELE_CLASS_BUTTON_GRAY, and ELE_CLASS_BUTTON_GRAY to add bit of vertical space.

2021-06-08-15-26-13
- Fixed eleTable->render to correctly set table thead and tbody.
- Renamed FontAwesome properties to FontIcon since we're using FontAwesome and Boostrap Icons.
- $_SESSION[ 'urlCurrent' ] is now $_SESSION[ SESS_URL ] to replace the string with a constant.

2021-06-06-16-20-23
- Updated Init, mmSettingsT, and Settings Card values to appear in similar order.
- Added Settings for Phone Number, Email Address, and Postal Address.

2021-06-05-16-30-10
- Added eleMeta->eleAlign that accepts left, right, center, justify which defaults to left.
- Added Utility Function arrayContainsString for searching arrays for a value.
- Added additional reqID properties 2, 3, 4, 5
- Added getListRow params $rowHaButton and $rowColNamesA for tables in List Cards.
- Added eleCard IDs to make Showing and Hiding Cards simple.
- Added eleSearchBarListDB->render optional properties for $inclColA, $inclColMod, and $inclColKeys.

2021-05-15-14-37-21
- Removed an unneeded call to fmREST.

2021-05-13-17-45-29
- Added Contacts Comms create SMS to go with call.

2021-05-13-17-12-47
- Fixed \xan\response->metaSet(). Removed an extra quote and closing bracket.

2021-05-13-17-01-49
- Updated Home to add more examples. Added a use of php date_default_timezone_get.

2021-05-13-16-39-14
- Added a clickable link to the 2FA SMS and Email messages that will open a new tab to complete the Login. Works similar to the Registration One Time Code.

2021-05-13-15-34-17
- Added setting the default timezone to UTC in init.php.
- Added a function for arrayValuesWrapWith and arrayValuesWrapWithBackticks. Using to wrapping Column Names with backticks. Moved array functions higher within functions_utility.php.
- Updated sqlUpsert to use arrayValuesWrapWithBackticks. Goal is to wrap all SQL Statement Column Names with backticks everywhere possible.

2021-05-13-14-38-07
- Renamed /sql/ files from sequential numbers to dates.
- Added /sql/xan-2021-05-13.sql to add columns for constants: APP_COUNTRY_CODE, TWITTER_SITE, TWITTER_AUTHOR.
- Changed ALTER TABLE commands to use AFTER to keep table column order.
- Changed init.php to use the database values for APP_COUNTRY_CODE, TWITTER_SITE, TWITTER_AUTHOR.

2021-05-13-12-57-31
- Added constants: APP_COUNTRY_CODE, APP_LOCALE, TWITTER_SITE, TWITTER_AUTHOR. Need to add to the Settings Database Record.
- Added properties to \xan\response to support optionally adding html meta tags via \xan\respone->metaSet();
- Added \xan\respone->metaSet(); to several pages.

2021-05-11-15-09-05
- Updated Register Password Rating as a function in xan.js xanPasswordRating.
- Added User Change Password Rating using xan.js xanPasswordRating.

2021-05-11-14-10-04
- Added a simple Password Rating of Weak in red, Moderate in yellow, Strong in green.

2021-05-11-12-51-44
- Added a function sqlUpsert that creates a sql statement that will INSERT / ON DUPLICATE KEY UPDATE that will either Insert a record or Update a record if it already exists.
- Renamed a few functions to: sqlInsertQuestions, sqlLikeWhere, sqlLikeBindNames, sqlLikeBindValues, dbQueryBuilder_DataType, dbQueryBuilder_FindFilter, and dbQueryOrderBy_DropdownItem.

2021-05-10-12-18-05
- Fixed an issue with quotes when displaying font icons during ajax calls.

2021-05-06-17-52-02
- Added Bootstrap Icons.
- Replaced iconFA function with fontIcon. Adds a tags parameter. Works with both Bootstrap Icons and FontAwesome.
- Planning to remove FontAwesome when to Bootstrap Icons collection is larger.
- Replaced all FontAwesome html with the equivalent fontIcon function.
- Ranamed all "FA_" icon constant names to "FI_".
- Removed eleCard->renderListItemLink as it's now redundant.

2021-05-04-16-46-46
- Commented out XanDo javascript alert.
- Touched images and index.php.

2021-05-04-15-48-16
- Summary: Simplifying List Cards while adding options: Items Text, Items Image + Text, or a Table Row.
- Removed three functions from moduleMeta class and each subclass. Replaced with sharable moduleMeta functions.
- Added eleMeta property eleWidthTable that defaults to empty string but can be overridden per Table Column Name.
- Added two new moduleMeta getList functions: getListItem is for text, getListItemWImage is for an image + text, and getListRow is for html tables at full page width with a default column width.
- Updated content-cards.php Lists for Contacts, Contact Picker ( image + text ), Settings-Users ( text ), and APIRequests ( html table ). It's now easy to change how Lists are displayed.

2021-05-01-18-08-00
- Added a link to the ChangeLog in the ReadMe.

2021-05-01-17-58-33
- Updated APIRequests getListItemRowHeader and getListItemRow functions to a single function getListRow as an option to getListItem.
- Updated APIRequests List Card Styles from mini/wide to items/rows.
- Updated APIRequests List Card Styles to also set the Card Width.

2021-05-01-17-06-03
- Updated APIRequests to have an option to have Mini or Wide List.

2021-05-01-16-58-12
- Updated APIRequests 100% Wide List Table to use Column Labels rather than Column Names.

2021-05-01-16-29-11
- Fixed usages of NameModule, NamePlural, and NameSingular.

2021-05-01-16-04-10
- Added, for Admins, a APIRequests Module with a 100% Wide List Table and Sticky Header Row. Left most Column has a Button with the Row Index to view Details in Cards below the list.

2021-05-01-15-06-37
- Removed AutoLogout HTML Meta Refresh tag and replaced with a Javascript function that can push the Logout time out after AJAX calls.

2021-04-29-16-33-46
- Updated Stats Sessions to first look in ini_get( 'session.save_path' ) and then /tmp/. If no sessions found, now shows "$sessionsPath: /var/lib/php/sessions/ does not seem to be accessible."
- Changed the Stats Card order to show Sessions above Process Pools.

2021-04-29-15-31-29
- Added Stats Versions for OS, PHP, and wkHTMLtoPDF. Added section dividers.
- Fixed Processes values that were off by one row.

2021-04-29-14-36-51
- Updated references to GET and POST parameters for ID within comments.
- Fixed the missing $ for 'mmUsersT->nameSingular'.

2021-04-29-13-54-22
- Updated references to GET and POST parameters for ID to use metaModule property NameTable.
- Fixed case on api-process-queued Semaphore Error Messages.

2021-04-28-20-11-42
- Added functions-utility.php function paramDecodeQuotes to decode just quotes.
- Update eleSearchBarListDB to remove an extra parameter.
- Fixed eleSearchBarListDB Simple Query and Query Builder as both stopped working.
- Fixed eleSearchBarListDB so Table Keys and Mod Columns would not appear in Query Builder.
- Added metaModule property NameTable used for GET and POST params.
- Updated mmCheckout.php as it was missed.

2021-04-27-13-01-06
- Updated page-resp.php to make UTF-8 be capitalized.
- Update API calls to follow redirects.

2021-04-25-16-16-44
- Added API Handling. Can process immediately or queue!

2021-04-22-17-08-26
- Added a xanDo javascript alert function.
- Touched images, index.php, loading.php, and router.php for OCD reasons.

2021-04-22-17-02-04
- Updated Home Location button to use backticks for Javascript quotes. Will be using backticks more!

2021-04-22-15-42-07
- Added example code for hourofDay function.
- Added /sql/xan-2021-03-02.sql which creates the starting tables and sample data.
- Added /sql/xan-2021-04-21.sql which adds Settings columns AppLangCode = 'en' and AppTimezoneID = 'America/New_York'.
- Added in init.php constants for AppLangCode and AppTimezoneID to be loaded from Settings.

2021-04-22-14-21-34
- Added hourOfDayFunction( $timezoneID ) function. Used to prevent or permit running code at specified hours.

2021-04-20-18-52-51
- Renamed Array Variable to fix naming standard.

2021-04-20-18-44-47
- Removed all references to Tenant Table, Primary Keys, and SQL Statements.

2021-04-20-15-29-03
- Added function strAsciiSum used for PHP Semaphores.

2021-04-13-12-07-24
- Fixed the Stripe include after inserting the incorrect script.
- Fixed formatting of PHP Auto Logout Meta tag, PHP XSS Header, and PHP Stripe script include.

2021-04-12-18-20-41
- Updated Stripe to include its javascript on request rather than all the time.

2021-04-12-15-08-40
- Updated the init file loader to use HTTP_HOST instead of SERVER_NAME to load 'init_DOMAIN.php'.
- Updated the init file loader to use __DIR__ instead of dirname( __FILE__ ). Both are equivalant.
- Updated upload.php to use permissions 775 instead of 777 when creating directories.

2021-04-11-16-41-05
- Moved the directories logs|brief|bucket to files/DOMAIN/logs|brief|bucket to separate between instances.
- Updated Bucket Upload to use the new folder structure.

2021-04-10-17-15-30
- Updated XSS to use a Header rather than a Meta tag as Headers work with 'frame-ancestors'.
- Updated the database settings from a hardcoded 'init_private.php' to look for a file based on the domain name like 'init_xanadu.xanweb.app.php'. A basic text 404 message is shown if the domain doesn't match an existing file.

2021-04-07-10-24-21
- Updated Darkly css to comment out Google Font 'Lato' to prevent XSS notfications when Google Fonts is not approved. Darkly is for Dark Mode and from https://bootswatch.com

2021-04-06-17-35-18
- Update Reload and XSS formatting.

2021-04-06-13-08-08
- Disabled Google Fonts from XSS after news from the EFF: https://twitter.com/EFF/status/1378813625960427521
- Updated the Session Updated and Expires timestamps comment.

2021-04-06-12-40-26
- Disabled Google Fonts after news from the EFF: https://twitter.com/EFF/status/1378813625960427521

2021-04-01-16-45-40
- Updated XSS Content-Security-Policy frame-ancestors to none.
- Updated the mobile / narrow window hamburger menu to appear correctly appear in light and dark mode.
- Updated xanLocationGet err.code = 2 message to help Mac Safari users enable Locations Services permissions.

2021-03-31-16-50-10
- Updated xanDo and xanDoSave so xanMessage to show an icon immediately and when done, a success or error messages is shown. On success, the icon and message fades out. Now uses a table for formatting.
- Added sendSMSDebug function and constant for APP_SMS_TO_DEBUG. Moved the debug constants to init_private.php. Needed this to find a pesky error.
- Added Logging PHP errors to a file in the logs folder.
- Error fixed. Icon constants FA_SORT_ASC and FA_SORT_DESC were missing.
- Added Session values for Path and Info in router.php.

2021-03-29-18-23-26
- Contacts: Fixed Table Row incrementer.
- Contacts: Fixed missing ": " in NameUpdate.
- Encoded the $aloe_request->path_get() and $aloe_request->path_components_get().
- Updated xanMessage for xanDo and xanDoSave with larger icons and fix spacing in the javascript console.
- Updated Users nameUpdate to use NameFull.

2021-03-29-17-14-52
- Replaced $rowIndex++ with ++$rowIndex to increment inline.

2021-03-29-16-58-56
- Added a preceding backslash before all usages of xan.

2021-03-29-16-51-17
- Moved xan.js from /include to /xan.

2021-03-29-16-28-15
- Replaced usages of $_POST with $aloe_request->post.
- Replaced usages of \xan\valuePOST with \xan\paramEncode.
- Removed the functions \xan\valuePOST and \xan\valueGET.

2021-03-29-12-40-45
- Updated paramEncode to accept a value or an array.
- Fixed XSS Error regarding frame-ancestors by adding the site url.
