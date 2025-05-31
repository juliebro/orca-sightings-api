# What is ISO 8601 format?

*Written by Gemini 2.5 Flash.*

ISO 8601 is a widely used international standard for representing dates and times. It provides a consistent and unambiguous way to express dates and times, regardless of cultural differences or time zones. The standard uses a specific format, including **year, month, day, hour, minute, second, and optionally milliseconds, with separators like hyphens, colons, and the letter "T" to delineate the different elements**.

## Key components of ISO 8601

- **YYYY-MM-DD:** Represents the date with four digits for the year, two for the month, and two for the day.
- **hh:mm:ss:** Represents the time of day with two digits for the hour, two for the minute, and two for the second.
- **T:** Separates the date and time components. 
- **Z or ±hh:mm:** Specifies the time zone. **Z** indicates UTC (Coordinated Universal Time), while **±hh:mm** indicates an offset from UTC.
- **Optional milliseconds:** Can be included after the seconds, denoted by a decimal point and three digits.

## Examples of ISO 8601 formats

- **YYYY-MM-DD:** 2023-10-27 (October 27, 2023)
- **YYYY-MM-DDTHH:mm:ss:** 2023-10-27T14:30:00 (October 27, 2023, at 2:30 PM)
- **YYYY-MM-DDTHH:mm:ss.sssZ:** 2023-10-27T14:30:00.123Z (October 27, 2023, at 2:30 PM UTC with 123 milliseconds) 
- **YYYY-MM-DDTHH:mm:ss.sss±hh:mm:** 2023-10-27T14:30:00.123-05:00 (October 27, 2023, at 2:30 PM with a 5-hour offset from UTC)

## Benefits of using ISO 8601

- **Unambiguous:** Eliminates the potential for confusion that can arise from different date formats in different cultures.
- **Standardized:** Provides a universally accepted format for representing dates and times.
- **Time zone aware:** Allows for precise representation of time, including UTC and offsets from UTC.
- **Computer-readable:** Easy to parse and process by computers and applications.

## Related topics

* [`/users` resource](./users-resource.md)
* [`sightings` resource](./sightings-resource.md)