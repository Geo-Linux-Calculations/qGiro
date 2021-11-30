![GitHub release (latest by date)](https://img.shields.io/github/v/release/Geo-Linux-Calculations/qGiro)
![GitHub Release Date](https://img.shields.io/github/release-date/Geo-Linux-Calculations/qGiro)
![GitHub repo size](https://img.shields.io/github/repo-size/Geo-Linux-Calculations/qGiro)
![GitHub all releases](https://img.shields.io/github/downloads/Geo-Linux-Calculations/qGiro/total)
![GitHub](https://img.shields.io/github/license/Geo-Linux-Calculations/qGiro)

# qGiro  
#### Author: Oleg  M.Kosorukov  
#### Version 0.3

#### Data processing program for orientation of the underground mine surveyor base.

The orientation of the side of underground polygonometry is performed using a gyrotheodolite with two gyro blocks and consists of:
- determination of the gyrotheodolite correction on the side with a known directional angle (work on the surface);
- determination of the directional angle of the oriented side of the underground polygonometry (work in the tunnel under construction);
- re-determination of the gyrotheodolite correction on the side with a known directional angle (work on the surface).
All measurements are taken by each gyro unit.

#### Methodology
The determination of the gyrotheodolite correction was carried out before and after the determination of the gyroscopic azimuth of the side of the underground polygonometry, on the sides of the ground polygonometry.
The essence of determining the constant correction (∆) is to determine the angle between the known directional angle of ground polygonometry of the planned reference justification and the gyroscopic azimuth determined by the gyrotheodolite.
The determination of the gyroscopic azimuth of the sides was carried out in accordance with paragraph 8.30. VSN 160-69, chapter 6.3.2 SP 120.13330.2012 "Subways. Updated edition of SNiP 32-02-2003".

The determination of the gyrotheodolite correction was carried out directly at the points of the planning justification, and the gyroscopic azimuth of the side of the underground polygonometry is performed "eccentrically",
i.e. the gyrotheodolite was installed not over the point of underground polygonometry, but at an arbitrary point in the immediate vicinity of it. When determining the azimuth, the directions to the points of polygonometry
and the distances to them are measured. The Aghir azimuth (vts) is corrected by ∆А.

As a result of the work performed, the gyroscopic azimuths of the sides of the underground polygonometry of the forward and backward directions should be determined.
The discrepancies in the values ​​of the calculated directional angle of the underground line, determined from several orientations, should not exceed 20"
(clause 8.58. VSN 160-69, chapter 6.3.2 SP 120.13330.2012" Subways. Updated edition of SNiP 32-02-2003).

#### Tab "Оформление":
Contains information about the date of measurement, the number of the gyrotheodolite and both gyro blocks.
- Theme - not used
- Letter - The number of the letter from the date and the name of the company that sent the application for implementation
- Header and footer - Information placed in the header
- Introduction - Information placed at the beginning of the report, which provides basic information

#### Tab "Наземные измерения":
- Latitude - Geographic latitude, accurate to 4 digits
- Points of ground polygonometry, coordinates and measured azimuth in both directions

#### Tab "Подземные из-я"
- Points of underground polygonometry
- X and Y coordinates
- measured azimuth by each gyro unit in both directions
- eccentric angle, if not needed you can put 0 00 00.0

#### Tab "Расчет" 
- All obtained directional angles from corrections and measured gyroscopic azimuth
- average value and difference with a tolerance for each gyro unit
- the average directional angle from all measurements and the difference with the directional angle from polygonometry.
- determination accuracy

#### Window "Лог работы программы" 
- all input data with checking the correctness of the entered azimuths
- calculation of corrections
- data and formula for calculating each directional angle from the amendments

#### Button "Вычислить"
- performs all calculations
- saves in detail each stage in the log window

#### Button "Отчет"
- reads the template file "templateFull.docx" from the root of the program folder
- fills in with calculated values
- saves to "C: \ WINDOWS \ Temp \ OtchetFull.docx"
- opens the saved report in WORD, if it is installed (checked in Office 2013)

#### TO-DO:
- Move the template "templateFull.docx" from the program folder to the user's folder "My Documents"
- Transfer the file "OtchetFull.docx" with the result to the user's folder.
- Add additional properties of the underground polygonometry point, "Ring number" and "Station" to the program and template.
