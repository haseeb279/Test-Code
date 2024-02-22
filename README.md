# Task Feedback

## Refactoring Suggestions

***app/Http/Controllers/BookingController.php***

- DRY Principle should be followed to refactor repetitive code snippets (e.g. variable assignments from `$data`) into utility functions.
- Data Validation can be done to ensure expected data types and formats in each controller.
- Longer methods like (`distanceFeed`) can be split into into smaller, more focused functions to improve readability and maintainability.
- Multiple If conditionals can be replaced with ternary operators to make code simpler and more readable.
- Error handling can be done in all controllers to handle errors more gracefully.
- Variable naming could be more descriptive.

***app/Repository/BookingRepository.php***

- For the separation of concerns, some functionality can be shifted to separate utility classes like sending email, sending push notifications, datetime formatting etc.
- Functions like `changeTimedoutStatus`, `changeCompletedStatus` etc contain duplicate logic for sending emails. which can be refactored into reusable helper functions like `sendJobStatusChangeEmail($user, $job, $newStatus)`.
- Common success/failure logic  can be extracted into helper functions and nested conditionals can be replaced with with else if statements in some functions.
- Some functions have a high complexity due to nested conditions and loops. Complex functions can be broken down into into smaller, more manageable functions.
- Error handling can be implemented to avoid uncertain errors and make the code more robust.
- Enums can be used to compare job types instead of comparing strings.
