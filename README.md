# The-Ultimate-Ball-by_Ball-Cricket-Dataset

![Cricket Dataset Banner](https://img1.hscicdn.com/image/upload/f_auto,t_ds_w_1280,q_80/lsci/db/PICTURES/CMS/325900/325966.jpg)

## 🧠 Overview

The objective of this project is to build one of the most **comprehensive open-source cricket datasets**, containing **ball-by-ball data enriched with detailed commentary-based features** such as:

- Ball Line (e.g., outside off, on middle)
- Ball Length (e.g., full, short, good length)
- Shot Played (e.g., drive, sweep, pull)
- Shot Direction (e.g., mid-wicket, third man, long off)

The dataset spans each ball of all International matches across formats and all IPL/WPL matches from **2003 to 2025**, combining traditional sources (like Cricsheet) with scraped and parsed data from **ESPNcricinfo**. This work took **over 3 months** of continuous scraping, cleaning, and validation, from the publicly available data, ensuring ~95% data accuracy.

## 🔗 Dataset Source

The base data was sourced and enriched from the following:

- 📊 **Ball-by-ball & match metadata**: [Cricsheet](https://cricsheet.org/)  
- 📋 **Player metadata & commentary**: [ESPNcricinfo](https://www.espncricinfo.com/)

## 🔧 Data Collection & Preprocessing

This dataset was built through a layered pipeline involving scraping, automation, and parsing:

- **Match Metadata**: Combined Cricsheet’s structured data with match info from the same source.
- **Player Metadata**: Scraped from ESPN using unique player IDs via BeautifulSoup.
- **Fixtures Scraping**:
  - Manually downloaded HTML pages for all seasons (2003–2025).
  - Extracted ~10,000 series links from those files.
- **Match & Commentary Extraction**:
  - Used Selenium to open and scroll ~80,000 match links.
  - Saved the HTML for matches with commentary (~9,000).
  - Parsed ball-by-ball commentary for ~4,000 matches with rich features.

## 🧪 Data Preview
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>match_id</th>
      <th>season</th>
      <th>start_date</th>
      <th>venue</th>
      <th>innings</th>
      <th>ball</th>
      <th>batting_team</th>
      <th>bowling_team</th>
      <th>striker</th>
      <th>non_striker</th>
      <th>bowler</th>
      <th>ball_length</th>
      <th>ball_line</th>
      <th>shot_played</th>
      <th>shot_direction</th>
      <th>runs_off_bat</th>
      <th>extras</th>
      <th>wides</th>
      <th>noballs</th>
      <th>byes</th>
      <th>legbyes</th>
      <th>penalty</th>
      <th>wicket_type</th>
      <th>player_dismissed</th>
      <th>other_wicket_type</th>
      <th>other_player_dismissed</th>
      <th>wicket</th>
      <th>striker balls faced</th>
      <th>total striker runs</th>
      <th>player out runs</th>
      <th>player out balls faced</th>
      <th>gender</th>
      <th>event</th>
      <th>match_number</th>
      <th>toss_winner</th>
      <th>toss_decision</th>
      <th>player_of_match</th>
      <th>player_of_match.1</th>
      <th>winner</th>
      <th>winner_runs</th>
      <th>winner_wickets</th>
      <th>outcome</th>
      <th>format</th>
      <th>type</th>
      <th>full name_striker</th>
      <th>country_striker</th>
      <th>batting style_striker</th>
      <th>bowling style_striker</th>
      <th>playing role_striker</th>
      <th>major teams_striker</th>
      <th>image url_striker</th>
      <th>full name_bowler</th>
      <th>country_bowler</th>
      <th>batting style_bowler</th>
      <th>bowling style_bowler</th>
      <th>playing role_bowler</th>
      <th>major teams_bowler</th>
      <th>image url_bowler</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>126308</th>
      <td>1473446</td>
      <td>2025</td>
      <td>2025-03-29</td>
      <td>Narendra Modi Stadium, Ahmedabad</td>
      <td>1</td>
      <td>6.4</td>
      <td>Gujarat Titans</td>
      <td>Mumbai Indians</td>
      <td>B Sai Sudharsan</td>
      <td>Shubman Gill</td>
      <td>HH Pandya</td>
      <td>full</td>
      <td>outside off</td>
      <td>drive</td>
      <td>sweeper cover</td>
      <td>1</td>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0</td>
      <td>22.0</td>
      <td>34.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>Indian Premier League</td>
      <td>9.0</td>
      <td>Mumbai Indians</td>
      <td>field</td>
      <td>M Prasidh Krishna</td>
      <td>NaN</td>
      <td>Gujarat Titans</td>
      <td>36.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>T20</td>
      <td>Fran(IPL)</td>
      <td>Bhardwaj Sai Sudharsan</td>
      <td>India</td>
      <td>Left hand Bat</td>
      <td>Legbreak</td>
      <td>Top order Batter</td>
      <td>India, Gujarat Titans, Chepauk Super Gillies, ...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Hardik Himanshu Pandya</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Medium fast</td>
      <td>Allrounder</td>
      <td>India, Mumbai Indians, Baroda, Gujarat Titans,...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
    </tr>
    <tr>
      <th>2510857</th>
      <td>1447493</td>
      <td>2024</td>
      <td>2024-09-06</td>
      <td>YSD-UKM Cricket Oval, Bangi</td>
      <td>2</td>
      <td>8.1</td>
      <td>Singapore</td>
      <td>Kuwait</td>
      <td>WA Simpson</td>
      <td>AE Paraam</td>
      <td>Shiraz Khan</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0</td>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0</td>
      <td>13.0</td>
      <td>8.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>ICC Men's T20 World Cup Asia Qualifier A</td>
      <td>17.0</td>
      <td>Singapore</td>
      <td>field</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Singapore</td>
      <td>NaN</td>
      <td>5.0</td>
      <td>NaN</td>
      <td>T20</td>
      <td>Intl</td>
      <td>William Arlington Simpson</td>
      <td>Singapore</td>
      <td>Right hand Bat</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Singapore</td>
      <td>NaN</td>
      <td>Shiraz Khan Shereef</td>
      <td>Kuwait</td>
      <td>Right hand Bat</td>
      <td>Legbreak Googly</td>
      <td>Allrounder</td>
      <td>Kuwait</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
    </tr>
    <tr>
      <th>1160832</th>
      <td>300426</td>
      <td>2007/08</td>
      <td>2007-12-26</td>
      <td>Eden Park</td>
      <td>1</td>
      <td>25.6</td>
      <td>Bangladesh</td>
      <td>New Zealand</td>
      <td>Mohammad Ashraful</td>
      <td>Tamim Iqbal</td>
      <td>DL Vettori</td>
      <td>NaN</td>
      <td>outside off</td>
      <td>drive</td>
      <td>deep extra cover</td>
      <td>1</td>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0</td>
      <td>48.0</td>
      <td>57.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>Bangladesh in New Zealand ODI Series</td>
      <td>1.0</td>
      <td>New Zealand</td>
      <td>field</td>
      <td>JM How</td>
      <td>NaN</td>
      <td>New Zealand</td>
      <td>NaN</td>
      <td>6.0</td>
      <td>NaN</td>
      <td>ODI</td>
      <td>Intl</td>
      <td>Mohammad Ashraful</td>
      <td>Bangladesh</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak, Legbreak</td>
      <td>Middle order Batter</td>
      <td>Bangladesh, Asia XI, Bangladesh A, Central Zon...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Daniel Luca Vettori</td>
      <td>New Zealand</td>
      <td>Left hand Bat</td>
      <td>Slow Left arm Orthodox</td>
      <td>Allrounder</td>
      <td>New Zealand, Delhi Daredevils, ICC World XI, J...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
    </tr>
    <tr>
      <th>2460743</th>
      <td>1435632</td>
      <td>2024</td>
      <td>2024-06-03</td>
      <td>Gahanga International Cricket Stadium, Rwanda</td>
      <td>1</td>
      <td>9.6</td>
      <td>Botswana</td>
      <td>Nigeria</td>
      <td>L Mophakedi</td>
      <td>P Mapotsane</td>
      <td>L Piety</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4</td>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0</td>
      <td>31.0</td>
      <td>22.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>female</td>
      <td>Kwibuka Women's Twenty20 Tournament</td>
      <td>15.0</td>
      <td>Botswana</td>
      <td>bat</td>
      <td>L Piety</td>
      <td>NaN</td>
      <td>Nigeria</td>
      <td>NaN</td>
      <td>9.0</td>
      <td>NaN</td>
      <td>T20</td>
      <td>Intl</td>
      <td>Laura Mophakedi</td>
      <td>Botswana</td>
      <td>Right hand Bat</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Botswana Women</td>
      <td>NaN</td>
      <td>Lucky Piety</td>
      <td>Nigeria</td>
      <td>Right hand Bat</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Nigeria Women, Nigeria Women Under-19s</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
    </tr>
    <tr>
      <th>2836564</th>
      <td>1062575</td>
      <td>2016/17</td>
      <td>2017-03-16</td>
      <td>JSCA International Stadium Complex</td>
      <td>2</td>
      <td>175.5</td>
      <td>India</td>
      <td>Australia</td>
      <td>WP Saha</td>
      <td>CA Pujara</td>
      <td>JR Hazlewood</td>
      <td>bouncer</td>
      <td>NaN</td>
      <td>ramp</td>
      <td>third man</td>
      <td>2</td>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0</td>
      <td>172.0</td>
      <td>78.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>Border-Gavaskar Trophy</td>
      <td>3.0</td>
      <td>Australia</td>
      <td>bat</td>
      <td>CA Pujara</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>draw</td>
      <td>TEST</td>
      <td>Intl</td>
      <td>Wriddhiman Prasanta Saha</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>NaN</td>
      <td>Wicketkeeper Batter</td>
      <td>India, Gujarat Titans, All India Electricity B...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Josh Reginald Hazlewood</td>
      <td>Australia</td>
      <td>Left hand Bat</td>
      <td>Right arm Fast medium</td>
      <td>Bowler</td>
      <td>Australia, AJ Finch's XI, Australia A, Austral...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
    </tr>
  </tbody>
</table>
</div>

### A Note on Completeness:

Not all matches in the original Cricsheet dataset had commentary, and among those with commentary, not all contained detailed information such as line, length, shot played, or direction. Only about 4,000 matches had these detailed attributes, and even then, not all had all four details.

## 🧠 Tools & Techniques

- **Scraping & Automation**: `BeautifulSoup`, `Selenium`  
- **Parsing & Transformation**: `Python`, `Pandas`, `Regex`  
- **Validation**: Manual reviews and sampling

## ✅ Results & Quality

This project delivers one of the most detailed and high-quality cricket datasets available for public use. By combining Cricsheet’s structured ball-by-ball data with commentary-derived features from ESPNcricinfo.

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Contact

For any queries or contributions, feel free to reach out to:
- **Ariharasudhan A** – [Email](mailto:ariadaikalam1234@gmail.com)  
- **Harish R** – [Email](mailto:harishsekar2004@gmail.com)
