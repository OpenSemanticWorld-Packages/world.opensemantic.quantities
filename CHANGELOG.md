# Changelog: world.opensemantic.quantities

Migration from SPARQL-based extraction to enriched QUDT JSON-LD (qudt-parsing).
QUDT version: 3.1.4

## Summary

| Metric | Count |
|--------|-------|
| Old items | 1369 |
| New items | 1103 |
| Removed | 370 |
| Added | 104 |
| Common | 999 |

## Known Limitations

- Some QUDT quantity kinds have no `applicableUnit` linked (e.g., BloodGlucoseLevel variants).
  These appear as removed characteristics with no replacement, as the old code used different join logic.
- Duplicate units exist in QUDT (e.g., `unit:FemtoM` and `unit:FEMTOM`) causing duplicate enum entries.

## Item Changes by Type

| Type | Removed | Added |
|------|---------|-------|
| ComposedQuantityUnit | 369 | 104 |
| QuantityKind | 1 | 0 |

## Removed Items

### ComposedQuantityUnit (369: 369 converted to subobjects, 0 truly removed)

Most removed ComposedQuantityUnits are **not deleted** — they were converted from
standalone Item pages to subobjects embedded in their base unit (e.g., `cm/s` is now
a `composed_units` entry inside `MetrePerSecond` with ID `Item:BASE#SUB`).

#### Converted to Subobjects (369)

| Name | Symbol | Label |
|------|--------|-------|
| AttojouleSecond | aJ·s | AttoJoule Second |
| CentimetrePerHour | cm/h | CentiMetre per Hour |
| CentimetrePerKelvin | cm/K | CentiMetre per Kelvin |
| CentimetrePerSecond | cm/s | CentiMetre per Second |
| CentimetrePerSquareSecond | cm/s² | CentiMetre per Square Second |
| CentimetreSecondDegreeCelsius | cm·s·°C | CentiMetre Second Degree Celsius |
| CentimetreToTheFourthPower | cm⁴ | CentiMetre to the Fourth Power |
| CentimetresPerThousandYears | cm/ka | CentiMetres per Thousand Years |
| CentimetresPerYear | cm/a | CentiMetres per Year |
| CentimolePerKilogram | cmol/kg | CentiMole per KiloGram |
| CentimolePerLitre | cmol/L | CentiMole per Litre |
| CentinewtonMetre | cN·m | CentiNewton Metre |
| CubicCentimeterPerMoleSecond | cm³/(mol·s) | Cubic CentiMeter per Mole Second |
| CubicCentimetre | cm³ | Cubic CentiMetre |
| CubicCentimetrePerCubicCentimetre | cm³/cm³ | Cubic CentiMetre per Cubic CentiMetre |
| CubicCentimetrePerCubicMetre | cm³/m³ | Cubic CentiMetre per Cubic Metre |
| CubicCentimetrePerDay | cm³/d | Cubic CentiMetre per Day |
| CubicCentimetrePerHour | cm³/h | Cubic CentiMetre per Hour |
| CubicCentimetrePerKelvin | cm³/K | Cubic CentiMetre per Kelvin |
| CubicCentimetrePerMinute | cm³/min | Cubic CentiMetre per Minute |
| CubicCentimetrePerMole | cm³/mol | Cubic CentiMetre per Mole |
| CubicCentimetrePerSecond | cm³/s | Cubic CentiMetre per Second |
| CubicCentimetresPerGram | cm³/g | Cubic CentiMetres per Gram |
| CubicDecametre | dam³ | Cubic DecaMetre |
| CubicDecimetre | dm³ | Cubic DeciMetre |
| CubicDecimetrePerCubicMetre | dm³/m³ | Cubic DeciMetre per Cubic Metre |
| CubicDecimetrePerDay | dm³/d | Cubic DeciMetre per Day |
| CubicDecimetrePerHour | dm³/h | Cubic DeciMetre per Hour |
| CubicDecimetrePerMinute | dm³/min | Cubic DeciMetre per Minute |
| CubicDecimetrePerMole | dm³/mol | Cubic DeciMetre per Mole |
| CubicDecimetrePerSecond | dm³/s | Cubic DeciMetre per Second |
| CubicKilometrePerSquareSecond | km³/s² | Cubic KiloMetre per Square Second |
| CubicMicrometresMicrons | μm³ | Cubic MicroMetres (microNs) |
| CubicMicronsPerCubicMetre | μm³/m³ | Cubic MicroNs per Cubic Metre |
| CubicMicronsPerMillilitre | μm³/mL | Cubic MicroNs per MilliLitre |
| CubicMillimetre | mm³ | Cubic MilliMetre |
| CubicMillimetrePerCubicMetre | mm³/m³ | Cubic MilliMetre per Cubic Metre |
| CubicMillimetrePerGram | mm³/g | Cubic MilliMetre per Gram |
| CubicMillimetrePerKilogram | mm³/kg | Cubic MilliMetre per KiloGram |
| DecilitrePerGram | dL/g | DeciLitre per Gram |
| DecinewtonMetre | dN·m | DeciNewton Metre |
| DecisiemensPerMetre | dS/m | DeciSiemens per Metre |
| FemtogramsPerKilogram | fg/kg | FemtoGrams per KiloGram |
| FemtogramsPerLitre | fg/L | FemtoGrams per Litre |
| FemtomolesPerKilogram | fmol/kg | FemtoMoles per KiloGram |
| FemtomolesPerLitre | fmol/L | FemtoMoles per Litre |
| GigacoulombPerCubicMetre | GC/m³ | GigaCoulomb per Cubic Metre |
| GigahertzMetre | GHz·m | GigaHertz Metre |
| GigajoulePerHour | GJ/h | GigaJoule per Hour |
| GigajoulePerSquareMetre | GJ/m² | GigaJoule per Square Metre |
| GigapascalCubedCentimetrePerGram | GPa·cm³/g | GigaPascal Cubed CentiMetre per Gram |
| GigawattHour | GW·h | GigaWatt Hour |
| HectopascalCubicMetrePerSecond | hPa·m³/s | HectoPascal Cubic Metre per Second |
| HectopascalLitrePerSecond | hPa·L/s | HectoPascal Litre per Second |
| HectopascalPerKelvin | hPa/K | HectoPascal per Kelvin |
| HectopascalsPerHour | hPa/h | HectoPascals per Hour |
| KiloElectronVoltPerMicrometre | keV/μm | Kilo Electron Volt per MicroMetre |
| KiloNewtonPerCubicMetre | kN/m³ | Kilo Newton per Cubic Metre |
| KiloNewtonPerMetre | kN/m | Kilo Newton per Metre |
| KiloNewtonPerSquareMetre | kN/m² | Kilo Newton per Square Metre |
| KiloNewtonSquareMetre | kN·m² | Kilo Newton Square Metre |
| KiloWatthour | kW·h | KiloWatthour |
| KiloampereHour | kA·h | KiloAmpere Hour |
| KiloamperePerMetre | kA/m | KiloAmpere per Metre |
| KiloamperePerSquareMetre | kA/m² | KiloAmpere per Square Metre |
| KilocoulombPerCubicMetre | kC/m³ | KiloCoulomb per Cubic Metre |
| KilocoulombPerSquareMetre | kC/m² | KiloCoulomb per Square Metre |
| KilogramKelvin | kg·K | KiloGram Kelvin |
| KilogramMetrePerSecond | kg·m/s | KiloGram Metre per Second |
| KilogramPerCubicCentimetre | kg/cm³ | KiloGram per Cubic CentiMetre |
| KilogramPerCubicDecimetre | kg/dm³ | KiloGram per Cubic DeciMetre |
| KilogramPerCubicMetre | kg/m³ | KiloGram per Cubic Metre |
| KilogramPerCubicSecondKelvin | kg/(s³·K) | KiloGram per Cubic Second Kelvin |
| KilogramPerDay | kg/d | KiloGram per Day |
| KilogramPerGigajoule | kg/GJ | KiloGram per GigaJoule |
| KilogramPerHectare | kg/ha | KiloGram per Hectare |
| KilogramPerHectarePerYear | kg/(ha·a) | KiloGram per Hectare per Year |
| KilogramPerHour | kg/h | KiloGram per Hour |
| KilogramPerJoule | kg/J | KiloGram per Joule |
| KilogramPerKilogram | kg/kg | KiloGram per KiloGram |
| KilogramPerKilomol | kg/kmol | KiloGram per KiloMol |
| KilogramPerLitre | kg/L | KiloGram per Litre |
| KilogramPerMetre | kg/m | KiloGram per Metre |
| KilogramPerMillimetre | kg/mm | KiloGram per MilliMetre |
| KilogramPerMinute | kg/min | KiloGram per Minute |
| KilogramPerMol | kg/mol | KiloGram per Mol |
| KilogramPerPascalSecondMetre | kg/(Pa·s·m) | KiloGram per Pascal Second Metre |
| KilogramPerSecond | kg/s | KiloGram per Second |
| KilogramPerSecondSquareMetre | kg/(s·m²) | KiloGram per Second Square Metre |
| KilogramPerSquareCentimetre | kg/cm² | KiloGram per Square CentiMetre |
| KilogramPerSquareFoot | kg/ft² | KiloGram per Square Foot |
| KilogramPerSquareMetre | kg/m² | KiloGram per Square Metre |
| KilogramPerSquareMetrePerDay | kg/(m²·d) | KiloGram per Square Metre per Day |
| KilogramPerSquareMetreSquareSecond | kg/(m²·s²) | KiloGram per Square Metre Square Second |
| KilogramPerSquareSecond | kg/s² | KiloGram per Square Second |
| KilogramPerYear | kg/a | KiloGram per Year |
| KilogramSquareCentimetre | kg·cm² | KiloGram Square CentiMetre |
| KilogramSquareMetre | kg·m² | KiloGram Square Metre |
| KilogramSquareMetrePerSecond | kg·m²/s | KiloGram Square Metre per Second |
| KilogramSquareMillimetre | kg·mm² | KiloGram Square MilliMetre |
| KilogramSquareSecond | kg·s² | KiloGram Square Second |
| KilogramsPerCubicMetreSecond | kg/(m³·s) | KiloGrams per Cubic Metre Second |
| KilogramsPerMetreHour | kg/(m·h) | KiloGrams per Metre Hour |
| KilogramsPerMetreSecond | kg/(m·s) | KiloGrams per Metre Second |
| KilogramsPerMetreSquareSecond | kg/(m·s²) | KiloGrams per Metre Square Second |
| KilogramsPerSquareKilometre | kg/km² | KiloGrams per Square KiloMetre |
| KilogramsPerSquareMetrePascalSecond | kg/(m²·Pa·s) | KiloGrams per Square Metre Pascal Second |
| KilogramsPerSquareMetreSecond | kg/(m²·s) | KiloGrams per Square Metre Second |
| KilohertzMetre | kHz·m | KiloHertz Metre |
| KilojoulePerKelvin | kJ/K | KiloJoule per Kelvin |
| KilojoulePerKilogram | kJ/kg | KiloJoule per KiloGram |
| KilojoulePerKilogramKelvin | kJ/(kg·K) | KiloJoule per KiloGram Kelvin |
| KilojoulePerMole | kJ/mol | KiloJoule per Mole |
| KilolitrePerHour | kL/h | KiloLitre per Hour |
| KilometrePerHour | km/h | KiloMetre per Hour |
| KilometrePerSecond | km/s | KiloMetre per Second |
| KilometresPerDay | km/d | KiloMetres per Day |
| KilomolePerCubicMetre | kmol/m³ | KiloMole per Cubic Metre |
| KilomolePerHour | kmol/h | KiloMole per Hour |
| KilomolePerKilogram | kmol/kg | KiloMole per KiloGram |
| KilomolePerMinute | kmol/min | KiloMole per Minute |
| KilomolePerSecond | kmol/s | KiloMole per Second |
| KilonewtonMetre | kN·m | KiloNewton Metre |
| KilonewtonMetrePerDegree | kN·m/° | KiloNewton Metre per Degree |
| KilonewtonMetrePerDegreeMetre | kN·m/(°·m) | KiloNewton Metre per Degree Metre |
| KilonewtonMetrePerMetre | kN·m/m | KiloNewton Metre per Metre |
| KilopascalPerKelvin | kPa/K | KiloPascal per Kelvin |
| KilopascalPerMillimetre | kPa/mm | KiloPascal per MilliMetre |
| KilopascalSquareMetrePerGram | kPa·m²/g | KiloPascal Square Metre per Gram |
| KilosiemensPerMetre | kS/m | KiloSiemens per Metre |
| KilotonnePerYear | kt/a | KiloTonne per Year |
| KilovoltAmpere | kV·A | KiloVolt Ampere |
| KilovoltAmpereHour | kV·A·h | KiloVolt Ampere Hour |
| KilovoltAmpereHour | kVA·h | KiloVolt Ampere Hour |
| KilovoltPerMetre | kV/m | KiloVolt per Metre |
| KilowattHourPerSquareMetre | kW·h/m² | KiloWatt Hour per Square Metre |
| KilowattPerSquareMetre | kW/m² | KiloWatt per Square Metre |
| KiloweberPerMetre | kWb/m | KiloWeber per Metre |
| MegaElectronVoltFemtometre | MeV·fm | Mega Electron Volt FemtoMetre |
| MegaElectronVoltPerCentimetre | MeV/cm | Mega Electron Volt per CentiMetre |
| MegaHertzPerKelvin | MHz/K | Mega Hertz per Kelvin |
| MegaHertzPerTesla | MHz/T | Mega Hertz per Tesla |
| MegaamperePerSquareMetre | MA/m² | MegaAmpere per Square Metre |
| MegacoulombPerCubicMetre | MC/m³ | MegaCoulomb per Cubic Metre |
| MegacoulombPerSquareMetre | MC/m² | MegaCoulomb per Square Metre |
| MegagramPerCubicMetre | Mg/m³ | MegaGram per Cubic Metre |
| MegagramPerHectare | Mg/ha | MegaGram per Hectare |
| MegagramPerHectarePerYear | Mg/(ha·a) | MegaGram per Hectare per Year |
| MegahertzMetre | MHz·m | MegaHertz Metre |
| MegajoulePerCubicMetre | MJ/m³ | MegaJoule per Cubic Metre |
| MegajoulePerHour | MJ/h | MegaJoule per Hour |
| MegajoulePerKelvin | MJ/K | MegaJoule per Kelvin |
| MegajoulePerKilogram | MJ/kg | MegaJoule per KiloGram |
| MegajoulePerSecond | MJ/s | MegaJoule per Second |
| MegajoulePerSquareMetre | MJ/m² | MegaJoule per Square Metre |
| MegajoulePerSquareMetrePerDay | MJ/(m²·d) | MegaJoule per Square Metre per Day |
| MeganewtonMetre | MN·m | MegaNewton Metre |
| MegapascalCubicMetrePerSecond | MPa·m³/s | MegaPascal Cubic Metre per Second |
| MegapascalLitrePerSecond | MPa·L/s | MegaPascal Litre per Second |
| MegapascalPerKelvin | MPa/K | MegaPascal per Kelvin |
| MegapascalSquareRootMetre | MPa√m | MegaPascal Square Root Metre |
| MegasiemensPerMetre | MS/m | MegaSiemens per Metre |
| MegatonnePerYear | Mt/a | MegaTonne per Year |
| MegavoltAmpere | MV·A | MegaVolt Ampere |
| MegavoltAmpereHour | MVA·h | MegaVolt Ampere Hour |
| MegavoltAmpereHour | MV·A·h | MegaVolt Ampere Hour |
| MegavoltPerMetre | MV/m | MegaVolt per Metre |
| MegawattHour | MW·h | MegaWatt Hour |
| MicroMetrePerNewton | μm/N | Micro Metre per Newton |
| MicrobecquerelsPerKilogram | μBq/kg | MicroBecquerels per KiloGram |
| MicrobecquerelsPerLitre | μBq/L | MicroBecquerels per Litre |
| MicrocoulombPerCubicMetre | μC/m³ | MicroCoulomb per Cubic Metre |
| MicrocoulombPerSquareMetre | μC/m² | MicroCoulomb per Square Metre |
| MicrofaradPerKilometre | μF/km | MicroFarad per KiloMetre |
| MicrofaradPerMetre | μF/m | MicroFarad per Metre |
| MicrogramPerCubicMetre | μg/m³ | MicroGram per Cubic Metre |
| MicrogramPerDecilitre | μg/dL | MicroGram per DeciLitre |
| MicrogramPerGramPerDay | μg/(g·d) | MicroGram per Gram per Day |
| MicrogramPerKilogram | μg/kg | MicroGram per KiloGram |
| MicrogramPerLitre | μg/L | MicroGram per Litre |
| MicrogramPerMilligram | μg/mg | MicroGram per MilliGram |
| MicrogramPerMillilitre | μg/mL | MicroGram per MilliLitre |
| MicrogramPerSquareInch | μg/in² | MicroGram per Square Inch |
| MicrogramsPerCubicMetreHour | μg/(m³·h) | MicroGrams per Cubic Metre Hour |
| MicrogramsPerGram | μg/g | MicroGrams per Gram |
| MicrogramsPerGramPerHour | μg/(g·h) | MicroGrams per Gram per Hour |
| MicrogramsPerLitreHour | μg/(L·h) | MicroGrams per Litre Hour |
| MicrogramsPerLitrePerHour | μg/(L·d) | MicroGrams per Litre per Hour |
| MicrogramsPerSquareCentimetreWeek | μg/(cm²·wk) | MicroGrams per Square CentiMetre Week |
| MicrogramsPerSquareMetreDay | μg/(m²·d) | MicroGrams per Square Metre Day |
| MicrohenryPerKiloohm | μH/kΩ | MicroHenry per KiloOhm |
| MicrohenryPerMetre | μH/m | MicroHenry per Metre |
| MicrohenryPerOhm | μH/Ω | MicroHenry per Ohm |
| MicrokatalPerLitre | μkat/L | MicroKatal per Litre |
| MicrolitrePerLitre | μL/L | MicroLitre per Litre |
| MicrometrePerKelvin | μm/K | MicroMetre per Kelvin |
| MicrometrePerMinute | μm/min | MicroMetre per Minute |
| MicrometrePerSecond | μm/s | MicroMetre per Second |
| MicromolePerMicromoleOfBiomassDay | μmol/(μmol·d) | MicroMole per MicroMole of Biomass Day |
| MicromolePerSquareMetrePerSquareSecond | μmol/(m²·s²) | MicroMole per Square Metre per Square Second |
| MicromolesPerGram | μmol/g | MicroMoles per Gram |
| MicromolesPerGramHour | μmol/(g·h) | MicroMoles per Gram Hour |
| MicromolesPerGramSecond | μmol/(g·s) | MicroMoles per Gram Second |
| MicromolesPerKilogram | μmol/kg | MicroMoles per KiloGram |
| MicromolesPerLitre | μmol/L | MicroMoles per Litre |
| MicromolesPerLitreDay | μm/(L·d) | MicroMoles per Litre Day |
| MicromolesPerLitreHour | μmol/(L·h) | MicroMoles per Litre Hour |
| MicromolesPerMole | μmol/mol | MicroMoles per Mole |
| MicromolesPerSecond | μmol/s | MicroMoles per Second |
| MicromolesPerSquareMetre | μmol/m² | MicroMoles per Square Metre |
| MicromolesPerSquareMetreDay | μmol/(m²·d) | MicroMoles per Square Metre Day |
| MicromolesPerSquareMetreHour | μmol/(m²·h) | MicroMoles per Square Metre Hour |
| MicromolesPerSquareMetreSecond | μmol/(m²·s) | MicroMoles per Square Metre Second |
| MicronewtonMetre | μN·m | MicroNewton Metre |
| MicrosiemenSquaredPerCentimetreSquared | μS²/cm² | MicroSiemen Squared per CentiMetre Squared |
| MicrosiemensPerCentimetre | μS/cm | MicroSiemens per CentiMetre |
| MicrosiemensPerMetre | μS/m | MicroSiemens per Metre |
| MicrosievertPerHour | μSv/h | MicroSievert per Hour |
| MicrovoltPerMetre | μV/m | MicroVolt per Metre |
| MicrowattPerSquareMetre | μW/m² | MicroWatt per Square Metre |
| MilliampereHour | mA·h | MilliAmpere Hour |
| MilliamperePerMillimetre | mA/mm | MilliAmpere per MilliMetre |
| MillibecquerelsPerGram | mBq/g | MilliBecquerels per Gram |
| MillibecquerelsPerKilogram | mBq/kg | MilliBecquerels per KiloGram |
| MillibecquerelsPerLitre | mBq/L | MilliBecquerels per Litre |
| MillibecquerelsPerSquareMetreDay | mBq/(m²·d) | MilliBecquerels per Square Metre Day |
| MillicoulombPerCubicMetre | mC/m³ | MilliCoulomb per Cubic Metre |
| MillicoulombPerKilogram | mC/kg | MilliCoulomb per KiloGram |
| MillicoulombPerSquareMetre | mC/m² | MilliCoulomb per Square Metre |
| MilligramPerCubicMetre | mg/m³ | MilliGram per Cubic Metre |
| MilligramPerDay | mg/d | MilliGram per Day |
| MilligramPerGram | mg/g | MilliGram per Gram |
| MilligramPerGramPerHour | mg/(g·h) | MilliGram per Gram per Hour |
| MilligramPerHectare | mg/ha | MilliGram per Hectare |
| MilligramPerHour | mg/h | MilliGram per Hour |
| MilligramPerKilogram | mg/kg | MilliGram per KiloGram |
| MilligramPerKilogramPerDay | mg/(kg·d) | MilliGram per KiloGram per Day |
| MilligramPerLitre | mg/L | MilliGram per Litre |
| MilligramPerMetre | mg/m | MilliGram per Metre |
| MilligramPerMillilitre | mg/mL | MilliGram per MilliLitre |
| MilligramPerMinute | mg/min | MilliGram per Minute |
| MilligramPerSecond | mg/s | MilliGram per Second |
| MilligramPerSquareCentimetre | mg/cm² | MilliGram per Square CentiMetre |
| MilligramPerSquareDecimetre | mg/dm² | MilliGram per Square DeciMetre |
| MilligramPerSquareMetre | mg/m² | MilliGram per Square Metre |
| MilligramsPerCubicMetreDay | mg/(m³·d) | MilliGrams per Cubic Metre Day |
| MilligramsPerCubicMetreHour | mg/(m³·h) | MilliGrams per Cubic Metre Hour |
| MilligramsPerCubicMetreSecond | mg/(m³·s) | MilliGrams per Cubic Metre Second |
| MilligramsPerDecilitre | mg/dL | MilliGrams per DeciLitre |
| MilligramsPerSquareMetreDay | mg/(m²·d) | MilliGrams per Square Metre Day |
| MilligramsPerSquareMetreHour | mg/(m²·h) | MilliGrams per Square Metre Hour |
| MilligramsPerSquareMetreSecond | mg/(m²·s) | MilliGrams per Square Metre Second |
| MillihenryPerKiloohm | mH/kΩ | MilliHenry per KiloOhm |
| MillihenryPerOhm | mH/Ω | MilliHenry per Ohm |
| MillijoulePerGram | mJ/g | MilliJoule per Gram |
| MillijoulePerSquareMetre | mJ/m² | MilliJoule per Square Metre |
| MillikatalPerLitre | mkat/L | MilliKatal per Litre |
| MillilitrePerCubicMetre | mL/m³ | MilliLitre per Cubic Metre |
| MillilitrePerDay | mL/d | MilliLitre per Day |
| MillilitrePerGram | mL/g | MilliLitre per Gram |
| MillilitrePerHour | mL/h | MilliLitre per Hour |
| MillilitrePerKelvin | mL/K | MilliLitre per Kelvin |
| MillilitrePerKilogram | mL/kg | MilliLitre per KiloGram |
| MillilitrePerLitre | mL/L | MilliLitre per Litre |
| MillilitrePerMinute | mL/min | MilliLitre per Minute |
| MillilitrePerSecond | mL/s | MilliLitre per Second |
| MillilitrePerSquareCentimetreMinute | mL/(cm²·min) | MilliLitre per Square CentiMetre Minute |
| MillilitrePerSquareCentimetreSecond | mL/(cm²·s) | MilliLitre per Square CentiMetre Second |
| MillilitresPerSquareMetreDay | mL/(m²·d) | MilliLitres per Square Metre Day |
| MillimetrePerHour | mm/h | MilliMetre per Hour |
| MillimetrePerKelvin | mm/K | MilliMetre per Kelvin |
| MillimetrePerMinute | mm/min | MilliMetre per Minute |
| MillimetrePerSecond | mm/s | MilliMetre per Second |
| MillimetrePerSquareMetre | mm/m² | MilliMetre per Square Metre |
| MillimetrePerYear | mm/a | MilliMetre per Year |
| MillimetresPerDay | mm/d | MilliMetres per Day |
| MillimolePerGram | mmol/g | MilliMole per Gram |
| MillimolePerKilogram | mmol/kg | MilliMole per KiloGram |
| MillimolePerSquareMetrePerHour | mmol/(m²·h) | MilliMole per Square Metre per Hour |
| MillimolesPerCubicMetre | mmol/m³ | MilliMoles per Cubic Metre |
| MillimolesPerCubicMetreDay | mmol/(m³·d) | MilliMoles per Cubic Metre Day |
| MillimolesPerLitre | mmol/L | MilliMoles per Litre |
| MillimolesPerMole | mmol/mol | MilliMoles per Mole |
| MillimolesPerSquareMetre | mmol/m² | MilliMoles per Square Metre |
| MillimolesPerSquareMetreDay | mmol/(m²·d) | MilliMoles per Square Metre Day |
| MillimolesPerSquareMetreSecond | mmol/(m²·s) | MilliMoles per Square Metre Second |
| MillinewtonMetre | mN·m | MilliNewton Metre |
| MillinewtonPerMetre | mN/m | MilliNewton per Metre |
| MillionUsDollarsPerFlight | $M/flight | MilliOn Us Dollars per Flight |
| MillipascalSecond | mPa·s | MilliPascal Second |
| MillisiemensPerCentimetre | mS/cm | MilliSiemens per CentiMetre |
| MillisiemensPerMetre | mS/m | MilliSiemens per Metre |
| MillivoltPerMetre | mV/m | MilliVolt per Metre |
| MillivoltPerMinute | mV/min | MilliVolt per Minute |
| MilliwattPerMilligram | mW/mg | MilliWatt per MilliGram |
| MilliwattPerSquareMetre | mW/m² | MilliWatt per Square Metre |
| MilliwattsPerSquareCentimetreMicrometreSteradian | mW/(cm²·μm·sr) | MilliWatts per Square CentiMetre MicroMetre Steradian |
| MilliwattsPerSquareMetreNanometre | mW/(m²·nm) | MilliWatts per Square Metre NanoMetre |
| MilliwattsPerSquareMetreNanometreSteradian | mW/(m²·nm·sr) | MilliWatts per Square Metre NanoMetre Steradian |
| NanobecquerelsPerLitre | nBq/L | NanoBecquerels per Litre |
| NanofaradPerMetre | nF/m | NanoFarad per Metre |
| NanogramPerCubicMetre | ng/m³ | NanoGram per Cubic Metre |
| NanogramPerDay | ng/d | NanoGram per Day |
| NanogramPerDecilitre | ng/dL | NanoGram per DeciLitre |
| NanogramPerKilogram | ng/kg | NanoGram per KiloGram |
| NanogramPerLitre | ng/L | NanoGram per Litre |
| NanogramPerMicrolitre | ng/μL | NanoGram per MicroLitre |
| NanogramPerMilligram | ng/mg | NanoGram per MilliGram |
| NanogramPerMillilitre | ng/mL | NanoGram per MilliLitre |
| NanogramPerSquareCentimetre | ng/cm² | NanoGram per Square CentiMetre |
| NanogramPerSquareCentimetreDay | ng/(cm²·d) | NanoGram per Square CentiMetre Day |
| NanogramPerSquareMetrePascalSecond | ng/(m²·Pa·s) | NanoGram per Square Metre Pascal Second |
| NanohenryPerMetre | nH/m | NanoHenry per Metre |
| NanokatalPerLitre | nkat/L | NanoKatal per Litre |
| NanometerPerCentimeterMegapascal | nm/(cm·MPa) | NanoMeter per CentiMeter MegaPascal |
| NanometerPerMillimeterMegapascal | nm/(mm·MPa) | NanoMeter per MilliMeter MegaPascal |
| NanomolePerSquareMetrePerSecond | nmol/(m²·s) | NanoMole per Square Metre per Second |
| NanomolesPerCubicCentimetreHour | nmol/(cm³·h) | NanoMoles per Cubic CentiMetre Hour |
| NanomolesPerGram | nmol/g | NanoMoles per Gram |
| NanomolesPerGramPerHour | nmol/(g·h) | NanoMoles per Gram per Hour |
| NanomolesPerGramSecond | nmol/(g·s) | NanoMoles per Gram Second |
| NanomolesPerKilogram | nmol/kg | NanoMoles per KiloGram |
| NanomolesPerLitre | nmol/L | NanoMoles per Litre |
| NanomolesPerLitreDay | nmol/(L·d) | NanoMoles per Litre Day |
| NanomolesPerLitreHour | nmol/(L·h) | NanoMoles per Litre Hour |
| NanomolesPerMicrogramHour | nmol/(μg·h) | NanoMoles per MicroGram Hour |
| NanomolesPerMicromole | nmol/μmol | NanoMoles per MicroMole |
| NanomolesPerMicromoleDay | nmol/(μmol·d) | NanoMoles per MicroMole Day |
| NanomolesPerSquareMetreDay | nmol/(m²·d) | NanoMoles per Square Metre Day |
| NanosiemensPerCentimetre | nS/cm | NanoSiemens per CentiMetre |
| NanosiemensPerMetre | nS/m | NanoSiemens per Metre |
| PicoampsPerMicromoleLitre | pA/(μmol·L) | PicoAmps per MicroMole Litre |
| PicofaradPerMetre | pF/m | PicoFarad per Metre |
| PicogramsPerGram | pg/g | PicoGrams per Gram |
| PicogramsPerKilogram | pg/kg | PicoGrams per KiloGram |
| PicogramsPerLitre | pg/L | PicoGrams per Litre |
| PicogramsPerMilligram | pg/mg | PicoGrams per MilliGram |
| PicogramsPerMillilitre | pg/mL | PicoGrams per MilliLitre |
| PicokatalPerLitre | pkat/L | PicoKatal per Litre |
| PicomolesPerCubicMetre | pmol/m³ | PicoMoles per Cubic Metre |
| PicomolesPerCubicMetreSecond | pmol/(m³·s) | PicoMoles per Cubic Metre Second |
| PicomolesPerKilogram | pmol/kg | PicoMoles per KiloGram |
| PicomolesPerLitre | pmol/L | PicoMoles per Litre |
| PicomolesPerLitreDay | pmol/(L·d) | PicoMoles per Litre Day |
| PicomolesPerLitreHour | pmol/(L·h) | PicoMoles per Litre Hour |
| PicomolesPerMetreWattSecond | pmol/(m·W·s) | PicoMoles per Metre Watt Second |
| PicomolesPerSquareMetreDay | pmol/(m²·d) | PicoMoles per Square Metre Day |
| PicopascalPerKilometre | pPa/km | PicoPascal per KiloMetre |
| PicosiemensPerMetre | pS/m | PicoSiemens per Metre |
| PicowattPerSquareMetre | pW/m² | PicoWatt per Square Metre |
| PicowattsPerSquareCentimetreLitre | pW/(cm²·L) | PicoWatts per Square CentiMetre Litre |
| QuarticMillimetre | mm⁴ | Quartic MilliMetre |
| SexticCentimetre | cm⁶ | Sextic CentiMetre |
| SquareCentimetre | cm² | Square CentiMetre |
| SquareCentimetreMinute | cm²·min | Square CentiMetre Minute |
| SquareCentimetrePerVoltSecond | cm²/(V·s) | Square CentiMetre per Volt Second |
| SquareCentimetreSecond | cm²·s | Square CentiMetre Second |
| SquareCentimetresPerCubicCentimetre | cm²/cm³ | Square CentiMetres per Cubic CentiMetre |
| SquareCentimetresPerSecond | cm²/s | Square CentiMetres per Second |
| SquareDecimetre | dm² | Square DeciMetre |
| SquareKilogramsPerSquareSecond | kg²/s² | Square KiloGrams per Square Second |
| SquareKilometresPerSquareSecond | km²/s² | Square KiloMetres per Square Second |
| SquareMicrometre | μm² | Square MicroMetre |
| SquareMicronsPerMillilitre | μm/mL | Square MicroNs per MilliLitre |
| SquareMillimetre | mm² | Square MilliMetre |
| SquareMillimetrePerSecond | mm²/s | Square MilliMetre per Second |
| SquareNanometre | nm² | Square NanoMetre |
| TerawattHour | TW·h | TeraWatt Hour |
| TerawattHourPerYear | TW·h/a | TeraWatt Hour per Year |

### QuantityKind (1)

| Name | Label | Units |
|------|-------|-------|
| LinearAcceleration | Linear Acceleration | 4 |

## Added Items

### ComposedQuantityUnit (104)

| Name | Symbol | Label |
|------|--------|-------|
| AmpsPerMoleLitre | A/(mol·L) | Amps per Mole Litre |
| BecquerelsPerGram | Bq/g | Becquerels per Gram |
| BecquerelsPerSquareMetreDay | Bq/(m²·d) | Becquerels per Square Metre Day |
| BulgarianLevPerWattHour | лв./(W·h) | Bulgarian Lev per Watt Hour |
| CoulombPerGram | C/g | Coulomb per Gram |
| CoulombPerGramSecond | C/(g·s) | Coulomb per Gram Second |
| CubicMetrePerGram | m³/g | Cubic Metre per Gram |
| CubicMetrePerGramSquareSecond | m³/(g·s²) | Cubic Metre per Gram Square Second |
| CubicMetresPerLitre | m³/L | Cubic Metres per Litre |
| CzechKorunaPerWattHour | Kč/(W·h) | Czech Koruna per Watt Hour |
| DanishKronePerWattHour | kr/(W·h) | Danish Krone per Watt Hour |
| DegreeCelsiusMetre | °C·m | Degree Celsius Metre |
| DegreesCelsiusGramPerSquareMetre | °C·g/m² | Degrees Celsius Gram per Square Metre |
| ElectronVoltMetre | eV·m | Electron Volt Metre |
| ErgPerSquareMetre | erg/m² | Erg per Square Metre |
| ForintPerWattHour | Ft/Wh | Forint per Watt Hour |
| GramKelvin | g·K | Gram Kelvin |
| GramMetre | g·m | Gram Metre |
| GramMetrePerSecond | g·m/s | Gram Metre per Second |
| GramPerCubicSecondKelvin | g/(s³·K) | Gram per Cubic Second Kelvin |
| GramPerGramPerDay | g/(g·d) | Gram per Gram per Day |
| GramPerHectarePerYear | g/(ha·a) | Gram per Hectare per Year |
| GramPerJoule | g/J | Gram per Joule |
| GramPerLiterPerDay | g/(L·d) | Gram per Liter per Day |
| GramPerMetreSecond | g/(m·s) | Gram per Metre Second |
| GramPerPascalSecondMetre | g/(Pa·s·m) | Gram per Pascal Second Metre |
| GramPerSecondSquareMetre | g/(s·m²) | Gram per Second Square Metre |
| GramPerSquareFoot | g/ft² | Gram per Square Foot |
| GramPerSquareInch | g/in² | Gram per Square Inch |
| GramPerSquareMetrePascalSecond | g/(m^2·Pa·s) | Gram per Square Metre Pascal Second |
| GramPerSquareMetreSquareSecond | g/(m²·s²) | Gram per Square Metre Square Second |
| GramPerSquareSecond | g/s² | Gram per Square Second |
| GramPerYear | g/a | Gram per Year |
| GramSquareMetre | g·m² | Gram Square Metre |
| GramSquareMetrePerSecond | g·m²/s | Gram Square Metre per Second |
| GramSquareSecond | g·s² | Gram Square Second |
| GramsPerCubicMetreDay | g/(m³·d) | Grams per Cubic Metre Day |
| GramsPerCubicMetreHour | g/(m³·h) | Grams per Cubic Metre Hour |
| GramsPerCubicMetreSecond | g/(m³·s) | Grams per Cubic Metre Second |
| GramsPerGramPerHour | g/(g·h) | Grams per Gram per Hour |
| GramsPerLitreHour | g/(L·h) | Grams per Litre Hour |
| GramsPerMetreHour | g/(m·h) | Grams per Metre Hour |
| GramsPerMetreSecondSquared | g/(m·s²) | Grams per Metre Second Squared |
| GramsPerSquareMetreSecond | g/(m²·s) | Grams per Square Metre Second |
| GramsPerSquareMetreWeek | g/(m²·wk) | Grams per Square Metre Week |
| JoulePerGramKelvinCubicMetre | J/(g·K·m³) | Joule per Gram Kelvin Cubic Metre |
| JoulePerGramKelvinPascal | J/(g·K·Pa) | Joule per Gram Kelvin Pascal |
| JoulePerSquareMetrePerDay | J/(m²·d) | Joule per Square Metre per Day |
| JouleSquareMetrePerGram | J·m²/g | Joule Square Metre per Gram |
| KelvinSquareMetresPerGramSecond | K·m²/(g·s) | Kelvin Square Metres per Gram Second |
| LitrePerCubicMetre | L/m³ | Litre per Cubic Metre |
| LitrePerGram | L/g | Litre per Gram |
| LitrePerSquareMetreMinute | L/(m²·min) | Litre per Square Metre Minute |
| LitrePerSquareMetreSecond | L/(m²·s) | Litre per Square Metre Second |
| LitresPerSquareMetreDay | L/(m²·d) | Litres per Square Metre Day |
| MeterPerLiter | m/L | Meter per Liter |
| MeterPerMeterPascal | m/(m·Pa) | Meter per Meter Pascal |
| MetersPerLitreDay | m/(L·d) | Meters per Litre Day |
| MetreGram | m·g | Metre Gram |
| MetrePerNewton | m/N | Metre per Newton |
| MetreSecondDegreeCelsius | m·s·°C | Metre Second Degree Celsius |
| MolePerGramPascal | mol/(g·Pa) | Mole per Gram Pascal |
| MolePerMoleDay | mol/(mol·d) | Mole per Mole Day |
| MolePerSquareMetrePerHour | mol/(m²·h) | Mole per Square Metre per Hour |
| MolePerSquareMetrePerSquareSecond | mol/(m²·s²) | Mole per Square Metre per Square Second |
| MolesPerCubicMetreDay | mol/(m³·d) | Moles per Cubic Metre Day |
| MolesPerCubicMetreHour | mol/(m³·h) | Moles per Cubic Metre Hour |
| MolesPerGram | mol/g | Moles per Gram |
| MolesPerGramSecond | mol/(g·s) | Moles per Gram Second |
| MolesPerLitreDay | mol/(L·d) | Moles per Litre Day |
| MolesPerLitreHour | mol/(L·h) | Moles per Litre Hour |
| MolesPerMetreWattSecond | mol/(m·W·s) | Moles per Metre Watt Second |
| NewtonMetrePerDegree | N·m/° | Newton Metre per Degree |
| NewtonMetrePerGram | N·m/g | Newton Metre per Gram |
| NewtonPerGram | N/g | Newton per Gram |
| NewtonSquareMetrePerSquareGram | N·m²/g² | Newton Square Metre per Square Gram |
| NorwegianKronePerWattHour | kr/(W·h) | Norwegian Krone per Watt Hour |
| PascalCubedMetrePerGram | Pa·m³/g | Pascal Cubed Metre per Gram |
| PascalSquareMetrePerGram | Pa·m²/g | Pascal Square Metre per Gram |
| PoundSterlingPerWattHour | £/(W·h) | Pound Sterling per Watt Hour |
| RadianSquareMetrePerGram | rad·m²/g | Radian Square Metre per Gram |
| ReciprocalMetreMetreSteradian | /(m·m·sr) | Reciprocal Metre Metre Steradian |
| ReciprocalMetrePerMetre | m^-2 | Reciprocal Metre per Metre |
| ReciprocalMolePerLitre | /(mol·L) | Reciprocal Mole per Litre |
| ReciprocalSquareGram | /g² | Reciprocal Square Gram |
| ReciprocalVoltAmpereHour | /(VA·h) | Reciprocal Volt Ampere Hour |
| ReciprocalVoltAmpereHour | /(V·A·h) | Reciprocal Volt Ampere Hour |
| RomanianNewLeuPerWattHour | RON/(W·h) | Romanian New Leu per Watt Hour |
| SiemensSquaredPerMetreSquared | S²/m² | Siemens Squared per Metre Squared |
| SievertPerHour | Sv/h | Sievert per Hour |
| SquareGramsPerSquareSecond | g²/s² | Square Grams per Square Second |
| SquareMetreMinute | m²·min | Square Metre Minute |
| SquareMetreSecond | m²·s | Square Metre Second |
| SquareMetresPerCubicMetre | m²/m³ | Square Metres per Cubic Metre |
| SwedishKronaPerWattHour | kr/(W·h) | Swedish Krona per Watt Hour |
| SwissFrancPerWattHour | CHF/(W·h) | Swiss Franc per Watt Hour |
| SwissFrancsPerGram | CHF/g | Swiss Francs per Gram |
| SwissFrancsPerGram | CHF/g | Swiss Francs per Gram |
| ThermochemicalCaloriePerCubicMetreKelvin | cal_th/(m³·K) | Thermochemical Calorie per Cubic Metre Kelvin |
| UsDollarsPerFlight | $/flight | US Dollars per Flight |
| VoltPerMinute | V/min | Volt per Minute |
| WattHourPerYear | W·h/a | Watt Hour per Year |
| WattsPerSquareMetreLitre | W/(m²·L) | Watts per Square Metre Litre |
| ZlotyPerWattHour | zł/(W·h) | Zloty per Watt Hour |

## Changed Items

### QuantityKind (146 changed)

| Name | Changes |
|------|---------|
| MolarVolume | units: 5 -> 5, removed 1, added 1 |
| Speed | units: 13 -> 13, removed 8, added 8 |
| Concentration | units: 12 -> 12, removed 7, added 7 |
| ThermalDiffusionCoefficient | units: 3 -> 3, removed 2, added 2 |
| RotationalMass | units: 3 -> 4, removed 3, added 4 |
| ElectricChargePerMass | units: 6 -> 7, removed 3, added 4 |
| Volume | units: 18 -> 18, removed 5, added 5 |
| VolumeThermalExpansion | units: 4 -> 4, removed 1, added 1 |
| ConductivityVariance | units: 1 -> 2, removed 1, added 2 |
| LengthTemperatureTime | units: 1 -> 2, removed 1, added 2 |
| MassTemperature | units: 1 -> 2, removed 1, added 2 |
| VolumetricFlux | units: 2 -> 4, removed 2, added 4 |
| SpecificAcousticImpedance | units: 2 -> 2, removed 1, added 1 |
| ReactionRateConstant | units: 2 -> 2, removed 1, added 1 |
| AmountOfSubstancePerMass | units: 11 -> 12, removed 11, added 12 |
| SectionModulus | units: 6 -> 6, removed 5, added 5 |
| MassFlowRate | units: 25 -> 26, removed 6, added 7 |
| MeasurementUnitOfSpectralRadiance | units: 10 -> 10, removed 1, added 1 |
| EnergyCost | units: 13 -> 23, removed 10, added 20 |
| Velocity | units: 24 -> 24, removed 12, added 12 |
| Permeability | units: 3 -> 3, removed 2, added 2 |
| DiffusionCoefficient | units: 3 -> 3, removed 2, added 2 |
| SpecificEnergy | units: 6 -> 7, removed 1, added 2 |
| Unknown | units: 80 -> 102, removed 29, added 51 |
| LinearCompressibility | units: 1 -> 2, removed 1, added 2 |
| MassPerAreaTime | units: 16 -> 20, removed 6, added 10 |
| Energy | units: 27 -> 27, removed 2, added 2 |
| EnergyDensity | units: 3 -> 3, removed 1, added 1 |
| DiffusionCoefficient | units: 3 -> 3, removed 2, added 2 |
| CoefficientOfHeatTransfer | units: 3 -> 4, removed 1, added 2 |
| StressOpticCoefficient | units: 5 -> 6, removed 2, added 3 |
| SpectralRadiantEnergyDensity | units: 7 -> 1, removed 6 |
| ElectrolyticConductivity | units: 12 -> 12, removed 1, added 1 |
| EnergyPerArea | units: 18 -> 20, removed 5, added 7 |
| TorquePerLength | units: 2 -> 2, removed 1, added 1 |
| MassConcentration | units: 27 -> 27, removed 10, added 10 |
| PressureCoefficient | units: 4 -> 4, removed 1, added 1 |
| ElectricChargeVolumeDensity | units: 8 -> 8, removed 5, added 5 |
| Viscosity | units: 4 -> 7, removed 3, added 6 |
| Permittivity | units: 6 -> 6, removed 4, added 4 |
| MomentOfInertia | units: 3 -> 4, removed 3, added 4 |
| Permeability | units: 3 -> 3, removed 2, added 2 |
| SpecificVolume | units: 8 -> 11, removed 8, added 11 |
| BloodGlucoseLevelByMass | units: 17 -> 17, removed 10, added 10 |
| ForcePerAreaTime | units: 4 -> 4, removed 1, added 1 |
| MassPerEnergy | units: 2 -> 3, removed 2, added 3 |
| ParticleFluence | units: 2 -> 3, removed 1, added 2 |
| BurstFactor | units: 1 -> 3, removed 1, added 3 |
| SpecificHeatVolume | units: 1 -> 2, removed 1, added 2 |
| ForcePerArea | units: 14 -> 15, removed 1, added 2 |
| ActivityConcentration | units: 5 -> 5, removed 3, added 3 |
| SpecificOpticalRotatoryPower | units: 1 -> 2, removed 1, added 2 |
| LinearDensity | units: 7 -> 7, removed 1, added 1 |
| RecombinationCoefficient | units: 3 -> 3, removed 2, added 2 |
| ElectromagneticWavePhaseSpeed | units: 8 -> 8, removed 6, added 6 |
| MolarMassVariationDueToPressure | units: 1 -> 2, removed 1, added 2 |
| MolarFluxDensity | units: 6 -> 7, removed 2, added 3 |
| WaterVapourDiffusionCoefficient | units: 1 -> 2, removed 1, added 2 |
| TotalCurrentDensity | units: 5 -> 5, removed 1, added 1 |
| StandardGravitationalParameter | units: 2 -> 2, removed 1, added 1 |
| ParticleFluenceRate | units: 2 -> 3, removed 1, added 2 |
| RotationalFrequency | units: 11 -> 10, removed 1 |
| Conductivity | units: 12 -> 12, removed 1, added 1 |
| Flux | units: 3 -> 4, removed 1, added 2 |
| EnergyPerTemperature | units: 3 -> 3, removed 1, added 1 |
| MassConcentrationRateOfChange | units: 1 -> 2, removed 1, added 2 |
| Power | units: 33 -> 34, removed 5, added 6 |
| LengthEnergy | units: 1 -> 2, removed 1, added 2 |
| BloodGlucoseLevel | units: 7 -> 7, removed 5, added 5 |
| LinearMomentum | units: 3 -> 6, removed 1, added 4 |
| VapourPermeance | units: 3 -> 4, removed 2, added 3 |
| AngularMomentum | units: 5 -> 6, removed 2, added 3 |
| SecondPolarMomentOfArea | units: 3 -> 3, removed 2, added 2 |
| InverseEnergy | units: 1 -> 2, removed 1, added 2 |
| Mobility | units: 2 -> 2, removed 1, added 1 |
| PressureGradient | units: 6 -> 6, removed 2, added 2 |
| KermaRate | units: 5 -> 8, removed 1, added 4 |
| LinearVelocity | units: 24 -> 24, removed 12, added 12 |
| HydraulicPermeability | units: 9 -> 9, removed 5, added 5 |
| PowerPerArea | units: 9 -> 10, removed 2, added 3 |
| ElectricChargeDensity | units: 8 -> 8, removed 5, added 5 |
| ElectricCharge | units: 27 -> 27, removed 2, added 2 |
| SecondMomentOfArea | units: 3 -> 3, removed 2, added 2 |
| MomentOfForce | units: 8 -> 8, removed 3, added 3 |
| MassPerTime | units: 14 -> 14, removed 5, added 5 |
| MassPerArea | units: 19 -> 21, removed 3, added 5 |
| TorquePerAngle | units: 2 -> 3, removed 1, added 2 |
| SpecificModulus | units: 3 -> 4, removed 2, added 3 |
| SpecificActivity | units: 4 -> 7, removed 4, added 7 |
| LinearEnergyTransfer | units: 4 -> 4, removed 2, added 2 |
| SecondAxialMomentOfArea | units: 3 -> 3, removed 2, added 2 |
| Action | units: 2 -> 2, removed 1, added 1 |
| Torque | units: 8 -> 8, removed 3, added 3 |
| ForcePerLength | units: 13 -> 5, removed 9, added 1 |
| DisplacementCurrentDensity | units: 5 -> 5, removed 1, added 1 |
| LengthTemperature | units: 3 -> 4, removed 1, added 2 |
| ElectromagneticEnergyDensity | units: 2 -> 2, removed 1, added 1 |
| SurfaceDensity | units: 12 -> 13, removed 1, added 2 |
| SpecificHeatPressure | units: 1 -> 2, removed 1, added 2 |
| TorsionalSpringConstant | units: 2 -> 3, removed 1, added 2 |
| EnergyFluence | units: 5 -> 5, removed 2, added 2 |
| Density | units: 30 -> 30, removed 10, added 10 |
| PowerPerElectricCharge | units: 3 -> 4, removed 1, added 2 |
| DynamicViscosity | units: 4 -> 7, removed 3, added 6 |
| VolumetricHeatCapacity | units: 3 -> 4, removed 1, added 2 |
| AngularImpulse | units: 5 -> 6, removed 2, added 3 |
| TotalMassStoppingPower | units: 1 -> 2, removed 1, added 2 |
| SoundVolumeVelocity | units: 3 -> 3, removed 2, added 2 |
| RadiantFluence | units: 5 -> 5, removed 2, added 2 |
| Area | units: 10 -> 10, removed 5, added 5 |
| VolumeFlowRate | units: 22 -> 22, removed 11, added 11 |
| VapourPermeability | units: 1 -> 2, removed 1, added 2 |
| LengthMass | units: 2 -> 5, removed 2, added 5 |
| AreaPerTime | units: 5 -> 5, removed 2, added 2 |
| MassRatio | units: 15 -> 15, removed 4, added 4 |
| Entropy | units: 3 -> 3, removed 1, added 1 |
| SpecificPower | units: 8 -> 11, removed 2, added 5 |
| AbsorbedDoseRate | units: 8 -> 11, removed 2, added 5 |
| Unbalance | units: 1 -> 3, removed 1, added 3 |
| CostPerMass | units: 1 -> 2, removed 1, added 2 |
| NuclearQuadrupoleMoment | units: 7 -> 7, removed 5, added 5 |
| SoundExposureLevel | units: 3 -> 2, removed 1 |
| Momentum | units: 3 -> 6, removed 1, added 4 |
| InverseSquareMass | units: 1 -> 2, removed 1, added 2 |
| IonicStrength | units: 11 -> 12, removed 11, added 12 |
| MassSpecificBiogeochemicalRate | units: 4 -> 6, removed 4, added 6 |
| VolumePerTime | units: 22 -> 22, removed 11, added 11 |
| MolarRefractivity | units: 5 -> 5, removed 1, added 1 |
| MassicActivity | units: 4 -> 7, removed 4, added 7 |
| VolumicElectromagneticEnergy | units: 2 -> 2, removed 1, added 1 |
| MassPerLength | units: 7 -> 7, removed 1, added 1 |
| CatalyticActivityConcentration | units: 16 -> 20, removed 9, added 13 |
| ElectricConductivity | units: 13 -> 13, removed 1, added 1 |
| BatteryCapacity | units: 5 -> 5, removed 2, added 2 |
| Mass | units: 20 -> 19, removed 1 |
| RadiantEnergyDensity | units: 2 -> 2, removed 1, added 1 |
| Impulse | units: 1 -> 4, removed 1, added 4 |
| AreaTime | units: 2 -> 4, removed 2, added 4 |
| Acceleration | units: 4 -> 4, removed 1, added 1 |
| PressureLossPerLength | units: 1 -> 2, removed 1, added 2 |
| MassDensity | units: 30 -> 30, removed 10, added 10 |
| ExposureRate | units: 1 -> 2, removed 1, added 2 |
| PhotosyntheticPhotonFluxDensity | units: 11 -> 12, removed 4, added 5 |
| TotalLinearStoppingPower | units: 4 -> 4, removed 2, added 2 |
| LineicMass | units: 7 -> 7, removed 1, added 1 |
| ElectricCurrentDensity | units: 5 -> 5, removed 1, added 1 |

