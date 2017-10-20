# data2csv
Parse bulk output files into a single CSV file

## Usage

    data2csv example.ini filelist.txt

Using ini format, example

```ini
[G4]
grep=grep --text "G4 Enthalpy="
unit=Hartree
folder=jobs/g4/
extension=out
indexcol=0
indexrow=0

[thermcorr]
grep=grep --text "Thermal correction to Enthalpy="
unit=Hartree
folder=jobs/b3lyp6311gdp-freq-scale/
extension=out
indexcol=0
indexrow=-1

[PM6]
grep=grep --text "FINAL HEAT OF FORMATION"
unit=kcal/mol
folder=jobs/pm6/
extension=out
indexcol=0
indexrow=0
```

will give col names

    G4 [Hartree], thermcorr [Hartree], PM6


