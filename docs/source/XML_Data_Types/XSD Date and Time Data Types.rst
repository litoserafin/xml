XSD Date and Time Data Types
=============================

1. **date**  
   - **Definition**: Represents a date in the format `yyyy-MM-dd`.
   - **Example**: <birthdate>2025-04-26</birthdate>
   - **Usage**: Ideal for storing dates without any time or timezone information.

2. **time**  
   - **Definition**: Represents a time in the format `hh:mm:ss` or `hh:mm:ss.sss`.
   - **Example**: <eventTime>14:30:00</eventTime>
   - **Usage**: Used to store time values (e.g., a start time for an event).

3. **dateTime**  
   - **Definition**: Represents a date and time combination in the format `yyyy-MM-ddThh:mm:ss` (optionally with time zone information).
   - **Example**: <meetingTime>2025-04-26T14:30:00</meetingTime>
   - **Usage**: Ideal for capturing both date and time with optional timezone.

4. **duration**  
   - **Definition**: Represents a period of time (e.g., "P3Y6M4DT12H30M5S").
   - **Example**: <projectDuration>P1Y2M3DT10H</projectDuration>
   - **Usage**: Used to store periods or durations such as a project's length or event duration.

5. **gYear**  
   - **Definition**: Represents a year in the format `yyyy`.
   - **Example**: <founded>2025</founded>
   - **Usage**: Ideal for situations where only a year
