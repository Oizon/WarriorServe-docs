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
When other things touch a Contact it is firing a queueable job which is failing in some instances from other async jobs

## Business Reason
Orgs personal development are failing due to WarriorServe code

## Current Behavior
There is internal flag on the class that skips only from the Veteran Confirmation Status but not because its Async

## Requested Behavior
The class should be aware of what called it so it auto skips

## Impacted Areas
- Apex Classes