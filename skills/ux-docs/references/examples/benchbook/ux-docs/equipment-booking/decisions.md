# Equipment booking decisions

## Book available equipment

When a member requests a time that overlaps a reservation or a [maintenance block](../maintenance/decisions.md#take-equipment-out-of-service), Benchbook declines the request and asks them to choose another time. For an available time, Benchbook confirms the reservation and updates the shared schedule.

## Reschedule a disrupted reservation

When [maintenance disrupts a reservation](../maintenance/decisions.md#handle-overlapping-reservations), Benchbook offers any available times for the same item. Selecting a new time follows the [booking availability rule](#book-available-equipment).

## Open questions

- Should Benchbook suggest a comparable item when the original item has no available times?
