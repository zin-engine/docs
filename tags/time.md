# 🕒 `<zin-time />` — Time & Date Formatter

The `<zin-time />` tag dynamically renders formatted dates, times, and timestamps directly in your HTML. It eliminates the need for client-side JavaScript or external libraries for common date formatting tasks.



## ✅ Basic Usage

```html
<!-- Default: full ISO datetime (now) -->
<zin-time />

<!-- ISO date -->
<zin-time view="date" />

<!-- Current time in 12-hour format -->
<zin-time view="time:12" />
````



## 🔮 Attributes

| Attribute | Required | Description                                                    |
| --- | --- | --- |
| `view`    | ❌        | Format type (e.g., `date`, `time`, `dayname`)                  |
| `when`    | ❌        | Offset from a specific date/time (e.g., `tomorrow`, `now +1m`) |
| `tz`      | ❌        | Timezone override (e.g., `Asia/Tokyo`)                         |



## 🔁 Common View Options

| `view` value  | Example Output          | Description      |
| - | -- | - |
| `date`        | `2025-06-27`            | ISO date         |
| `time`        | `14:35`                 | 24-hour time     |
| `time:12`     | `2:35 PM`               | 12-hour time     |
| `datetime`    | `2025-06-27 14:35`      | 24-hour datetime |
| `datetime:12` | `Jun 27, 2025, 2:35 PM` | 12-hour datetime |
| `day`         | `27`                    | Day of the month |
| `dayname`     | `Friday`                | Weekday name     |
| `month`       | `06`                    | Month number     |
| `monthname`   | `June`                  | Month name       |
| `year`        | `2025`                  | Full year        |
| `week`        | `26`                    | ISO week number  |
| `unix`        | `1724793294210`         | Unix time (ms)   |
| `unix:sec`    | `1724793294`            | Unix time (s)    |



## 🗓️ Examples

```html
<!-- Tomorrow's date in 12-hour datetime format -->
<zin-time when="tomorrow" view="datetime:12" />

<!-- 3 weeks ago from today, show the weekday -->
<zin-time when="today -3w" view="dayname" />

<!-- First day of next month -->
<zin-time when="now +1m @startOf:month" view="date" />

<!-- Last day of any given date’s month -->
<zin-time when="2025-02-01 @endOf:month" view="date" />

<!-- Current time in Tokyo -->
<zin-time view="time:12" tz="Asia/Tokyo" />
```



## ⚠️ Notes

* If `view` is not provided, ZIN defaults to `datetime` in ISO format.
* Timezone must be a valid IANA timezone (e.g., `America/New_York`, `Asia/Kolkata`).
* Complex `when` expressions support basic math:

  * `+1d`, `-2w`, `+3m`, etc.
  * Use `@startOf:month` or `@endOf:month` for date boundary control.



## 🔗 See Also

* [All ZIN Tags →](../Tags/)
* [Getting Started →](../Getting-Started.md)
