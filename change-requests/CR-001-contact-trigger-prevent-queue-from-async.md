# CR-001 Contact Trigger Prevent Queue From Async

## Status
Working

## Request Date 
2026-04-19

## Requested By
William Galinat / WarriorServe

## Owner
William Galinat / WarriorServe

## Summary
When Contact records are updated by asynchronous Apex processes, the Contact trigger may attempt to enqueue VeteranConfirmationStatus_Queueable, causing async execution failures.

## Business Reason
Customer and internal org automations that update Contact records must not fail due to WarriorServe attempting to start queueable work from an asynchronous execution context.
## Current Behavior
Existing logic only skips processing for certain Veteran Confirmation Status re-entry scenarios. It does not prevent enqueue attempts when the Contact trigger executes from batch, future, queueable, or scheduled Apex.

## Requested Behavior
The Contact trigger should skip enqueuing VeteranConfirmationStatus_Queueable when running in asynchronous Apex contexts to prevent nested async failures.

## Impacted Areas
- Apex Classes