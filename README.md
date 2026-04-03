# Unit-Converter

A simple unit conversion tool written in XCX, supporting multiple measurement categories through an interactive console menu.

---

## Features

- **Temperature**: Convert between Celsius (°C), Fahrenheit (°F), and Kelvin (K)
- **Length**: Convert between metres, kilometres, centimetres, millimetres, miles, feet, inches, and yards
- **Weight**: Convert between kilograms, grams, milligrams, pounds, ounces, tonnes, and stones
- **Volume**: Convert between litres, millilitres, centilitres, cubic metres, US gallons, quarts, pints, cups, fluid ounces, tablespoons, and teaspoons
- **Speed**: Convert between m/s, km/h, mph, ft/s, knots, and Mach number

All conversions use a pivot-unit approach for accuracy and maintainability.

---

## Project Structure

``` text
Unit-Converter/
├── project.pax          # Project configuration
└── src/
    ├── main.xcx         # Entry point & main menu
    ├── temperature.xcx  # Temperature conversion module
    ├── length.xcx       # Length conversion module
    ├── weight.xcx       # Weight conversion module
    ├── volume.xcx       # Volume conversion module
    └── speed.xcx        # Speed conversion module
```

---

## Requirements

- XCX compiler/runtime environment
- No external dependencies required

---

## Installation

1. Clone or download the project:
   git clone <repository-url>
   cd Unit-Converter

2. Ensure your XCX environment is properly configured.

---

## Usage

1. Run the main file:
   xcx run src/main.xcx

2. Select a conversion category from the menu:
   1  Temperature
   2  Length
   3  Weight
   4  Volume
   5  Speed
   q  Quit

3. Follow the prompts:
   - Enter the source unit (e.g., km)
   - Enter the target unit (e.g., mi)
   - Enter the numeric value to convert

4. View the result and continue or exit.

---

## Supported Units

| Category    | Units                                                                  |
|-------------|------------------------------------------------------------------------|
| Temperature | C, F, K                                                                |
| Length      | m, km, cm, mm, mi, ft, in, yd                                         |
| Weight      | kg, g, mg, lb, oz, t, st                                              |
| Volume      | l, ml, cl, m3, cm3, gal, qt, pt, cup, floz, tbsp, tsp               |
| Speed       | ms, kmh, mph, fps, kn, mach                                           |

---

## Error Handling

- Invalid units trigger a halt.error with a descriptive message
- Unknown menu choices are reported gracefully without crashing
- All conversions validate input before processing

---

## Design Notes

- **Pivot-unit architecture**: Each module converts via a base unit (e.g., metres for length) to simplify logic and ensure consistency
- **Modular structure**: Each category is isolated in its own file for easy maintenance and extension
- **Interactive REPL-style UI**: Designed for terminal use with clear prompts and formatted output

---
