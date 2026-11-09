# Rinse — expanded car wash pitch demo

A static, responsive concept hosted on GitHub Pages. No build step or dependencies.

## Pitch walkthrough

1. Choose **Explore customer demo**. The Hyundai i20 starts with 3 of 4 Essential washes remaining; a second vehicle has no package.
2. Select **Book a wash**, choose an available time tomorrow and confirm. Two sample bookings make 10:00–11:00 unavailable on both bays.
3. Switch **Explore the concept** to **Staff dashboard preview**. Find the new booking and move it through Arrived → In Progress → Completed.
4. Return to Customer preview: the wash balance has decreased once. Completion and expiry messages appear under Reminders.
5. Switch to Owner preview to edit opening hours, available bays, closures, provisional service prices and durations. Existing bookings retain their price/duration.
6. Use My cars to add sample vehicles; choose a car without an active package to demonstrate purchase. OTP code is **123456**.

## Demonstration assumptions

Four service tiers have provisional prices/durations: Essential ₹299/30min, Complete ₹499/45min, Premium ₹699/60min, Signature ₹999/90min. These replace the original simplified pitch prices and are not commercial offers. Package choices are 1/4/8/12 washes with no example discount and 30-day validity, manual renewal, per-car/per-service credits. Vehicle category surcharges are not implemented. One active package per car/service. A booking reserves a credit; staff completion deducts it. Pay-at-centre bookings require demo payment confirmation before completion. Cancellation is allowed while Booked and before start, without a fee.

The in-memory scheduler prevents overlapping reservations per bay and overlapping bookings for the same vehicle within this tab. This does not provide production-safe concurrency across browsers. No shared backend, persistent database, real OTP, payments, access control or messaging exists. Changes reset on refresh. Role switching and staff enable/disable are illustrative, not authentication. Do not enter real customer details.

Advanced reporting/export, refunds, rescheduling, walk-in entry, manager balance corrections, feedback, automatic renewal, photo uploads, referrals and multi-location support are outside this wireframe. Owner changes affect new availability; existing bookings need review. Final business rules and pricing remain subject to agreement.

## Hosting

Live demo: https://gavriankur.github.io/rinse-car-wash-wireframe/

GitHub Pages deploys from main, root directory. The printed pitch QR points at the same URL and remains valid. This is a pitch demo; production needs commercial hosting, a backend and a database.
