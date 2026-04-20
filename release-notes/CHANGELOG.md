# Change Log

All notable changes to WarriorServe will be documented in this file.

This project follows:
- Semantic-ish versioning if applicable
- Categories such as Added, Changed, Fixed, Removed, Security

## [Beacon 1.9] - 04-20-2026
### Added
- Added async prevention from calling in ContactTriggerHandler to prevent limits issues
### Changed
- VeteranConfirmationStatus_Queuable from manually setting ContactTriggerHandler to skip calling from queueable
### Fixed
- None
### Removed
- None

### Request
- [CR-001 Contact Trigger Prevent Queue From Async](../change-requests/CR-001-contact-trigger-prevent-queue-from-async.md)