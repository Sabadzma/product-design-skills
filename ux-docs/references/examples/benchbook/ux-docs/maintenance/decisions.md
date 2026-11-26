# Maintenance decisions

## Take equipment out of service

When a coordinator confirms a maintenance block, Benchbook reserves that time for servicing on the item's shared schedule.

## Handle overlapping reservations

If a proposed maintenance block overlaps a reservation, Benchbook shows the affected reservations before the coordinator confirms. If the coordinator confirms, Benchbook marks those reservations as disrupted and lets members [choose another time](../equipment-booking/decisions.md#reschedule-a-disrupted-reservation).

Showing conflicts before confirmation gives the coordinator a chance to choose a time that affects fewer members.
