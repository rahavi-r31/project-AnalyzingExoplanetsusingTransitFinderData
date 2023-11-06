# Data Analysis Project for Internship

## 1. Project Overview 📝

- **Project Title**: Analyzing Exoplanets using Transit Finder Data
- **Goal of the project**: **Predict Future Transits:** Using the transit epoch and period, you can predict when future transits will occur.
- **Dataset(s) used**: TESS Objects of Interest (6873 TOIs; [CSV file](https://astro.swarthmore.edu/transits/toi_targets.csv))
- **Team Members**: Rahavi S

## 2. Data Overview 📁

- **Source(s) of the Data**:
    
    Kepler mission: This NASA mission observed thousands of stars over several years, looking for transits, or tiny dips in a star's brightness that may indicate the presence of a planet.
    TESS (Transiting Exoplanet Survey Satellite): Another NASA mission, TESS is surveying the entire sky to find exoplanets around nearby bright stars.
    UKIRT (United Kingdom Infrared Telescope) Microlensing Survey: This survey looked for exoplanets using the technique of gravitational microlensing, which occurs when the gravitational field of a planet bends the light from a distant star.
    
- **Data Size**: 1.15MB
- **Brief Description of the Data**: The TESS Objects of Interest (TOI) data set is a collection of the most promising exoplanet candidates identified by the Transiting Exoplanet Survey Satellite (TESS) during its prime mission. The data set includes parameters such as the size and brightness of the exoplanet candidates, as well as information about their orbits and potential host stars. The TOI data set is vetted by the TESS Science Office and deemed to be promising candidates for further study. The TOI catalog is updated regularly as new data is collected by TESS, and it is used by astronomers to identify potential exoplanets for further investigation. It's an important resource for understanding the diversity of exoplanets and their potential habitability.

## 3. Data Cleaning and Preparation 🔧

- **Missing Value Treatment**: ignore
- **Outlier Detection & Treatment**: -
- **Feature Engineering**: 1.Add Time Since Last Transit  2.

## 4. Exploratory Data Analysis 🕵️‍♀️

- Predicting future transits of an exoplanet is an essential part of exoplanetary research, as it allows astronomers to plan observations, gather more data, and study the exoplanet's behavior over time. To predict future transits using the transit epoch and orbital period, you can follow these steps:
    1. **Understand the Basics**:
        - **Transit Epoch (\(epoch\))**: This is the reference time at which a specific transit event occurred. It represents the center of a transit and is typically given in Julian Date (JD) or Gregorian Date.
        - **Orbital Period (\(period\))**: This is the time it takes for the exoplanet to complete one orbit around its host star, typically measured in days.
    2. **Calculate the Time Since Last Transit**:
        - First, calculate the time that has passed since the last observed transit. This is done by subtracting the transit epoch from the current date or the date from which you want to predict future transits.
        - For example, if the last observed transit of an exoplanet occurred at \(epoch = 2458723.383\) JD, and today's date is \(JD = 2459324.678\), you would calculate the time elapsed since the last transit as:
            
            \[ \text{Time Since Last Transit} = 2459324.678 - 2458723.383 \]
            
    3. **Calculate the Number of Orbits Completed**:
        - Next, divide the time since the last transit by the orbital period to determine how many complete orbits have occurred during that time.
        - For example, if the orbital period is \(period = 0.73654604\) days, you would calculate the number of orbits as:
            
            \[ \text{Number of Orbits Completed} = \frac{\text{Time Since Last Transit}}{0.73654604} \]
            
    4. **Calculate the Next Transit Epoch**:
        - To predict the next transit epoch, add the number of orbits completed to the last transit epoch. This will give you the expected epoch of the next transit event.
        - In our example, if you found that 14.45 orbits have been completed since the last transit, you would calculate the next transit epoch as:
            
            \[ \text{Next Transit Epoch} = 2458723.383 + (14.45 \times 0.73654604) \]
            
    5. **Confirm and Refine Predictions**:
        - It's important to keep in mind that this calculation assumes that the exoplanet's orbit is perfectly periodic, with no perturbations or variations in the orbital period. In reality, exoplanet orbits may be influenced by gravitational interactions with other planets, leading to variations in the orbital period.
        - To make more accurate predictions, consider using more sophisticated models that account for potential variations in the orbital period.
    6. **Plan Observations**:
        - Once you have predicted the next transit epoch, you can plan observations to confirm the prediction and study the upcoming transit event. This might involve scheduling telescope time or preparing for data collection.

## 7. Final Report and Presentation 📑

- **Key Findings**: We have found next transit event using data available
- **Recommendations and Next Steps**: Efficiently plan observation schedule

## 8. References and Data Sources 📚

- **Dataset Links**: [https://astro.swarthmore.edu/transits/toi_targets.csv](https://astro.swarthmore.edu/transits/toi_targets.csv)
- **Research Papers or Articles Referenced**:

## 9. Project Files 📂

- **EDA Code Files**:

[GitHub - rahavi-r31/project-AnalyzingExoplanetsusingTransitFinderData](https://github.com/rahavi-r31/project-AnalyzingExoplanetsusingTransitFinderData)
