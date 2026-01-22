# Units Module

Utilities for converting between metric and imperial units of measurement.

## Usage

```ez
Simply copy the `units` directory into your projects structure
Then, in the file you plan on using the `units` modules functions or constants write the following at the top of said file:

import "relative/path/to/units"
```

### Length Conversions

```ez
temp km = units.convert_mile_to_kilometer(5.0)      // Returns 8.04672
temp feet = units.convert_meter_to_feet(10.0)       // Returns 32.8084
temp inches = units.convert_centimeter_to_inch(2.54) // Returns 1.0
```

### Area Conversions

```ez
temp sqm = units.convert_sq_foot_to_sq_meter(100.0)  // Returns 9.2903
temp acres = units.convert_hectare_to_acre(1.0)      // Returns 2.47105
temp area = units.calculate_circle_area(5.0)         // Returns 78.5398
```

### Weight Conversions

```ez
temp kg = units.convert_pound_to_kilogram(150.0)    // Returns 68.0388
temp oz = units.convert_gram_to_ounce(100.0)        // Returns 3.5274
temp tons = units.convert_kilogram_to_metric_ton(1000.0) // Returns 1.0
```

### Temperature Conversions

```ez
temp f = units.convert_celsius_to_fahrenheit(100.0)  // Returns 212.0
temp c = units.convert_fahrenheit_to_celsius(32.0)   // Returns 0.0
temp k = units.convert_celsius_to_kelvin(0.0)        // Returns 273.15
```

### Volume Conversions

```ez
temp liters = units.convert_gallon_to_liter(1.0)     // Returns 3.78541
temp cups = units.convert_liter_to_cup(1.0)          // Returns 4.22675
temp ml = units.convert_fluid_ounce_to_milliliter(8.0) // Returns 236.588
```

### Speed Conversions

```ez
temp kmh = units.convert_miles_per_hour_to_kilometers_per_hour(60.0) // Returns 96.5604
temp knots = units.convert_kilometers_per_hour_to_knot(100.0)        // Returns 53.9957
temp mps = units.convert_feet_per_second_to_meters_per_second(10.0)  // Returns 3.048
```

### Data Storage Conversions

```ez
temp gb = units.convert_megabyte_to_gigabyte(1000.0)  // Returns 1.0 (SI)
temp gib = units.convert_mebibyte_to_gibibyte(1024.0) // Returns 1.0 (IEC)
temp kb = units.convert_kibibyte_to_kilobyte(1.0)     // Returns 1.024
```

## API Reference

### Length Functions

| Function | Description |
|----------|-------------|
| `convert_centimeter_to_meter(val float) -> float` | Convert cm to meters |
| `convert_meter_to_centimeter(val float) -> float` | Convert meters to cm |
| `convert_meter_to_kilometer(val float) -> float` | Convert meters to km |
| `convert_kilometer_to_meter(val float) -> float` | Convert km to meters |
| `convert_inch_to_feet(val float) -> float` | Convert inches to feet |
| `convert_foot_to_inch(val float) -> float` | Convert feet to inches |
| `convert_feet_to_yard(val float) -> float` | Convert feet to yards |
| `convert_yard_to_feet(val float) -> float` | Convert yards to feet |
| `convert_yard_to_mile(val float) -> float` | Convert yards to miles |
| `convert_mile_to_yard(val float) -> float` | Convert miles to yards |
| `convert_feet_to_mile(val float) -> float` | Convert feet to miles |
| `convert_mile_to_feet(val float) -> float` | Convert miles to feet |
| `convert_inch_to_centimeter(val float) -> float` | Convert inches to cm |
| `convert_inch_to_meter(val float) -> float` | Convert inches to meters |
| `convert_feet_to_meter(val float) -> float` | Convert feet to meters |
| `convert_feet_to_centimeter(val float) -> float` | Convert feet to cm |
| `convert_yard_to_meter(val float) -> float` | Convert yards to meters |
| `convert_mile_to_kilometer(val float) -> float` | Convert miles to km |
| `convert_mile_to_meter(val float) -> float` | Convert miles to meters |
| `convert_centimeter_to_inch(val float) -> float` | Convert cm to inches |
| `convert_meter_to_inch(val float) -> float` | Convert meters to inches |
| `convert_meter_to_feet(val float) -> float` | Convert meters to feet |
| `convert_meter_to_yard(val float) -> float` | Convert meters to yards |
| `convert_kilometer_to_mile(val float) -> float` | Convert km to miles |
| `convert_kilometer_to_feet(val float) -> float` | Convert km to feet |

### Area Functions

| Function | Description |
|----------|-------------|
| `calculate_rectangle_area(l, w float) -> float` | Calculate rectangle area |
| `calculate_square_area(s float) -> float` | Calculate square area |
| `calculate_triangle_area(b, h float) -> float` | Calculate triangle area |
| `calculate_circle_area(r float) -> float` | Calculate circle area |
| `calculate_parallelogram_area(b, h float) -> float` | Calculate parallelogram area |
| `calculate_trapezoid_area(b1, b2, h float) -> float` | Calculate trapezoid area |
| `calculate_ellipse_area(r1, r2 float) -> float` | Calculate ellipse area |
| `calculate_rhombus_area(d1, d2 float) -> float` | Calculate rhombus area |
| `convert_sq_centimeter_to_sq_meter(val float) -> float` | Convert sq cm to sq m |
| `convert_sq_meter_to_sq_centimeter(val float) -> float` | Convert sq m to sq cm |
| `convert_sq_meter_to_sq_kilometer(val float) -> float` | Convert sq m to sq km |
| `convert_sq_kilometer_to_sq_meter(val float) -> float` | Convert sq km to sq m |
| `convert_sq_meter_to_hectare(val float) -> float` | Convert sq m to hectares |
| `convert_hectare_to_sq_meter(val float) -> float` | Convert hectares to sq m |
| `convert_sq_inch_to_sq_foot(val float) -> float` | Convert sq in to sq ft |
| `convert_sq_foot_to_sq_inch(val float) -> float` | Convert sq ft to sq in |
| `convert_sq_foot_to_sq_yard(val float) -> float` | Convert sq ft to sq yd |
| `convert_sq_yard_to_sq_foot(val float) -> float` | Convert sq yd to sq ft |
| `convert_sq_foot_to_acre(val float) -> float` | Convert sq ft to acres |
| `convert_acre_to_sq_foot(val float) -> float` | Convert acres to sq ft |
| `convert_acre_to_sq_mile(val float) -> float` | Convert acres to sq mi |
| `convert_sq_mile_to_acre(val float) -> float` | Convert sq mi to acres |
| `convert_sq_inch_to_sq_centimeter(val float) -> float` | Convert sq in to sq cm |
| `convert_sq_foot_to_sq_meter(val float) -> float` | Convert sq ft to sq m |
| `convert_sq_yard_to_sq_meter(val float) -> float` | Convert sq yd to sq m |
| `convert_acre_to_sq_meter(val float) -> float` | Convert acres to sq m |
| `convert_acre_to_hectare(val float) -> float` | Convert acres to hectares |
| `convert_sq_mile_to_sq_kilometer(val float) -> float` | Convert sq mi to sq km |
| `convert_sq_centimeter_to_sq_inch(val float) -> float` | Convert sq cm to sq in |
| `convert_sq_meter_to_sq_foot(val float) -> float` | Convert sq m to sq ft |
| `convert_sq_meter_to_sq_yard(val float) -> float` | Convert sq m to sq yd |
| `convert_sq_meter_to_acre(val float) -> float` | Convert sq m to acres |
| `convert_hectare_to_acre(val float) -> float` | Convert hectares to acres |
| `convert_sq_kilometer_to_sq_mile(val float) -> float` | Convert sq km to sq mi |

### Weight Functions

| Function | Description |
|----------|-------------|
| `convert_milligram_to_gram(val float) -> float` | Convert mg to g |
| `convert_gram_to_milligram(val float) -> float` | Convert g to mg |
| `convert_gram_to_kilogram(val float) -> float` | Convert g to kg |
| `convert_kilogram_to_gram(val float) -> float` | Convert kg to g |
| `convert_kilogram_to_metric_ton(val float) -> float` | Convert kg to metric tons |
| `convert_metric_ton_to_kilogram(val float) -> float` | Convert metric tons to kg |
| `convert_ounce_to_pound(val float) -> float` | Convert oz to lb |
| `convert_pound_to_ounce(val float) -> float` | Convert lb to oz |
| `convert_pound_to_stone(val float) -> float` | Convert lb to stones |
| `convert_stone_to_pound(val float) -> float` | Convert stones to lb |
| `convert_pound_to_short_ton(val float) -> float` | Convert lb to short tons |
| `convert_short_ton_to_pound(val float) -> float` | Convert short tons to lb |
| `convert_ounce_to_gram(val float) -> float` | Convert oz to g |
| `convert_ounce_to_kilogram(val float) -> float` | Convert oz to kg |
| `convert_pound_to_gram(val float) -> float` | Convert lb to g |
| `convert_pound_to_kilogram(val float) -> float` | Convert lb to kg |
| `convert_stone_to_kilogram(val float) -> float` | Convert stones to kg |
| `convert_short_ton_to_kilogram(val float) -> float` | Convert short tons to kg |
| `convert_short_ton_to_metric_ton(val float) -> float` | Convert short tons to metric tons |
| `convert_gram_to_ounce(val float) -> float` | Convert g to oz |
| `convert_gram_to_pound(val float) -> float` | Convert g to lb |
| `convert_kilogram_to_ounce(val float) -> float` | Convert kg to oz |
| `convert_kilogram_to_pound(val float) -> float` | Convert kg to lb |
| `convert_kilogram_to_stone(val float) -> float` | Convert kg to stones |
| `convert_kilogram_to_short_ton(val float) -> float` | Convert kg to short tons |
| `convert_metric_ton_to_short_ton(val float) -> float` | Convert metric tons to short tons |

### Temperature Functions

| Function | Description |
|----------|-------------|
| `convert_celsius_to_fahrenheit(val float) -> float` | Convert Celsius to Fahrenheit |
| `convert_celsius_to_kelvin(val float) -> float` | Convert Celsius to Kelvin |
| `convert_fahrenheit_to_celsius(val float) -> float` | Convert Fahrenheit to Celsius |
| `convert_fahrenheit_to_kelvin(val float) -> float` | Convert Fahrenheit to Kelvin |
| `convert_kelvin_to_celsius(val float) -> float` | Convert Kelvin to Celsius |
| `convert_kelvin_to_fahrenheit(val float) -> float` | Convert Kelvin to Fahrenheit |

### Volume Functions

| Function | Description |
|----------|-------------|
| `convert_milliliter_to_liter(val float) -> float` | Convert mL to L |
| `convert_liter_to_milliliter(val float) -> float` | Convert L to mL |
| `convert_liter_to_cubic_meter(val float) -> float` | Convert L to cubic meters |
| `convert_cubic_meter_to_liter(val float) -> float` | Convert cubic meters to L |
| `convert_fluid_ounce_to_cup(val float) -> float` | Convert fl oz to cups |
| `convert_cup_to_fluid_ounce(val float) -> float` | Convert cups to fl oz |
| `convert_cup_to_pint(val float) -> float` | Convert cups to pints |
| `convert_pint_to_cup(val float) -> float` | Convert pints to cups |
| `convert_pint_to_quart(val float) -> float` | Convert pints to quarts |
| `convert_quart_to_pint(val float) -> float` | Convert quarts to pints |
| `convert_quart_to_gallon(val float) -> float` | Convert quarts to gallons |
| `convert_gallon_to_quart(val float) -> float` | Convert gallons to quarts |
| `convert_fluid_ounce_to_gallon(val float) -> float` | Convert fl oz to gallons |
| `convert_gallon_to_fluid_ounce(val float) -> float` | Convert gallons to fl oz |
| `convert_fluid_ounce_to_milliliter(val float) -> float` | Convert fl oz to mL |
| `convert_fluid_ounce_to_liter(val float) -> float` | Convert fl oz to L |
| `convert_cup_to_milliliter(val float) -> float` | Convert cups to mL |
| `convert_cup_to_liter(val float) -> float` | Convert cups to L |
| `convert_pint_to_liter(val float) -> float` | Convert pints to L |
| `convert_quart_to_liter(val float) -> float` | Convert quarts to L |
| `convert_gallon_to_liter(val float) -> float` | Convert gallons to L |
| `convert_gallon_to_milliliter(val float) -> float` | Convert gallons to mL |
| `convert_milliliter_to_fluid_ounce(val float) -> float` | Convert mL to fl oz |
| `convert_liter_to_fluid_ounce(val float) -> float` | Convert L to fl oz |
| `convert_milliliter_to_cup(val float) -> float` | Convert mL to cups |
| `convert_liter_to_cup(val float) -> float` | Convert L to cups |
| `convert_liter_to_pint(val float) -> float` | Convert L to pints |
| `convert_liter_to_quart(val float) -> float` | Convert L to quarts |
| `convert_liter_to_gallon(val float) -> float` | Convert L to gallons |
| `convert_milliliter_to_gallon(val float) -> float` | Convert mL to gallons |

### Speed Functions

| Function | Description |
|----------|-------------|
| `convert_meters_per_second_to_kilometers_per_hour(val float) -> float` | Convert m/s to km/h |
| `convert_kilometers_per_hour_to_meters_per_second(val float) -> float` | Convert km/h to m/s |
| `convert_miles_per_hour_to_feet_per_second(val float) -> float` | Convert mph to ft/s |
| `convert_feet_per_second_to_miles_per_hour(val float) -> float` | Convert ft/s to mph |
| `convert_miles_per_hour_to_kilometers_per_hour(val float) -> float` | Convert mph to km/h |
| `convert_miles_per_hour_to_meters_per_second(val float) -> float` | Convert mph to m/s |
| `convert_feet_per_second_to_meters_per_second(val float) -> float` | Convert ft/s to m/s |
| `convert_feet_per_second_to_kilometers_per_hour(val float) -> float` | Convert ft/s to km/h |
| `convert_kilometers_per_hour_to_miles_per_hour(val float) -> float` | Convert km/h to mph |
| `convert_meters_per_second_to_miles_per_hour(val float) -> float` | Convert m/s to mph |
| `convert_meters_per_second_to_feet_per_second(val float) -> float` | Convert m/s to ft/s |
| `convert_kilometers_per_hour_to_feet_per_second(val float) -> float` | Convert km/h to ft/s |
| `convert_knot_to_kilometers_per_hour(val float) -> float` | Convert knots to km/h |
| `convert_kilometers_per_hour_to_knot(val float) -> float` | Convert km/h to knots |
| `convert_knot_to_miles_per_hour(val float) -> float` | Convert knots to mph |
| `convert_miles_per_hour_to_knot(val float) -> float` | Convert mph to knots |
| `convert_knot_to_meters_per_second(val float) -> float` | Convert knots to m/s |
| `convert_meters_per_second_to_knot(val float) -> float` | Convert m/s to knots |

### Data Storage Functions (SI - Decimal)

| Function | Description |
|----------|-------------|
| `convert_byte_to_kilobyte(val float) -> float` | Convert bytes to KB |
| `convert_kilobyte_to_byte(val float) -> float` | Convert KB to bytes |
| `convert_kilobyte_to_megabyte(val float) -> float` | Convert KB to MB |
| `convert_megabyte_to_kilobyte(val float) -> float` | Convert MB to KB |
| `convert_megabyte_to_gigabyte(val float) -> float` | Convert MB to GB |
| `convert_gigabyte_to_megabyte(val float) -> float` | Convert GB to MB |
| `convert_gigabyte_to_terabyte(val float) -> float` | Convert GB to TB |
| `convert_terabyte_to_gigabyte(val float) -> float` | Convert TB to GB |
| `convert_terabyte_to_petabyte(val float) -> float` | Convert TB to PB |
| `convert_petabyte_to_terabyte(val float) -> float` | Convert PB to TB |

### Data Storage Functions (IEC - Binary)

| Function | Description |
|----------|-------------|
| `convert_byte_to_kibibyte(val float) -> float` | Convert bytes to KiB |
| `convert_kibibyte_to_byte(val float) -> float` | Convert KiB to bytes |
| `convert_kibibyte_to_mebibyte(val float) -> float` | Convert KiB to MiB |
| `convert_mebibyte_to_kibibyte(val float) -> float` | Convert MiB to KiB |
| `convert_mebibyte_to_gibibyte(val float) -> float` | Convert MiB to GiB |
| `convert_gibibyte_to_mebibyte(val float) -> float` | Convert GiB to MiB |
| `convert_gibibyte_to_tebibyte(val float) -> float` | Convert GiB to TiB |
| `convert_tebibyte_to_gibibyte(val float) -> float` | Convert TiB to GiB |
| `convert_tebibyte_to_pebibyte(val float) -> float` | Convert TiB to PiB |
| `convert_pebibyte_to_tebibyte(val float) -> float` | Convert PiB to TiB |

### Data Storage Functions (Cross-system)

| Function | Description |
|----------|-------------|
| `convert_kilobyte_to_kibibyte(val float) -> float` | Convert KB to KiB |
| `convert_megabyte_to_mebibyte(val float) -> float` | Convert MB to MiB |
| `convert_gigabyte_to_gibibyte(val float) -> float` | Convert GB to GiB |
| `convert_terabyte_to_tebibyte(val float) -> float` | Convert TB to TiB |
| `convert_kibibyte_to_kilobyte(val float) -> float` | Convert KiB to KB |
| `convert_mebibyte_to_megabyte(val float) -> float` | Convert MiB to MB |
| `convert_gibibyte_to_gigabyte(val float) -> float` | Convert GiB to GB |
| `convert_tebibyte_to_terabyte(val float) -> float` | Convert TiB to TB |

### Constants

**Length:** `CM_PER_METER`, `METERS_PER_KM`, `INCHES_PER_FOOT`, `FEET_PER_YARD`, `FEET_PER_MILE`, `YARDS_PER_MILE`, `CM_PER_INCH`, `METERS_PER_FOOT`, `KM_PER_MILE`, `FEET_PER_METER`, `MILES_PER_KM`

**Area:** `SQ_CM_PER_SQ_METER`, `SQ_METERS_PER_SQ_KM`, `SQ_INCHES_PER_SQ_FOOT`, `SQ_FEET_PER_SQ_YARD`, `SQ_FEET_PER_ACRE`, `ACRES_PER_SQ_MILE`, `SQ_METERS_PER_SQ_FOOT`, `HECTARES_PER_ACRE`

**Weight:** `MG_PER_GRAM`, `GRAMS_PER_KG`, `KG_PER_METRIC_TON`, `OZ_PER_LB`, `LB_PER_STONE`, `LB_PER_SHORT_TON`, `GRAMS_PER_OZ`, `KG_PER_LB`, `LB_PER_KG`

**Temperature:** `CELSIUS_TO_FAHRENHEIT_MULTIPLIER`, `FAHRENHEIT_TO_CELSIUS_MULTIPLIER`, `FAHRENHEIT_OFFSET`, `KELVIN_OFFSET`

**Volume:** `ML_PER_LITER`, `LITERS_PER_CUBIC_METER`, `FL_OZ_PER_CUP`, `CUPS_PER_PINT`, `PINTS_PER_QUART`, `QUARTS_PER_GALLON`, `ML_PER_FL_OZ`, `LITERS_PER_GALLON`, `GALLONS_PER_LITER`

**Speed:** `KMH_PER_MPS`, `MPS_PER_KMH`, `KMH_PER_MPH`, `MPH_PER_KMH`, `KMH_PER_KNOT`, `KNOTS_PER_KMH`, `MPH_PER_KNOT`

**Data (SI):** `BYTES_PER_KB`, `KB_PER_MB`, `MB_PER_GB`, `GB_PER_TB`, `TB_PER_PB`

**Data (IEC):** `BYTES_PER_KIB`, `KIB_PER_MIB`, `MIB_PER_GIB`, `GIB_PER_TIB`, `TIB_PER_PIB`

## Potential Use Cases

- **Scientific calculations**: Convert between metric and imperial measurements
- **Cooking applications**: Convert recipe measurements between cups, mL, oz, etc.
- **Fitness apps**: Convert weight between kg and lbs, distance between km and miles
- **Weather apps**: Convert temperatures between Celsius, Fahrenheit, and Kelvin
- **Navigation**: Convert speeds between mph, km/h, and knots
- **File management**: Display file sizes in appropriate units (KB, MB, GB, KiB, MiB, GiB)
- **Real estate**: Convert between square feet, square meters, and acres
