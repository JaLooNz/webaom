# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.2.0] - 2025-08-02
### Add
- Added Launch4j to build WebAOM.exe
- Migrate to Gradle project

## [2.1.0] - 2023-04-09
### Fixed
- More code cleanup using stricter Java compiler settings.
- Updated Jacksum classes from v1.5.0 to v3.5.0.
- Removed gnu crypto classes in favour of pulling them in via the latest gnu-crypto dependency (v2.0.1)
- Removed the bitzi TigerTree class in favour of the Jacksum version.
- Removed the twmacinta fast MD5 hash classes in favour of the built-in JRE/JDK MD5 hash. The modern version of the MD5 hash in the JRE/JDK is slightly faster than the old fast MD5 version.
- Fix various potential resource leaks.

## [2.0.1] - 2023-04-07
### Fixed
- Update Pom file to build jar file with dependencies.

## [2.0.0] - 2023-04-07
### Fixed
- Replaced the MySQL and PostgreSQL DB support with SQLite which means that this version is incompatible with all previous versions.
- Major code refactor and cleanup to target Java 17.
- The GUI look and feel will now default to the system look and feel.
*Requires Java 17

## [1.19] - 2006-11-20
### Fixed
- 'year' parsing exception
- 'I' test (defined) for 'ver', meaning true if greater than 1
- db update for postgresql users
- extra k printed in ed2k hash @ info window
- stored order of columns in 'Jobs'
- some minor bugs

### Added
- 'ASSUME [SPECIAL] {int}' rule. For padding epno when total is unknown (always true for specials)
- english episode name to 'E' test
- column 'len' to 'Jobs'. (Length in sec)
- regexp test to E(pisode) test
- 'TRUNCATE {int max len}' to rules. Will truncate file name if necessary
- two columns in 'Job' list; mds, mda (missing data flags)
- job-list-column-customization to options file
- option 'Auto save'; save options to disk without asking
- support for avinfo.dll ([[Avdump]], put the dll somewhere it will be found)
- filtering in 'Jobs' view
- selectable titles in 'Alt' view (romaji,kanji,english)
- 'Path regexp' to options file
- 'Load db on startup' and 'Auto log' options
- 'Remove from mylist' to job menu
- 'Set fid (force)' to job menu. For self edited files. (Hashing is still required.)
- support for encrypted and compressed communication
- support for private/local mysql database
- support for path 'P', extension 'E' and genre 'N' in tests
- support for ELSE IF and RETURN in scripts
- coloring, sorting, aid and gid columns, in job table
- new file info frame, html style
- Pause, Restore name, Rehash, Identify, Add to mylist, Set Finished, Set Folder to job popup menu
- support for postgre database
- support for import and export of data
- 'Edit Folder Path' to job menu
- 'Log to file' option
- support for gzip (parser was broken)
- support for dub language (D) and sub language (L) in tests
- tags %kan = Jap. Kanji Title and %eng = English Title
- support for hentai (needs to be enabled in profile)
- possibility to save options
- new rule system: rename and move files based on file info
- Tiger Tree Hash
- possibility to choose each hash type
- extensive hashing. MD5, SHA-1 and CRC32
- connection options
- connection check

### Changed
- 'I' test "syntax"; I(%eng) -> I(eng)
- 'Show Info' bug (thx to TechnoMage)
- back to 1.4 compliance level
- keep-alive is now enabled also when nat is not detected (every 30 min)
- job colors; red -> corrupted, gray -> missing (not found)
- options file encoding to utf8
- Only Java 1.5 support from now
- massive internal changes
- improved support for large font sizes
- table row height
- font in popup menu
- To change the 'Log' font; press DELETE, edit header, press ok
- To customize the file info page; extract 'file.htm' from the jar, edit, save as '.webaom.htm' in your home folder
- Job-filter-combo-box -> check boxes. (suggested by weedy)
- 'Alt' view. V3: path exlude, improved %, added M(issing) col, secondary sort
- 'Alt' view. V2: size column, FNF filter, 3 selectable structures;
::Anime-File, Anime-Episode-File, Anime-Group-File, Anime-Folder-File
- change in file handler: Will not try to add files that are locked (used by another process)
- change in rule system. Scripting. Textfield instead of table
- changes in debug window
- changes in gui and underlying system:
 -File lists replaced with one table.
 -Rename option panel replaced with Rules tab.
 -Start and Stop buttons replaced with toggle buttons for hasher thread and communication thread.
- changes in the status and logging system
- changes in option tab
- changes in the error handler
- bugfix: Applet crash with Opera and Firefox

## [1.18b] - 2006-07-21
### Fixed
- 'Show Info' bug (thx to TechnoMage)
- bug in !mystats (thx to GuntherDW)

### Added
- more keyboard mappings (and changed E to X)
- more tool tips and changed some text to make WebAOM more understandable
- 'Cancel' button to the 'The options has changed' dialog
- Rules->Rename/Moving-radio-buttons bug (thx to Kei-kun)
- joint eps bug; java.lang.NumberFormatException
- drop and ctrl-v support to 'Jobs' table
- selectable columns in 'Job' view. (Right click table header.)
- new job colors; red -> corrupted, gray -> missing (not found)
- password (and apipass) storage option
- 'Alt' key mappings to 'Jobs' too
- 'Remove from mylist' to job menu
- a bunch of key mappings to 'Alt'; afgmwe, left, right, and enter
- key mapping q to 'File Info' window (close)
- support for encrypted and compressed communication
- support for postgre database
- updated the database definition and included it in jar
- support for import and export of data
- 'Edit Folder Path' to job menu
- 'Set fid (force)' to job menu. For self edited files. (Hashing is still required.)
- change: 3 timeouts -> lockdown, new: unlocks after 15 min.
- fixed minor bug in pinger when port is out of range
- support for encrypted and compressed communication
- fixed minor epno padding bug
- fixed "Data too long for column 'audio' at row 1"
- fixed (hopefully) out of mem error when adding large folders
- change: Login Dialog doesn't show up at startup anymore
- minor changes in gui

## [1.18] - 2006-07-14
### Fixed
- bug in !mystats (thx to GuntherDW)
- some minor bugs

### Added
- more tool tips and changed some text to make WebAOM more understandable
- 'Cancel' button to the 'The options has changed' dialog
- Rules->Rename/Moving-radio-buttons bug (thx to Kei-kun)
- joint eps bug; java.lang.NumberFormatException
- drop and ctrl-v support to 'Jobs' table
- selectable columns in 'Job' view. (Right click table header.)
- change: Job-filter-combo-box -> check boxes. (suggested by weedy)
- change: Keep-alive is now enabled also when nat is not detected (every 30 min)
- fixed bug in keep-alive code
- minor ui update bug in 'Alt'
- sorting bug in 'Jobs' when changing filter
- new job colors; red -> corrupted, gray -> missing (not found)
- change: options file encoding to utf8
- Only Java 1.5 support from now
- massive internal changes
- support for avinfo.dll ([[Avdump]], put the dll somewhere it will be found)
- improved support for large font sizes
**Fixed table row height.
**Fixed font in popup menu.
**To change the 'Log' font; press DELETE, edit header, press ok.
**To customize the file info page; extract 'file.htm' from the jar, edit, save as '.webaom.htm' in your home folder.
- filtering in 'Jobs' view
- selectable titles in 'Alt' view (romaji,kanji,english)
- minor UI changes

## [1.17] - 2006-05-07
### Fixed
- bug in !mystats (thx to GuntherDW)
- NullPointerEx on 'Add to mylist' when file is unknown, thx to egg
- some minor bugs

### Added
- 'Edit File Name' to pop up menu
- more tool tips and changed some text to make WebAOM more understandable
- 'Cancel' button to the 'The options has changed' dialog
- Rules->Rename/Moving-radio-buttons bug (thx to Kei-kun)
- joint eps bug; java.lang.NumberFormatException
- drop and ctrl-v support to 'Jobs' table
- selectable columns in 'Job' view. (Right click table header.)
- change: Job-filter-combo-box -> check boxes. (suggested by weedy)
- change: Keep-alive is now enabled also when nat is not detected (every 30 min)
- fixed bug in keep-alive code
- minor ui update bug in 'Alt'
- sorting bug in 'Jobs' when changing filter
- new job colors; red -> corrupted, gray -> missing (not found)
- change: options file encoding to utf8
- Only Java 1.5 support from now
- massive internal changes
- support for avinfo.dll ([[Avdump]], put the dll somewhere it will be found)
- improved support for large font sizes
**Fixed table row height.
**Fixed font in popup menu.
**To change the 'Log' font; press DELETE, edit header, press ok.
**To customize the file info page; extract 'file.htm' from the jar, edit, save as '.webaom.htm' in your home folder.
- filtering in 'Jobs' view
- selectable titles in 'Alt' view (romaji,kanji,english)
- 'Path regexp' to options file
- 'Load db on startup' and 'Auto log' options
- hidden feature: F9 resets application
- updated 'Alt' view. V3: path exlude, improved %, added M(issing) col, secondary sort
- password (and apipass) storage option
- 'Alt' key mappings to 'Jobs' too
- code cleanup
- 'Remove from mylist' to job menu
- a bunch of key mappings to 'Alt'; afgmwe, left, right, and enter
- key mapping q to 'File Info' window (close)
- updated 'Alt' view. V2: size column, FNF filter, 3 selectable structures;
::Anime-File, Anime-Episode-File, Anime-Group-File, Anime-Folder-File
- test for codec (C). Tests both audio and video.
- change: it's now possible to set job 'Finished' even if the file is not found
- check box for connection keep-alive
- 'Set fid (force)' to job menu. For self edited files. (Hashing is still required.)
- change: 3 timeouts -> lockdown, new: unlocks after 15 min.
- fixed minor bug in pinger when port is out of range
- support for encrypted and compressed communication
- fixed minor epno padding bug
- fixed "Data too long for column 'audio' at row 1"
- fixed (hopefully) out of mem error when adding large folders
- change: Login Dialog doesn't show up at startup anymore
- minor changes in gui

## [1.16] - 2006-01-13
### Fixed
- bug in !mystats (thx to GuntherDW)
- some minor bugs

### Added
- support for udp server v3. Removed support for v2.
- simple chii emulator. (!uptime,!stats,!top,!mystats,!anime,!group,!randomanime,!mylist,!state)
- improved html log performance
- key command ESC in job list which stops the menu worker thread if running
- key command DEL in html log which deletes the log
- first version of an alternative job/file view (mylist tree view)
- support for postgre database
- updated the database definition and included it in jar
- support for import and export of data. (An anidb mylist export template will be added asap.)
- 'Edit Folder Path' to job menu
- fixed: infinite loop when 'Waiting/Add' and 'Add to mylist' unchecked thx to egg
- change: switching between 'Renaming' and 'Moving' @ 'Rules' does now 'Apply'. (eh..)

## [1.15] - 2005-11-09
### Fixed
- bug in rule system: Test 'A' did not work
- some minor bugs

### Added
- 'E' in test. Added regexp test to 'P' (file path). Extensions can be tested here now.
- test 'I' (Is defined). Checks whether a tag is defined or not. (E.g. I(%eng).)
- save dialog on shutdown
- 'log to file' option
- support for //-comments in rules
- removed 'offline mode' check box. And some other changes in the gui.
- support for gzip (parser was broken)
- fixed some bugs thx to egg and neginegi

## [1.14] - 2005-10-30
### Fixed
- bug in rule system: Test 'A' did not work
- some minor bugs

### Added
- support for private/local mysql database
- support for path 'P', extension 'E' and genre 'N' in tests
- support for ELSE IF and RETURN in scripts
- coloring, sorting, aid and gid columns, in job table
- new file info frame, html style
- Pause, Restore name, Rehash, Identify, Add to mylist, Set Finished, Set Folder to job popup menu
- changes in debug window

### Changed
- cleanup. A lot of internal changes (in job handling / html parsing / data structures)
- significant changes in gui and underlying system:
 -File lists replaced with one table.
 -Rename option panel replaced with Rules tab.
 -Start and Stop buttons replaced with toggle buttons for hasher thread and communication thread.
- added slider for delay between datagrams sent to server (3-10 sec)
- added updating of progress bar when checking crc (after move)
- added updating of second progress bar (total progress)

## [1.13] - 2005-09-26
### Fixed
- bug in rule system: Test 'A' did not work
- some minor bugs

### Added
- support for private/local mysql database
- support for path 'P', extension 'E' and genre 'N' in tests
- support for ELSE IF and RETURN in scripts
- coloring, sorting, aid and gid columns, in job table
- new file info frame, html style
- Pause, Restore name, Rehash, Identify, Add to mylist, Set Finished, Set Folder to job popup menu
- changes in debug window

### Changed
- change in Rule system. Scripting. Textfield instead of table
- changes in debug window
- changes in gui and underlying system:
 -File lists replaced with one table.
 -Rename option panel replaced with Rules tab.
 -Start and Stop buttons replaced with toggle buttons for hasher thread and communication thread.

## [1.12] - 2005-09-24
### Fixed
- bug in rule system: Test 'A' did not work
- some minor bugs

### Added
- extra '0' padding in epnr when an anime serie got more than 99 episodes. Will only work when total num of eps is known.
- support for dub language (D) and sub language (L) in tests
- support for NOT (!) in tests
- tags %kan = Jap. Kanji Title and %eng = English Title. (If null then %ann is used.)
- support for hentai (needs to be enabled in profile)
- change in file handler: Will not try to add files that are locked (used by another process)

## [1.11] - 2005-09-22
### Fixed
- bug in rule system: Test 'A' did not work
- some minor bugs

### Added
- combobox 'Renaming' for selection of renaming mode
- change in file handler: Will not try to add files that are locked (used by another process)

## [1.10] - 2005-09-15
### Fixed
- bug where Job is not set to Finished (when rename/moving is enabled but not needed)
- parsing bug. (Movies has parts, not episodes.)
- some minor bugs

### Added
- slider for delay between datagrams sent to server (3-10 sec)
- updating of progress bar when checking crc (after move)
- updating of second progress bar (total progress)

## [1.09] - 2005-09-09
### Fixed
- rename bug when group is "raw/unknown" (gid=0). These are now just called "unknown"
- some minor bugs

### Added
- possibility to save options
- new rule system: rename and move files based on file info
- significant changes in gui and underlying system:
 -File lists replaced with one table.
 -Rename option panel replaced with Rules tab.
 -Start and Stop buttons replaced with toggle buttons for hasher thread and communication thread.
- timeout slider for UDP communication (20-60 sec)
- "Hash Dirs", "Browser Path" and "My Database" text fields
- Wiki button. (Works only on Windows systems, unless browser path is defined.)

## [1.08] - 2005-07-05
### Fixed
- mylist file states
- file info parser (renamer was broken)

## [1.07] - 2005-06-12
### Fixed
- some minor bugs

### Added
- second progress bar
- changed comm. thread sleeping routine
- file info dialog to a text dialog
- Tiger Tree Hash
- possibility to choose each hash type
- debug tab
- made 1.4.2 comp again thx to gyrojoe

## [1.06] - 2005-05-29
### Fixed
- some minor bugs

### Added
- changed the way files are hashed and added to mylist. This is now done concurrent.
- changes in the status and logging system

## [1.05] - 2005-05-14
### Fixed
- some minor bugs

### Added
- custom renaming of files thx to ExElNeT
- some more checking on username and password
- changes in option tab

## [1.04] - 2005-05-11
### Fixed
- some minor bugs

### Added
- extra file information thx to ExElNeT. Double click rows in 'Finished Files' to see.
- offline mode
- bugfix in file rename code. thx to ExElNeT and visnu

## [1.03] - 2005-02-19
### Fixed
- some minor bugs

### Added
- extensive hashing. MD5, SHA-1 and CRC32
- changes in the error handler
- bugfix: Applet crash with Opera and Firefox

## [1.02] - 2005-02-04
### Fixed
- some minor bugs

### Added
- connection options
- connection check

## [1.01] - 2005-01-30
### Fixed
- some minor bugs

### Added
- new layout, options in own tab
- "Source" and "Other" string for AniDB file info
- possibility to save the log
- illegal character replacement customization
- recursive directory search
- new filehandler
- bugfix in AniDBConnection

## [1.00] - 2005-01-23
### Added
- First version