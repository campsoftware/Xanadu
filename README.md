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
