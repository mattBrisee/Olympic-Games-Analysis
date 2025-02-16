# Analysis of Olympic sports and medals (1896 - 2012)

Data link: [Olympic Summer Data](https://www.kaggle.com/datasets/the-guardian/olympic-games?select=summer.csv)

## A brief overview

This report generated in Python using pandas library aims at analysis of Olympic games in 1896 - 2012 period.The parent dataset contains three csv files: summer.csv, winter.csv and dictionary.csv; however, this analysis pertains to the summer games only.

## Data in a glance

This analysis integrates nine distinct datasets, each capturing different aspects of road incidents: comprehensive accident details, vehicle specifications, personal information of involved parties, event sequences, precise location data, weather conditions at the time of accidents, detailed crash configurations (sub DCA), intersection/node information, and road surface characteristics.

## Reports

Power BI was used to analysis and generate reports about all aspects of road crashes. The reports are organised into four distinct pages shown here:

1- Accidents by Date and Time

<img width="605" alt="Image" src="https://github.com/user-attachments/assets/4c97764b-beb9-420d-89d7-533b1f720b27" />

2- Casualties Status

<img width="599" alt="Image" src="https://github.com/user-attachments/assets/185673d8-afd5-4dca-8dc6-59d7e7009459" />

3- Accident Location and Road and Environmental Conditions

<img width="605" alt="Image" src="https://github.com/user-attachments/assets/bde78a18-7742-4698-9717-07adf3d02627" />

4-Accident Category and Sub-category Contributors

<img width="603" alt="Image" src="https://github.com/user-attachments/assets/db249d72-3cda-4fb1-8be9-c7247009428b" />

Model schema is also shown below:

<img width="691" alt="Image" src="https://github.com/user-attachments/assets/654f7916-d65f-4574-b85b-bc1ed2833f53" />


### Analysis Insights

Analysis of the temporal patterns in the accident data reveals the following key findings:

1. Monthly Variations:
- March had the highest number of total accidents (17,483) and injuries (22,323)
- June had the lowest number of total accidents (13,589) and injuries (17,405)
- November recorded the highest number of fatalities (284)

2. Daily and Hourly Patterns:
- Weekdays show consistent high-risk periods during:
  * Morning peak (8:00-9:00 AM)
  * Afternoon/evening peak (3:00-7:00 PM)
- Weekends display different patterns with:
  * Higher accident concentrations between 11:00 AM-3:00 PM
  * Generally lower early morning incidents

Long-term Trends:

1. Accident Fluctuations:
- Notable peak around 2016 across multiple months
- Significant dip in 2020 (likely due to COVID-19 restrictions)
- Recovery trend post-2020 with numbers increasing again

2. Injury and Fatality Patterns:
- Injury numbers generally follow accident patterns
- Fatality rates show more variation and don't always correlate directly with accident numbers
- The ratio of injuries to accidents remains relatively consistent (approximately 1.3 injuries per accident)

Overall Statistics (Averages across months):
- Monthly accidents: ~14,000-17,000
- Monthly injuries: ~17,000-22,000
- Monthly fatalities: ~230-300

Time-based Risk Patterns:

1. High-Risk Periods:
- Highest accident volumes: 15:00-16:00 (9,164 car accidents)
- Morning peak: 7:00-8:00 (4,731 car accidents)
- Evening peak: 17:00-18:00 (9,755 car accidents)
- Lowest accident volumes: Late night/early morning (23:00-0:00 with 2,168 car accidents)

2. Road User Distribution:
- Drivers make up the largest proportion throughout the day:
  * Highest: Early morning (65%+ during 5:00-7:00)
  * Lowest: Night hours (54-56% during 20:00-23:00)
- Passenger involvement shows interesting patterns:
  * Highest: Late night (28-29% during 22:00-23:00)
  * Lowest: Morning rush (14-15% during 6:00-7:00)

3. Vulnerable Road Users:
- Pedestrians:
  * Fairly consistent (4-6% throughout the day)
  * Slightly higher representation during evening hours (5-6%)
- Cyclists:
  * Peak during morning commute (9-10% during 7:00-9:00)
  * Lower during night hours (minimal presence 22:00-0:00)
- Motorcyclists:
  * Higher representation during midday and afternoon (7-9%)
  * Lower during late night/early morning hours (4-5%)

4. Age and Gender Patterns:
- Young adults (18-29):
  * Highest involvement during night hours
  * Male predominance more pronounced during these hours
- Children (0-17):
  * Higher proportion during school transport hours
  * More balanced gender distribution
- Elderly (70+):
  * Higher vulnerability during daylight hours
  * Lower involvement during night hours

5. Vehicle Type Distribution:
- Cars consistently lead in accidents across all hours
- Station wagons maintain second position
- Night-time differences:
  * Lower bicycle involvement
  * Reduced utility vehicle presence
  * Proportionally higher car involvement

Key Safety Implications:
1. Need for enhanced safety measures during peak commute hours
2. Special focus on young male drivers during night hours
3. Protection of vulnerable road users during their peak activity times
4. Different risk profiles between day and night requiring targeted interventions
5. School transport hours requiring specific safety protocols

These patterns suggest the need for time-specific safety strategies rather than one-size-fits-all approaches to road safety management.

Notable points:
- The seasonal effect is evident with higher incidents during certain months
- There's a clear pattern of reduced accidents during early morning hours (2:00-5:00 AM)
- The recovery pattern post-2020 suggests returning to pre-pandemic levels
- The data shows a consistent relationship between accident times and daily routines (work commutes, school runs, etc.)

Geographic and Temporal Distribution:

1. Urban-Rural Pattern Over 24 Hours:
- Melbourne Urban dominance varies significantly:
  * Highest: Evening period (18:00-19:00) at 69.71%
  * Night hours (20:00-23:00) remains high at 64-66%
  * Early morning (3:00-4:00) shows lowest urban concentration
- Rural Victoria shows inverse pattern:
  * Peaks during early morning hours (24-30%)
  * Lowest during evening rush (15-19%)
  * Maintains 20-22% share during late night hours

2. Time-Based Risk Patterns:
- Peak accident times:
  * Afternoon peak (15:00-16:00): 9,164 car accidents
  * Evening rush (17:00-18:00): 9,755 car accidents
  * Morning peak (7:00-8:00): 4,731 car accidents
- Lowest accident volumes:
  * Late night/early morning (23:00-00:00): 2,168 accidents
  * Pre-dawn hours (2:00-4:00): Similar low volumes

3. Road Surface Conditions:
- Consistent patterns across 24 hours:
  * Dry conditions dominate accident numbers
  * Wet conditions show secondary but significant impact
  * Minimal incidents in extreme conditions (icy/snowy)
- Location categories remain consistent:
  * Intersections (cross, T, Y) show high incident rates
  * Non-intersection accidents form significant portion
  * Dead ends consistently show lower rates

4. Regional Distribution:
- Large Provincial Cities (4-6%):
  * Relatively stable throughout 24 hours
  * Slight increase during business hours
- Small Cities and Towns (combined 5-8%):
  * Higher percentages during daylight hours
  * Reduced representation at night

5. Spatial Clustering:
- Melbourne Metropolitan Area:
  * Dense concentration in CBD and inner suburbs
  * Major arterial routes show consistent patterns
  * Outer suburban areas show time-dependent variation
- Regional Areas:
  * Highway corridors show consistent activity
  * Regional centers have distinct patterns
  * Coastal areas show notable accident clusters

Key Safety Implications:

1. Time-Based Interventions:
- Enhanced enforcement during peak hours
- Special attention to late-night rural driving
- Early morning urban-rural transition period monitoring

2. Geographic Focus:
- Targeted urban strategies for peak hours
- Rural-specific interventions for high-risk periods
- Regional center-specific approaches

3. Infrastructure Priorities:
- Intersection safety improvements
- Wet weather management systems
- Rural road safety enhancements

4. Resource Allocation:
- Time-based emergency response positioning
- Geographic distribution of safety resources
- Weather-dependent intervention strategies

Accident Volume Pattern:

1. Type of Accidents by Time:

Daytime (6:00-18:00):
- Dominated by vehicle-to-vehicle collisions
- High rear-end collision rates (3,000+ during peak hours)
- Significant cross-traffic incidents at intersections

Evening (18:00-22:00):
- Vehicle collisions remain primary (3,089-4,659)
- Increased fixed object collisions (983-1,068)
- Higher pedestrian incidents (548-741)

Late Night (22:00-4:00):
- Higher proportion of fixed object collisions
- Increased animal-related incidents
- Single vehicle accidents more common

2. High-Risk Behaviors:

Peak Hours:
- Rear-end collisions (highest during 16:00-18:00)
- Intersection violations
- Multiple vehicle incidents

Evening Hours:
- Left/right off carriageway incidents increase
- Out-of-control vehicle incidents rise
- Cross traffic at intersections remains significant

Late Night:
- Fixed object collisions become more prevalent
- Vehicle control issues increase
- Higher proportion of single-vehicle accidents

3. Vulnerable Road Users:

Pedestrians:
- Highest risk during evening peak (15:00-19:00)
- Significant numbers during night (500+ between 20:00-22:00)
- Lower but still concerning numbers in early morning

Animals:
- Increased incidents during dawn/dusk
- Peak during early morning hours
- Higher proportion of total accidents at night

4. Safety Implications:

Time-Based Interventions:
- Enhanced traffic management during 15:00-18:00
- Specific night-time safety measures (22:00-4:00)
- Early morning vigilance (especially for animal incidents)

Risk Management:
- Focused intersection control during peak hours
- Enhanced lighting and signage for night hours
- Special attention to pedestrian areas during evening hours

Geographic Considerations:
- Urban areas need peak hour management
- Rural areas need night-time safety measures
- Suburban areas need balanced approach

This comprehensive analysis suggests that different risk factors dominate at different times, requiring varied safety approaches throughout the day. The transition from peak to off-peak hours shows clear patterns in both the volume and nature of accidents, with distinct characteristics during night hours versus day hours.

The data clearly demonstrates the need for time-specific safety interventions, with particular attention to the distinct challenges presented during peak hours, evening transition periods, and late-night/early morning hours.

## Summary and coclusion

Victoria's road accident analysis reveals distinct temporal patterns with critical peaks during afternoon hours (15:00-18:00) accounting for approximately 14,400 accidents daily, followed by morning rush (8:00-9:00) with 11,146 accidents. The urban-rural distribution shows Melbourne dominating evening accidents (69.71% during 18:00-19:00) while rural areas peak in early mornings (24-30%). Vehicle-to-vehicle collisions, particularly rear-end incidents, dominate peak hours with 3,500+ cases during 17:00-18:00, while fixed object collisions and animal strikes increase significantly during night hours (22:00-04:00). Young adults (18-29) show highest night-time risk, while vulnerable road users follow specific patterns: cyclists peak during morning commute (9-10% of accidents), and pedestrians face highest risk during evening peak (15:00-19:00). Monthly data indicates March as the riskiest month (17,483 accidents, 22,323 injuries) and June as safest (13,589 accidents). Key recommendations include: implementing smart traffic systems and variable speed limits during peak hours, enhancing street lighting and DUI enforcement for night hours (22:00-04:00), establishing time-based emergency response positioning, and developing targeted interventions for specific user groups (school zones, cyclist lanes, pedestrian crossings). The most critical infrastructure priorities should focus on intersection safety improvements, wet weather management systems, and enhanced road marking visibility for night driving.
