# ProtonMail Bridge and Import-Export app Changelog

Changelog [format](http://keepachangelog.com/en/1.0.0/)

## [IE 1.2.1] Elbe

### Added
* GODT-799 Skipped messages do not change total counts but shows as separate number.

## Fixed
* GODT-799 Fix skipping unwanted folders importing from mbox files.
* GODT-769 Close connection before deleting labels to prevent panics accessing deleted bucket.

### Removed
* GODT-766 Remove GUI popup for IMAP TLS error.


## [Bridge 1.5.0] Golden Gate
### Changed
* Updated go-mbox dependency back to upstream.

### Fixed
* GODT-847 Waiting for unilateral update during deleting the message.
* GODT-849 Show in error counts in the end also lost messages.
* GODT-835 Do not include conversation ID in references to show properly conversation threads in clients.
* GODT-685 Improve deb packaging regarding dejavu font


## [IE 1.2.0] Elbe

### Added
* GODT-763 Detect Gmail labels from All Mail mbox export (using X-Gmail-Label header).
* GODT-834 Info about tags in BUILDS.md and link to Import-Export page in README.md.
* GODT-777 Support Apple Mail MBOX export format.

### Fixed
* GODT-677 Windows IE: global import settings not fit in window.
* GODT-794 Congo fails to update to Danube
* GODT-749 Don't force PGP/Inline when sending plaintext messages.
* GODT-764 Fix deadlock in integration tests for Import-Export.
* GODT-662 Do not resume paused transfer progress after dismissing cancel popup.
* GODT-772 Sanitize mailbox names for exporting to follow OS restrictions.
* GODT-771 Show fatal errors after export is terminated.
* GODT-779 Do not propagate updates when progress is stopped.
* GODT-779 Unpause progress during fatal error to properly stop progress.
* GODT-779 Stop ongoing transfer calls sooner (re-check after import request is generated).
* Fix measurement of uploading attachments during transfer.
* GODT-827 Do not spam sentry with bad ID by integration test.
* GODT-700 Fix UTF-7 incompatibility.
* GODT-837 Fix flaky TestFailUnpauseAndStops.
* GODT-782 Don't use TLS pinning when checking connectivity status.

### Changed
* TLS pins conform to official list.


## [Bridge 1.4.5] Forth

### Fixed
* GODT-829 Remove `NoInferior` to display sub-folders in apple mail.

## [Bridge 1.4.4] Forth

### Fixed
* GODT-798 Replace, don't add, transfer encoding when making body 7-bit clean.
* Move/Copy duplicate for emails with References in Outlook
* CSB-247 Cannot update from 1.4.0


## [Bridge 1.4.3] Forth

### Changed
* Reverted sending IMAP updates to be not blocking again.

### Fixed
* GODT-783 Settings flags by FLAGS (not using +/-FLAGS) do not change spam state.


## [Bridge 1.4.2] Forth

### Changed
* GODT-761 Use label.Path instead of Name to partially support subfolders for webapp beta release.
* GODT-765 Improve speed of checking whether message is deleted.


## [IE 1.1.2] Danube (beta 2020-09-xx)

### Fixed
* GODT-770 Better handling of extraneous end-of-mail indicator.
* GODT-776 Fix crash when IMAP client connects while account is logging in.

### Changed
* Bump crypto version to v0.0.0-20200818122824-ed5d25e28db8
* GODT-785 Clear separation of different message IDs in integration tests.
### Changed
* GODT-741 Import-Export shows "Unable to parse time" notice instead of zero time in error report window.

* Bump crypto version to v0.0.0-20200818122824-ed5d25e28db8.
* GODT-374 Allow to send calendar update multiple times.

## [IE 1.1.1] Danube (beta 2020-09-xx) [Bridge 1.4.1] Forth (beta 2020-09-xx)

### Fixed
* GODT-752 Parsing message with empty addresses.
* GODT-752 Parsing non-utf8 multipart/alternative message.
* GODT-752 Parsing message with duplicate charset parameter.


## [IE 1.1.0] Danube

### Fixed
* GODT-703 Import-Export showed always at least one total message.
* GODT-738 Fix for mbox files with long lines.
### Fixed
* GODT-732 Do not mix font awesome icon with regular text to avoid issues on Fedora.


## [Bridge 1.4.0] Forth

### Added
* GODT-682 Persistent anonymous API cookies for Import-Export.
* GODT-357 Use go-message to make a better message parser.
* GODT-720 Time measurement of progress for Import-Export.

### Changed
* GODT-511 User agent format changed.
* Unsilent errors reading mbox files.
* GODT-692 QA build with option to change API URL by ENV variable.
* GODT-704 User agent detected by fake IMAP extension instead of AUTH callback (some clients use LOGIN instead of AUTH).
* GODT-695 Parallel upload for ProtonMail target.

### Removed
* GODT-519 Unused AUTH scope parsing methods.

### Fixed
* GODT-698 Use correct package type for signed PGP/Inline messages.
* Generic bug report window title.
* Fix missing check for unencrypted recipients during sending.
* Version checking for catalina.
* GODT-730 Limit maximal TLS version for Yahoo IMAP server.


## [IE 1.0.x] Congo (v1.0.0 live 2020-09-08)

### Added
* GODT-633 Persistent anonymous API cookies for better load balancing and abuse detection. 
* GODT-461 Add support for `\Deleted` flag.

### Changed
* GODT-462 Pausing event loop while FETCHing to prevent EXPUNGE
* Wait for unilateral response to be delivered
* GODT-409 Set flags have to replace all flags.
* GODT-531 Better way to add trusted certificate in macOS.
* Bumped golangci-lint to v1.29.0
* GODT-549 Check log file size more often to prevent huge log files.
* Bumped various dependencies:
    * andybalholm/cascadia v1.1.0 -> v1.2.0
    * emersion/go-imap-specialuse 20161227184202-ba031ced6a62 -> 20200722111535-598ff00e4075
    * emersion/go-sasl 20191210011802-430746ea8b9b -> 20200509203442-7bfe0ed36a21
    * github.com/go-resty/resty/v2 v2.2.0 -> v2.3.0
    * github.com/golang/mock v1.4.3 -> v1.4.4
    * github.com/google/go-cmp v0.4.0 -> v0.5.1
    * github.com/hashicorp/go-multierror v1.0.0 -> v1.1.0
    * github.com/jaytaylor/html2text 20200220170450-61d9dc4d7195 -> 20200412013138-3577fbdbcff7
    * github.com/jhillyerd/enmime v0.8.0 -> v0.8.1
    * github.com/keybase/go-keychain 20200218013740-86d4642e4ce2 -> 20200502122510-cda31fe0c86d
    * github.com/logrusorgru/aurora 20200102142835-e9ef32dff381 -> v2.0.3+incompatible
    * github.com/miekg/dns v1.1.29 -> v1.1.30
    * github.com/nsf/jsondiff 20190712045011-8443391ee9b6 -> 20200515183724-f29ed568f4ce
    * github.com/sirupsen/logrus v1.4.2 -> v1.6.0
    * github.com/stretchr/testify v1.5.1 -> v1.6.1
    * github.com/therecipe/qt 20200126204426-5074eb6d8c41 -> 20200701200531-7f61353ee73e
    * github.com/urfave/cli v1.22.3 -> v1.22.4
    * golang.org/x/net 20200301022130-244492dfa37a -> 20200707034311-ab3426394381
    * golang.org/x/text v0.3.2 -> v0.3.3
* Set first-start to false in bridge, not in frontend.
* GODT-400 Refactor sendingInfo.
* GODT-513 Update routes to API v4.
* GODT-551 Do not ignore errors during message flagging.
* GODT-380 Adding IE GUI to Bridge repo and building
    * BR: extend functionality of PopupDialog
    * BR: makefile APP_VERSION instead of BRIDGE_VERSION
    * BR: use common logs function for Qt
    * BR: change `go.progressDescription` to `string`
    * IE: Rounded button has fa-icon
    * IE: `Upgrade` → `Update`
    * IE: Moving `AccountModel` to `qt-common`
    * IE: Added `ReportBug` to `internal/importexport`
    * IE: Added event watch in GUI
    * IE: Removed `onLoginFinished`
    * Structure for transfer rules in QML
* GODT-213 Convert panics from message parser to error.
* GODT-585 Do not allow deleting messages from All Mail.

### Fixed
* GODT-655 Fix date picker with automatic Windows DST
* GODT-454 Fix send on closed channel when receiving unencrypted send confirmation from GUI.
* GODT-597 Duplicate sending when draft creation takes too long
* GODT-634 Hover on links in popups.



## [v1.3.x] Emma (v1.3.2 beta 2020-08-04, v1.3.3 beta 2020-08-06, v1.3.3 live 2020-08-12)

### Added
* GODT-554 Detect and notify about "bad certificate" IMAP TLS error.
* IMAP mailbox info update when new mailbox is created.
* GODT-72 Use ISO-8859-1 encoding if charset is not specified and it isn't UTF-8.

### Changed
* GODT-360 Detect charset embedded in html/xml.
* GODT-354 Do not label/unlabel messsages from `All Mail` folder.
* GODT-388 Support for both bridge and import/export credentials by package users.
* GODT-387 Store factory to make store optional.
* GODT-386 Renamed bridge to general users and keep bridge only for bridge stuff.
* GODT-312 Validate recipient emails in send before asking for their public keys.
* GODT-368 Bump docker-credential-helpers version.
* GODT-394 Don't check SMTP message send time in integration tests.
* GODT-280 Migrate to gopenpgp v2.
    * `Unlock()` call on pmapi-client unlocks both User keys and Address keys.
    * Salt is available via `AuthSalt()` method.
* GODT-308 Better user error message when request is canceled.
* GODT-162 User Agent does not contain bridge version, only client in format `client name/client version (os)`.
* GODT-258 Update go-imap to v1.
    * Fix UNSEEN to return sequence number of first unseen message and not count of unseen messages.
    * INBOX name is never quoted.
* GODT-204 `ClientManager`.
    * `Client` is now an interface; `client` is the concrete type.
    * `Client`s are only created by `ClientManager`.
    * Only one `Client` per userID exists at any given time; clients are reused.
    * Tokens are managed by `ClientManager` (`TokenManager` is removed).
    * `expiresAt` is no longer part of `Client`; token expiry and refreshing is handled by `ClientManager`.
    * Auths generated by clients during Auth/AuthRefresh are handled by `ClientManager` (which forwards them to `Bridge`).
    * `ClientManager` is the "one source of truth" for the host URL for all `Client`s.
    * Alternative Routing is enabled/disabled by `ClientManager`.
    * Logging out of `Clients` is handled/retried asynchronously by `ClientManager`.
* GODT-265 Alternative Routing v2 (more resiliant to short term connection drops).
* GODT-310 Alternative parsing of `References` header (old parsing probably malformed message IDs).
* GODT-320 Only report the same TLS issue once every 24 hours.
* GODT-468 Bump go-imap version to get fix for NIL client delimiter.
* GODT-465 Bump go-imap version to get fix for SELECT function.
* GODT-456 Bump bbolt version from 1.3.3 to 1.3.5 to get fixes for unsafe operations.

### Removed
* Dead code from `pkg/message`.

### Fixed
* GODT-356 Fix crash when removing account while mail client is fetching messages (regression from GODT-204).
* GODT-358 Bad timeouts with Alternative Routing.
* GODT-363 Drafts are not deleted when already created on webapp.
* GODT-390 Don't logout user if AuthRefresh fails because internet was off.
* GODT-341 Fixed flaky unittest for Store synchronization cooldown.
* Crash when failing to match necessary html element.
* Crash in message.combineParts when copying nil slice.
* Handle double charset better by using local ParseMediaType instead of mime.ParseMediaType.
* Don't remove log dir.
* GODT-422 Fix element not found (avoid listing credentials, prefer getting).
* GODT-404 Don't keep connections to proxy servers alive if user disables DoH.
* Ensure DoH is used at startup to load users for the initial auth.
* Issue causing deadlock when reloading users keys due to double-locking of a mutex.
* Correctly handle failure to unlock single key.
* GODT-479 Fix flaky integration tests.
* GODT-484 Fix infinite loop when decoding invalid 2231 charset
* GODT-267 Correctly detect if a message is a draft even if does not have DraftLabel.
* GODT-308 Reduce minimum read speed threshold to avoid issues with flaky internet.
* GODT-321 Changing address ordering would cause all messages to disappear in combined mode.
* GODT-129 Fix custom message PGP by using template.
* GODT-280 Don't assume contact keys are stored armored.
* GODT-427 Fix race condition in auth refresh that could cause user to be logged out.


## [v1.2.8] Donghai-fix-append  (beta 2020-06-XXX)

### Changed
* GODT-396 reduce number of EXISTS calls.
* GODT-143 Allow appending to Sent folder when sender matches account address.

### Fixed
* GODT-502 Fixed crash when unable to parse a message header.

## [v1.2.7] Donghai-fix-sync - (beta 2020-05-07 live 2020-04-20)

### Added
* IMAP extension MOVE with UIDPLUS support.
* IMAP extension Unselect.
* More logs about event loop activity.

### Changed
* GODT-313 Reduce number of synchronizations.
    * Do not trigger sync by counts.
    * Cooldown timer for sync retries.
    * Poll interval randomization.
* GODT-225 Do not send an EXISTS reposnse after EXPUNGE or when nothing changed (fixes rebuild of mailboxes in Outlook for Mac).
* GODT-165 Optimization of RebuildMailboxes.
* GODT-282 Completely delete old draft instead moving to trash when user updates draft.
* Adding DSN Sentry as build time parameter.
* GODT-124 Bump go-appdir from v1.0.0 to v1.1.0.
* CSB-72 Skip processing message update event if http statuscode is 422.

### Fixed
* Use correct binary name when finding location of addcert.scpt.


## [v1.2.6] Donghai - beta (2020-03-31)

### Added
* GODT-145 Support drafts.
    * GODT-211,GODT-231 fix updating subject and other fields.
    * GODT-220 Fix deleting drafts.
    * GODT-224 Fix creating draft from outlook without sender.
    * GODT-230,GODT-232 fix constructing sender address for drafts.
    * Sync already synced draft to newly created drafts mailbox.
    * Add Subject to EventMessageUpdated in pmapi.
* GODT-37 Add body and TLS handshake timeouts.
* GODT-90 Implement DOH (DNS over HTTPS) proxy.
* Noninteractive mode.


### Changed
* Bump version go-1.14.
* Bump dependencies:
| Repo                               | Old Version                        | New Version                        |
| github.com/0xAX/notificator        | v0.0.0-20161214074916-82e921414e03 | v0.0.0-20191016112426-3962a5ea8da1 |
| github.com/ProtonMail/go-autostart | v0.0.0-20171017232241-85d98b097aae | v0.0.0-20181114175602-c5272053443a |
| github.com/abiosoft/ishell         | v0.0.0-20171224170712-50251d04cb42 | v2.0.0+incompatible                |
| github.com/emersion/go-sasl        | v0.0.0-20161116183048-7e096a0a6197 | v0.0.0-20191210011802-430746ea8b9b |
| github.com/fatih/color             | v1.7.0                             | v1.9.0                             |
| github.com/golang/mock             | v1.4.2                             | v1.4.3                             |
| github.com/google/go-cmp           | v0.3.1                             | v0.4.0                             |
| github.com/jaytaylor/html2text     | v0.0.0-20190408195923-01ec452cbe43 | v0.0.0-20200220170450-61d9dc4d7195 |
| github.com/jhillyerd/enmime        | v0.7.0                             | v0.8.0                             |
| github.com/logrusorgru/aurora      | v0.0.0-20190803045625-94edacc10f9b | v0.0.0-20200102142835-e9ef32dff381 |
| github.com/skratchdot/open-golang  | v0.0.0-20160302144031-75fb7ed4208c | v0.0.0-20200116055534-eef842397966 |
| github.com/stretchr/testify        | v1.4.0                             | v1.5.1                             |
| github.com/therecipe/qt            | v0.0.0-20191022233421-590f404884c9 | v0.0.0-20200126204426-5074eb6d8c41 |
| github.com/urfave/cli              | v1.19.1                            | v1.22.3                            |

* Pkg/updates: closing File reader to avoid too many opened files during update.
* Created monorepo with bridge, pmapi, bridge utils, mime and srp.
    * One lint config for all packages and lint fixes in the code.
    * Fix tests for bridge utils to work on MacOS.
    * All tests use testify framework.
    * Processed TODOs or created issues.
    * Cleanup up comments.
* GODT-169 Reduce the number of keyring unlocks.
* CSB-40 return error instead of panic in credential store.
* #577 Avoid multiple send.
* GODT-39 Sync is paging per message ID with ability to continue after interrupted sync.
* Panic handler used in store for event loop and sync.
* GODT-109 Merge only 50 events into one.
* Use v1.0.16 of pmapi.
* GODT-236 Requests to /messages/{read,unread,delete,undelete,label,unlabel} are paged with up to 100 message IDs.

### Fixed
* GODT-227 Mitigate potential crash due to using a logged out pmapi client (proper fix to come in emma release).
* UserIDs were not checked when importing to Sent folder (affects copying from account1/sent to account2/sent).


## [v1.2.5] Charles - live (2020-03-11) beta (from 2020-02-10)

### Hotfix
* CSB-40 panic in credential store.
* Keyring unlocking locker.
* No panic on failed html parse.
* Too many open files.

### Added
* GODT-112 Migration of preferences from c10 to c11.
* GODT-100 Test for external internal ID when appending to Sent folder to return APPEND UID otherwise skip with no error.
* GODT-43 Connection troubleshooting modal.
* GODT-55 Uid support in fake api.
* GODT-88 Increase uid validity on switch mode.
* #951 Implementation of IMAP extension UIDPLUS.
* #964 New store package, see Changed section.

### Removed
* MOVE IMAP extension due to missing interaction with UIDPLUS.

### Changed
* GODT-88 Run mbox sync in parallel when switch password mode (re-init not user).
* GODT-95 Do not throw error when trying to create new mailbox in IMAP root.
* GODT-75 Do not fail on unlabel inside delete.
* #1095 always delete IMAP USER including wrong pasword.
* Unique pmapi client userID (including #1098).
* Using go.enmime@v0.6.1 snapshot.
* Better detection of non-auth-error.
* Reset `hasAuthChannel` during logout for proper login functionality (set up auth channel and unlock keys).
* Allow `APPEND` messages without parsable email address in sender field.
* #1060 avoid `Append` after internal message ID was found and message was copyed to mailbox using `MessageLabel`.
* #1049 Basic usage of store in SMTP package to poll event loop during sending message.
* #1050 pollNow waits for events to be processed.
* #1047 Fix fetch of empty mailbox.
* #1046 Fix removing mailbox counts.
* #1048 For any message build error return custom message.
* When event loop exits with error it logs out user from Bridge.
* #953 #984 First label messages before unlabeling when moving messages.
* Fixes after refactor:
    * Slight memory optimization.
    * #1043 do not stuck in loop for updating message which does not exist anywhere anymore.
    * #1034 fix UID dynamic range for empty list.
    * Fix of sequence number in IMAP IDLE expunge during deleting messages.
    * #1030 #1028 Fix some crashes and bad auths.
    * #953 #984 label messages first during moving them.
* #964 (and #769,#899,#918,#930,#931,#949) refactor of IMAP.
    * Fix of sequence number in IMAP IDLE expunge during deleting messages.
    * Fix not-returning empty result for UID dynamic range as said in RFC.
    * Separated IMAP to store and IMAP.
    * Store is responsible for everything about db and calls to pmapi, including event loop, sync, address mode.
    * IMAP is responsible only for IMAP interfaces.
    * Event loop is only one per ProtonMail account (instead of one per alias)
    * It also means only one database per account (instead of one per address)
    * Changing address mode is not destroying database, only buckets with IDs mapping (keeping metadata for account)
    * Before first sync we set event ID so we will not miss changes happening during sync.
    * Thanks to previous point we are not starting new sync when we finish first one because of unprocessed events.
    * Sync is not blocking event loop (user can get new messages even during sync)
    * Sync is not blocking reading operations (user can list mailboxes even before first sync is done)
    * Sync is not blocking writing operations such as mark messages read/unread and so on.
    * Most operations have to be passed to API and only event loop is writing them to the database.
    * Avoid relying on counts API endpoint; use event counts as much as possible.
    * Separate function for storing message content type and header into database.
    * Sequence number optimised for last item in mailbox.
    * Allow sending IMAP idle update to timeout to avoid blocking bridge.
    * Synchronisation will create a label if not yet present.
    * Labels and Folders (including system folders) are stored in DB together with their counts for offline read-out.
    * AddressIDs for all user addresses are stored in DB.
    * IMAP updates channel is set when an IMAP client connects (and IMAP updates are dropped until then)
    * DB keeps track of address mode (split/combined)
* Event loop starts as soon as user is initialised (i.e. logged in), not just when imap is connected.
* Use pmapi v1.0.13.
* Logout user if initialisation fails.
* Send UserRefreshEvent on user login and logout.
* Use godog v0.8.0 under new name 'cucumber' (instead of DATA-DOG).

### Fixed
* #1057 Logging in to an already logged in user would display unrelated error "invalid mailbox password".
* #1056 Changing mailbox password sometimes didn't log out user.
* #1066 Split address mode can not work when credentials store is cleared.
* #1071 Bridge can think it is in combined mode when actually it's in split mode.
* Missing `enmime` dependency.
* Issue where a failed sync was not attempted again.
* Removing an address would crash bridge.
* #1087 Accounts with capital letters could not be added.
* #1087 Inactive addresses were not filtered out of the store.
* #1087 Unlock with correct key if message is sent to alias and not primary (aka original) address.
* #1109 Receiving an event referencing an address that isn't present could crash bridge.
* Avoid concurrent map writes in imap backend.
* GODT-103 User keys were not unlocked later if they were not unlocked during startup.


## [v1.2.4] Brooklyn beta (2019-12-16)

### Added
* #976: fix slow authentication.
    * Server security setting in info (GUI, CLI).
    * Default SSL for SMTP based on Mac version.
    * GUI/CLI items to controls SMTP security setup.
    * Set new security and restart.

### Changed
* #961 Timeouts for go-pmapi client with http.Transport.
* Event poll with no change will hang forever. Using separate goroutine and timeout instead of proper fix (will be in refactor).
* Fixed an issue where entering an in-use port multiple times via the CLI would make bridge use it.
* Update therecipe/qt and Qt to 5.13.

## [v1.2.3] Akashi - live (2019-11-05) beta (2019-10-22)

### Added
* #963 report first-start metric with bridge version.
* #941 report new-login metric, report daily heartbeat.
* #921 remote key lookup via Web Key Directory (WKD).
* #919 TLS issue notification in CLI.

### Changed
* #769 #930 #931 #949 Syncing messages and fetching message and attachments in parallel with five workers.
* #956 #741 update keychain.
* Re-download and re-unlock user keyring when addresses are changed.
* #944 Ugrade go-pmapi dependency to v1.0.4 to support phase one of the key migration.
* #683 Password rehides each time password entry screen is shown.
* Import-Export#219 fix double parameter definition.
* Upgrade go-pm-bridge-utils dependency to v1.0.1.
* #935 Fix wrong download link for linux updates.
* #952 fix error when sending mail with only BCC recipients (use empty slice instead of nil slice).
* Refactor `generateSendingInfo` to simplify logic; add test for this method.
* Generate code-coverage report with `make code-coverage`.
* #942 fix focus window with logout message when trying to connect from the client.
* Do not use panic for second instance.
* #928 do not hide 'no keychain' dialog when upgrade is needed.
* Sending `NO` for errors while `FETCH`.
* #899 Upgrade from Bolt to BBolt.
* Upgrade to gopenpgp.
* Bridge utils in own repository.
* Code made compatible with name changes in go-pmapi.


## [v1.2.2] - beta and live 2019-09-06

### Changed
* User compare case insensitive.

## [v1.2.1] - beta and live 2019-09-05

### Changed
* #924 fix start of bridge without internet connection.

## [v1.2.0] - beta 2019-08-22

### Added
* #903 added http.Client timeout to not hang out forever.
* Closing body after checking internet connection.
* Pedantic lint for bridgeUtils.
* Selected events are buffered and emited again when frontend loop is ready.
* #890 implemented 2FA endpoint (auth split).
* #888 TLS Cert.
    * Error bar and modal with explanation in GUI.
    * Signal to show error.
    * Add pinning to bridge (only for live API builds).
* #887 #883:
 * Wait before clearing data.
 * Configer which provides pmapi.ClientConfig and app directories.
* #861 restart after clear data.
* Panic handler for all goroutines.
* CD for linux.
* #798.
    * Check counts after sync.
    * Update counts in all mailboxes after sync.
    * `db.Mailbox.RemoveMissing`, `db.Mailbox.PutMany`.
    * `util.NotImplemented`.
    * Tests for sync.
* Bridge core tests:
    * Introduced interfaces: `pmapiClienterFactory`, `pmapiClienter`, `credentialStorer`.
    * Automatic mock generation for  `listener.Listener`, `bridge.pmapiClienter`, `bridge.credentialStorer`.
* #818 REFACTOR: see doc/code-structure.md.
    * Tests for bridge core & utils.
    * Update user before `GetQuota`.
    * Http bridge API.
* Bridge core tests:
    * Introduced interfaces: `pmapiClienterFactory`, `pmapiClienter`, `credentialStorer`.
    * Automatic mock generation for  `listener.Listener`, `bridge.pmapiClienter`, `bridge.credentialStorer`.
* #774 start initialization with sync immediately after login.

### Removed
* Using `PutMeta` for DB to not rewrite header and size.
* `Timeout` for connection (keep only `DialTimeout`).
* #798 `imapMailbox.sync`.
* #818 REFACTOR: see doc/code-structure.md.
    * Bridge global functions `GetAuth`, `GetAuthInfo`, `GetUserSettings` (using member functions of `pmapi.Client` instead).
    * `backend.setCache`: not used.
    * IMAP extension for `XSTOP` and `XFOCUS`.
    * Keychain `Disconnected` is not used,  deleting directly (not using hide).
   * `apiIdFrom(uid bool, id uint32)`, `apiIdRangeFromSeq(uid bool, seq imap.Seq)`: not used.
   * `server/dial.go` not used.
   * Util `CustomMessage`, `StartTicker` not used.

### Changed
* Check before first even sync.
* Do sync in parallel from events.
* Closing event loop by CloseConnectionEvent.
* Allow client to log in with address only.
* Fix IMAP users lock.
* #646 download headers when needed for first time.
* #895 fix of parsing address list.
* #844 do not spam GUI with logout events & sleep after bad login attempt from the client.
* #887 #883 #898 #902 logout account from API and all IMAP connections before clearing cache for account.
* #882 unassign PMAPI client after logout and force to run garbage collector.
* #880, #884, #885, #886 fix of informing user about outgoing non-encrypted e-mail.
* #838 `Sirupsen` -> `sirupsen`.
* #893 save panic report file everytime.
* #880 fix of informing user about outgoing non-encrypted e-mail.
* Fix aliases in split mode.
* Fix decrypted data in log notification.
* #471 fix of using font awesome in regular text.
* `SearchMessage` all IDs from DB not depends on `totalOnAPI`.
* #798 populate efficiently.
    * Improved `imap.db.mailbox.Counts()`.
    * `mbox.total,unread` -> `mbox.totalOnAPI,unreadOnAPI`.
    * Always show DB status (even for `IDLE` updates).
    * `imapUser.sync` now takes `labelID` as parameter.
    * Split population by 1000 messages.
    * `db.User.put(msgs,keepCache)` is used in sync to not overwrite `msg.Size` and `msg.Header` in DB.
    * Separate sync function from `backend.labelMailbox` class.
    * `UidNext` uses bolt sequence value instead of cursor position.
* `util.tests.go` moved to `bridgeUtils`.
* #471 fix of using font awesome in regular text.
* #818 REFACTOR: see doc/code-structure.md.
    * No global states/variables anymore.
    * Code separated from one big package into smaller packages (bridge core, utils, IMAP, SMTP, API).
    * Bridge core completely refactored - core should be API over credentials store and PMAPI.
    * Configuration and preferences are on one place; passed as dependency to all packages.
    * Bridge utils separated from the rest of the bridge code to be used in Import/Export.
    * Many channels converted into one listener which can register listeners and emit events to them.
    * Each package is ready to be used with interfaces for possibility of mocking.
    * Removed IMAP extension XFOCUS, used bridge local API instead.
    * Removed IMAP extension XSTOP.
    * Sentry is not used in dev environment.
    * Logs are not cleared after start, clearing is triggered by `watchLogFileSize()` instead.
    * Log path changed one folder level up i.e. from `.../protonmail/bridge/c10` to `.../protonmail/bridge`.
    * Always cleared malformed keychain records.
    * Set credentials version on each `Put`.
    * `util.WriteHeader` -> `imap.writeHeader`.
    * Save `message.ExternalID` for every client not just AppleMail.
    * Server errors reported to frontend by common event listener.
* Handle logout in event loop.


## [v1.1.6] - 2019-07-09 (beta 2019-07-01)

### Added
* #841 assume text/plain during sending e-mails when missing content type.
* #805 list the new package links in upgrade dialog for linux.
* #802 report the list errors to sentry.
* #508 content related header fields for mail are saved in DB inside `msg.Header`.
* #508 `doNotCacheError` to decide whether to rebuild message.
* CI with lint check.
* Build flag `nogui`.
* Dummy html interface.

### Removed
* #508 content type rewrite on `GetHeader`.
* #508 content type on custom message.

### Changed
* #854 avoid `nil` header and bodystructure on fail (as regression of #508).
* Sanitize version in json file.
* #850 keep correct main and body headers for import (as regression of #508).
* #841 choose parent ID only when there is exactly one message with external ID.
* #811 #proton/backend-communication#11 go-pmapi!57 uid fixed.
* Update Qt 5.11.3 to 5.12.0.
* Using gomodules instead of glide.
* #508 use MIMEType and attachments to choose correct `Content-Type`.
* #508 custom message replaces body before header is created.
* #508 main header has `Content-Type` only after message was fully fetched.
* #770 ignore empty key from data card and support multiple keys for contacts.
* Build tags for simpler build of beta and QA builds.
* Lint corrections.


## [v1.1.5] - 2019-05-23 (beta 2019-05-23, 2019-05-16)

### Changed
* Fix custom message format.
* #802 acumulated long lines while parsing body structure.
* Process `AddressEvent` before `MessageEvent`.
* #791 updated crypto: fix wrong signature format.
* #793 fix returning size.
* #706 improved internet connection checking.
* #771 updated raven, crypto, pmapi.
* #792 use `INFO` as basic log level.
* Only one crash from second instance.
* During event `MessageID` in log as field.

## [v1.1.4 live] - 2019-04-10 (beta 2019-04-05, 2019-03-27)

### Added
* Address with port to IMAP debug.
* #750 `backend/events.Manager.LastEvent`.
* #750 `backend.user.areAllEventsProcessed`.
* #750 Wait with message events until all related mailboxes are synchronized.
* Restart limit to 10.
* Release string to raven.

### Changed
* #748 when charset missing assume utf8 and check the validity.
* #750 before sync check that events are uptodate, if not poll events instead of sync.
* Use pmapi with support of decrypted access token.
* #750 Status is using DB status instead of API.
* Format panic error as string instead of struct dump.
* Validity of local certificate to increased to 20 years.

### Removed
* #750 Synchronization after 450 messages.

## [v1.1.3] - 2019-03-04

### Added
* Sentry crash reporting in main.
* Program arguments to turn of CPU and memory profiling.
* Full version of program visible on release notes.

### Changed
* #720 only one concurent DB sync.
* #720 sync every 3 pages.
* #512 extending list of charsets go-pm-mime!4.

## [v1.1.2] - beta only 2019-02-21

### Changed
* #512 fail on unknown charset.
* #729 #733 visitor for MIME parsing.

## [v1.1.1] - 2019-02-11
### Added
* #671 include `name` param in attachment `Content-Type` (in addition to `Content-Disposition` param `filename`).
* #671 do not include content headers for section requests e.g. `BODY.PEEK[2]`.
* Version info checks for newer version (do not show dialog when older is online).
* #592 new header `X-Pm-ConversationID-Id` and also added to `References`.
* #666 invoke `panic` while adding account `jakubqa+crash@protonmail.com`.
* #592 new header fields `X-Pm-Date` storing m.Time and `X-Pm-External-Id` storing m.ExternalID.
* #484 search criteria `Unkeyword` support.

### Changed
* Fix srp modulus issue with new `ProtonMail/crypto`.
* Generate version files from main file.
* Be able to set update set on build.
* #597 check on start that certificat will be still valid after one month and generate new cert if not.
* #597 extended certificate validity to 2 years.
* Copyright 2019.
* Exclude `protontech` repos from credits.
* Refactor of `go-pmapi`, `go-pm-crypto`, `go-pm-mime` and `go-srp`.
* Re-signed pubkey key.
* Version, revision and build time is set in main.
* #666 use `bytes.Reader` instead of `bytes.Buffer`.
* #666 clear unused buffers in body structure map.
* No API request for fetch `body[header]`.
* Added crash file counter to pass log tests.
* #484 search fully relies on DB information (no need to reach API).
* #592 `parsingHeader` allows negative time (before 1.1.1970).
* #592 add original header first and then rewrite.
* #592 `Message-Id` rewritten only if not present.
* #592 rename `X-Internal-Id` to `X-Pm-Internal-Id`.
* #592 internal references are added only when not present already.
* #592 field `Date` changed to m.Time only when wrong format or missing `Date`.
* #645 pmapi#26 `Message.Flags` instead of `IsEncrypted`, `Type`, `IsReplied`, `IsRepliedAll`, `IsForwarded`.
* DB: do not allow to put Body or Attachements to db.
* #574 SMTP: can now send more than one email.
* #671 Verbosity levels: `debug` (only bridge), `debug-client` (bridge and client communication), `debug-server` (bridge, whole SMTP/IMAP communication).
* #644 Return rfc.size 0 or correct size of fetched body (stored in DB).
* #671 API requests URI in debug logs.
* #625 Fix search results for Flagged and Unflagged.
* Draft optimization fetch header.
* #656 Fix sending of calendar invite on Outlook on MacOS.
* #46 Allowed to run multiple instances, once per user.

### Removed
* Makefile clean up old deploy code.

### Release notes
* Support multiple Bridge instances running in parallel (one per user).

### Fixed bugs
* SMTP stays authenticated after sent message.
* Reduce memory, processor and number of API calls.

## [v1.1.0] - 2018-10-22

### Removed
* `go-pmapi.Config.ClientSecret`.
* `go-pmapi.PublicKey.Send`.
* Program argument `main`.
* `backend.getMIMEMessageBodySection` (use `message.BodySection`).
* `backend.getSize` (use `message.BodySection`).

### Added
* IMAP server: more info when write/send/flush error occurs #648.
* Linux package paths inside version-json.
* Draggable popup windows for outgoing non-encrypted message #519.
* Pmapi able to receive plain accessToken go-pmapi#23 #604.
* DB debug switch.
* Clearing message cache when db is cleared.
* Debug string to tests.
* Mime tree section parsing and test.
* Start ticker.
* Dump DB status.
* `backend.ApplicationOutdated()` mechanism: once triggered logout all email clients. On try to login say _application outdated_.
* Force upgrade event (send from event loop).
* New systray with error symbol (used in mac for force update).
* Test for upgrade.
* GUI for upgrade.
* Add native upgrade to updates.
* Dial timeout client.
* Custom `copyRecursively` function.
* When there is fresh version on start show release notes.
* Keychain helper using GNU pass.
* Error message on missing keychain.

### Changed
* Imap `SEARCH` loops until all messages are listed #581.
* Cached message timestamp is renewed on load.
* Message cache ID is userID+messageID.
* Private cache and added bodystructure.
* Remove addresses from `m.ToList` that were not requested in SMTP `TO`.
* IsFirstStart setup before loading Gui. Set it to false right after (don't wait till quit).
* Check `eventMessage` not nil before address check.
* `util.EventChannel` refactor: `SendEvent`->`Send` and new `SendEvent(EventCode)`.
* Information bar keeps on once app is outdated.
* Error dialog for upgrade has option for force upgrade.
* IsFirstStart setup before loading Gui. Set false right after (don't wait till quit).
* Pmapi: access token decrypted only if needed.
* Move `updates` from `frontend` to `util`.
* Move `CheckInternetConnection()` to `util`.
* Makefile clean up and change scripts for building.
* Reorganized updates.
* Start with new versioning.

          1.1.0
          | | `--- bug fix number (internal, irregular, beta relases)
          | `----- minor version (features, release once per month, live release, milestones)
          `------- major version (big changes, once per year, breaking changes, api force upgrade)

* Upgrade restart option in qt-frontend.
* GOOS save functions.
* Windows update procedure.
* Darwin update procedure.
* `zip` replaced by `tgz`.
* Using move instead of write truncated.
* Linux dependencies (pass and gnome-keychain optional).
* `Store.helper` -> `Store.secrets`.

### Release notes
* New self-update procedure.
* Changed restarting mechanism.
* Support for GNU pass for linux.
* Various GUI improvements.

### Fixed bugs
* RFC complaint SEARCH and FETCH responses.
* Additional synchronization of mail database.


## [v1.0.6 silent] - 2018-08-23
### Added
* New svg icon in linux package.

## [v1.0.6] - 2018-08-09

### Added
* `backend.GetUserSettings()`.

### Changed
* Related to Desktop-Bridge#561.
* Api flag to build scripts.
* `BodyKey` and `AttachmentKey` contains `Key` and `Algorithm`.
* `event.User.Addresses` -> `event.Addresses`.
* `user.Addresses` -> `client.Addresses()`.
* Typos and fixes.
* Pmapi update.
* `backend.configClient` -> `backend.authClient`.
* `auth.Uid` -> `auth.Uid()`.
* `keyRingForAddress()` -> `Client.KeyRingForAddressID()`.
* `Message.IsRead` -> `Message.Unread`.
* `pmapi.User.Unlock()` -> `pmapi.Client.UnlockAddresses()`.
* `TwoFactor` -> `HasTwoFactor()` and `PasswordMode` -> `HasMailboxPassword()`.
* Icon to match ImportExport.


### Release notes
* Removed deprecated API routes.

### Fixed bugs
* Frequent Thunderbird timeout.
* SMTP requests not case-sensitive.

## [v1.0.5] - 2018-07-12

### Added
* UpdateCurrentAgent from lastMailClient.
* Current OS.
* Use Qt to set nice OS with version.
* All `client.Do` errors are interpreted as connection issue.
* Moved to internal gitlab.
* Typo `frontend-qml`.
* Better message for case when server is not reacheable.
* Setting 1min timeout to IMAP connection.

### Changed
* Password: click2show, click2hide.
* Notification in bug report window.
* Less frequent version check.
* Closing ticker.

### Removed
* Sockets and unused libraries.

### Release notes
* Improved response of IMAP server.
* Sending requests with client information.
* Less frequent notification about new version.

### Fixed bugs
* Support of Outlook calendar event format.
* Too many opened file descriptors issue.
* Fixed 7bit MIME issue while sending.


## [v1.0.4] - 2018-05-15

### Changed
* Version files available at both download and static.
* MIME `text/calendar` are parsed as attachment.
* UserID as identifier in keychain and pmapi token.
* Keychain format and function refactor.
* Create crash file on panic with full trace.
* Clear old data only in main process (no double keychain typing).
* Create label udpate API route.
* Selectable text in release notes.

### Added
* Support sending to external PGP recipients.
* Return error codes: `0: Ok`, `2: Frontend crashed`, `3: Bridge already running`, `4: Uknown argument`, `42: Restart application`.

### Release notes
* Support of encryption to external PGP recipients using contacts created on beta.protonmail.com (see https://protonmail.com/blog/pgp-vulnerability-efail/ to understand the vulnerabilities that may be associated with sending to other PGP clients).
* Notification that outgoing email will be delivered as non-encrypted.
* NOTE: Due to a change of the keychain format, you will need to add your account(s) to the Bridge after installing this version.

### Bugs fixed
* Support accounts with same user names.
* Support sending vCalendar event.

## [v1.0.3] - 2018-03-26
* All from silent updates plus following.

### Changed
* Okay -> "Remind me later".
* Imported message with `text/html` body was imported as `text/plain`.
* Reload cache when labeling Seen/Unseen.
* Merge with Import-Export branch.
    * Inheritable Bug report window.
    * Common functions: WriteHeader (parse PM mail) and CustomMessage (when incorrect keys).
    * Updates refactor.
    * Bug report window.
    * Checkbox and with label (only I/E).
    * Error dialog and Info tooltip (only I/E).
    * Add user modal formating (colors, text).
    * Account view style.
    * Input box style (used in bug report).
    * Input field style (used in add account and change port).
    * Added style variables for I/E.
    * Tab button style.
    * Window bar style and functionality (closing / minimize window).

### Release notes
* Improved responsiveness in the UI.

### Fixed bugs
* Fixed some formatting issues with imports.
* Fixed port changing via CLI.

## Silent update - 2018-03-13

### Changed
* Remove firewall error message.


## [v1.0.2] - 2018-03-12
* All from silent updates plus following.

### Added
* UTF-7 support.
* Message when communication between bridge and email client is blocked by firewall (Windows only).

### Changed
* Added gnome-keyring dejavu fonts into linux dependency.
* Corrected parentID when reply/forward: taken from `protonmail.internalid` reference.
* Update user object in backend after unlock to apply address changes.

### Release notes
* UTF7 encoding support for older imported emails.

### Fixed bugs
* Fixed issues with conversation threading.
* Support for multiple "ReplyTo" addresses.
* Fixed issue where some address updates would not register immediately.



## [v1.0.1-4 (linux only)] Silent deploy - 2018-02-28

### Changed
* More similar look of window title bar to Windows 10 style.
* Qt 5.10 Button Controls 2 conflict (`icon`->`iconText`).

### Added
* Linux default font.
* Multiple reply-to addresses support (also API).
* Command line interface.
* Credits are generated automatically from glide.lock.
* Created script to build linux packages (dep,rpm,PKGBUILD).
* Correct config folders with env variable `$XDG_CONFIG_HOME`.

### Fixed bugs
* Clearing global cache.
* Default linux font problems.
* Support Reply-To multiple addresses.

### Release notes
* Improved visual appearance for win and linux.



## [v1.0.1] Silent deploy - 2017-12-30

### Changed
* Fixed bug with parsing address list (CC became BCC).



## [v1.0.1] - 2017-12-20

### Added
* When current log file is more than 10MB open new one, checked every 15min.
* Keep only last three log files including current one, triggered every start and when switching log files.
* Translation context.
* Accessibility objects for button and static text.
* All objects are accessible including focus scope for modals and messages.
* Automatically fill the email client in bug report form.
* Catch corrupted MacOS keychain error and show the link to FAQ.
* Unlabel message.
* Update emptying and filtering routes.
* Parse the address comment as defined in RFC.

### Changed
* Default log level set to Warning.
* Info logs during adding account and connecting client promoted to warning level.
* Log only when email client was changed (previously logged on every assign).
* Force upgrade bubble notification only when requested by API.
* Don't show warning systray icon when "You have then newest version!" bubble message is showed.
* Header date format  RFC822Z -> RFC1123Z.
* IMAP ID and QUOTA responses forced to use quoted strings (fixing SparkMail issue).
* Avoid AddressChanged bubble when no address was changed.

### Release notes
* Reduced log file size and log file history.
* Accessibility support for MacOS VoiceOver and Windows Narrator.
* Improved notification system.
* Supported imports with older address format.



## [v1.0.0] - 2017-12-06

### Added
* Encoding support of message body, title items, attachment name, for all standard charsets.
* Force update API message handled as new version event.

### Changed
* Refactor `bridge-qtfronted` -> `frontend`.
* Only one main file and basic support of CLI (not finished).
* Common QML package `ProtonUI`, which is used by `BridgeUI` and `ImportExportUI`.
* ChangedUser signal contain address and event type to distinguish between logout, internet off/on, address_change.
* API address changed event handled gracefully (if not possible, logout).
* Update mac keychain (should resolve problem with adding new account to bridge, NOT CONFIRMED).
* Solved hanging GUI on keychain error (should solve all win-7, no-gui errors).
* New systray icons for Mac (black and white no background).
* GUI cosmetics:
    * "Click here to start" triangle position.
    * Wrong cursor type on link.
    * Create main window before notification.

### Release notes
* Better notification when new version is needed or when account address is changed.
* Encoding support for the standard charsets.
* Improved visual appearance.

### Fixed bugs
* Fixed missing GUI for Windows with empty keychain.



## Changelog format
* Changelog [format](http://keepachangelog.com/en/1.0.0/).

### Guiding Principles
* Changelogs are for humans, not machines.
* There should be an entry for every single version.
* The same types of changes should be grouped.
* Versions and sections should be linkable.
* The latest version comes first.
* The release date of each version is displayed.
* Mention whether you follow Semantic Versioning.

### Types of changes
* `Added` for new features.
* `Changed` for changes in existing functionality.
* `Deprecated` for soon-to-be removed features.
* `Removed` for now removed features.
* `Fixed` for any bug fixes.
* `Security` in case of vulnerabilities.
* Additional for in app release notes.
    * `Release notes` in case of vulnerabilities.
    * `Fixed bugs` in case of vulnerabilities.

