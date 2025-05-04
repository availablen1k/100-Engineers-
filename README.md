# Itinerary Pettifier

Itinerary Prettifier is a command-line tool that formats flight itineraries into a more readable and customer-friendly format. It replaces airport codes with their full names, formats date/time values, and removes excessive whitespace.

## Features
- Converts IATA & ICAO codes to airport names (from airport-lookup.csv).
- Formats dates & times (ISO 8601 → human-readable format).
- Removes excessive blank lines (allows max 1 consecutive blank line).
- Supports terminal color formatting (optional).
- Handles malformed input gracefully.

## Installation
1. Clone the Repository:
   git clone https://gitea.koodsisu.fi/nikolaondoja/itinerary.git
   cd itinerary-prettifier

## Usage
Run the program with the following command:
   go run . ./input.txt ./output.txt ./airport-lookup.csv

### With Colors (Terminal Output Only)
   go run . ./colors ./input.txt ./output.txt ./airport-lookup.csv

### Show Help Message
   go run . -h

## Input & Output Example

### Input (`input.txt`)
Your flight departs from #LAX, and your destination is ##EGLL.
Departure date: D(2022-05-09T08:07Z)
Departure time: T12(2022-05-09T08:07Z)

Thank you for booking with us!

### Output (`output.txt`)
Your flight departs from Los Angeles International Airport, and your destination is London Heathrow Airport.
Departure date: 09 May 2022
Departure time: 08:07 AM (+00:00)

Thank you for booking with us!

## How It Works

### Airport Code Conversion
| Code Type | Format | Example | Converts To |
|-----------|--------|---------|-------------|
| **IATA**  | `#XXX`  | `#LAX`  | `Los Angeles International Airport` |
| **ICAO**  | `##XXXX` | `##EGLL` | `London Heathrow Airport` |

### Date & Time Formatting
| Input Format | Example | Output |
|-------------|---------|--------|
| `D(YYYY-MM-DDTHH:MMZ)` | `D(2022-05-09T08:07Z)` | `09 May 2022` |
| `T12(YYYY-MM-DDTHH:MMZ)` | `T12(2022-05-09T08:07Z)` | `08:07 AM (+00:00)` |
| `T24(YYYY-MM-DDTHH:MMZ)` | `T24(2022-05-09T08:07Z)` | `08:07 (+00:00)` |

### Whitespace Cleaning
- Replaces `\v, \f, \r` with `\n`.
- Ensures only **one** blank line is preserved.

## Error Handling
| Scenario | Behavior ||----------|----------|
| **Incorrect usage** | Shows help message |
| **Missing input file** | Prints `"Input not found"` |
| **Missing `airport-lookup.csv`** | Prints `"Airport lookup not found"` |
| **Malformed lookup file** | Prints `"Airport lookup malformed"` |
| **Unknown airport code** | Leaves the code unchanged |


## License
This project is **open-source** under the **MIT License**.

## Credits
Built with ❤️  by Nikolao Ndoja.
