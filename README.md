# starlight-time

**Time and Date Utilities for the Starlight Programming Language**


Developer – Dominex Macedon


---

## Overview

starlight-time provides simple and efficient time and date utilities for server-side Starlight programs.
It is designed to be lightweight, synchronous where needed, and easy to use inside long-running services, scripts, and schedulers.

---

## Installation

`
npm install starlight-time
`

---

## Importing

`
import time from "starlight-time";
`

---

## Available Functions

**now()**
Returns the current Date object.

`
let current = time.now();
`

---

**formatDate(date?)**
Formats a Date object into YYYY-MM-DD.
If no argument is provided, the current date is used.

`
let today = time.formatDate();
let custom = time.formatDate(time.now());
`

---

**formatTime(date?)**
Formats a Date object into HH:MM:SS.
If no argument is provided, the current time is used.

`
let clock = time.formatTime();
`

---

**sleep(ms)**
Blocks execution for the given milliseconds.
Useful for controlled delays in scripts.

`
time.sleep(1000);
`

---

**setTimer(callback, interval)**
Runs a callback repeatedly at a fixed interval.
Returns a function to stop the timer.

`
let stop = time.setTimer(() => {
  sldeploy(time.formatTime());
}, 1000);
`

`
stop();
`

---

**secondsToHMS(seconds)**
Converts seconds into HH:MM:SS format.

`
let duration = time.secondsToHMS(3661);
`

---

## Typical Usage (Clock Style)

`
import time from "starlight-time";

time.setTimer(() => {
let now = time.formatTime();
sldeploy(now);
}, 1000); `

---

## Server-Side Notes

• Designed for server-side execution
• No browser dependencies
• Safe for long-running processes
• Ideal for schedulers, logs, timers, and system utilities

---

## Related


Starlight Language Learning Hub


---


starlight-time is part of the official Starlight standard ecosystem.
