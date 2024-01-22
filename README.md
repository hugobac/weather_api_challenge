
# Programming Challenge - API Integration

Thank you for participating in our programming challenge session. Good luck! ;)

## Expectations

This exercise aims to assess your coding skills. Don't worry about being correct; there is no right or wrong answer.

## Before You Start

The challenge takes 45 minutes. Ensure your computer is properly configured (e.g., programming language, code editor, and internet connection).

## Context

You're traveling to a foreign city and want to know what clothes are appropriate for the weather. Instead of checking the climate conditions, you decide to create an application using the AccuWeather API.

## Instructions

Create a project that integrates with the AccuWeather API, checks the weather forecast for the next 5 days, and outputs which clothes to take based on the criteria below:

```plaintext
+-----------------------+-----------------------+-----------------------+
| AccuWeather Field     | Condition             | Clothes               |
+=======================+=======================+=======================+
| DailyForecasts[].Temp | Less than 45          | "Coat", "Winter jacket"|
| erature.Maximum.Value | degrees               |                       |
+-----------------------+-----------------------+-----------------------+
| DailyForecasts[].Temp | 45 to 79              | "Fleece", "Short      |
| erature.Maximum.Value | degrees               | Sleeves"               |
+-----------------------+-----------------------+-----------------------+
| DailyForecasts[].Temp | 80 degrees and above  | "Shorts"               |
| erature.Maximum.Value |                       |                       |
+-----------------------+-----------------------+-----------------------+
| DailyForecasts[].Day. | Above 50              | "Rain Coat"            |
| RainProbability       |                       |                       |
| or                    |                       |                       |
| DailyForecasts[].Night| Above 50              | "Snow Outfit"          |
| .RainProbability      |                       |                       |
| or                    |                       |                       |
| DailyForecasts[].Day. | Above 50              | "Shell Jacket"         |
| IceProbability        |                       |                       |
| or                    |                       |                       |
| DailyForecasts[].Night|                       |                       |
| .IceProbability       |                       |                       |
+-----------------------+-----------------------+-----------------------+
```

- No conversion is needed from/to Celsius.
- Feel free to model the solution as you wish (e.g., CLI, API, function, etc).
- While coding, take the opportunity to say out loud what you are thinking (if you are comfortable with). If you get stuck, just ask for help. Feel free to search (Stackoverflow, Google, Docs, etc).

## API Specs

API KEY: `xaaaaax`

Endpoint: [https://dataservice.accuweather.com/forecasts/v1/daily/5day/60449?apikey=xaaaaax&details=true](https://dataservice.accuweather.com/forecasts/v1/daily/5day/60449?apikey=xaaaaax&details=true)

City Codes: 60449 (Santiago), 45881 (São Paulo), 349727 (New York), 101924 (Beijing), 127164 (Cairo).

## Expected Output

Your project should present/return a JSON output following the example below:

```json
{
  "forecasts": [
    {
      "date": "2022-03-24",
      "clothes": ["Coat", "Winter jacket"]
    },
    {
      "date": "2022-03-25",
      "clothes": ["Rain Coat"]
    }
  ]
}
```

## Evaluation Criteria

- Automated Tests
- Architectural Decisions
- Communication Skills
- Project Structure
- Good programming practices (DRY, YAGNI, KISS, variable/function names, comments if necessary, etc)
- Absence of Bad Smells
- Error handling
