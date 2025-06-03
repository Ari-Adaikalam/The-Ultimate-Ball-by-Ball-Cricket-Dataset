# The-Ultimate-Ball-by_Ball-Cricket-Dataset

![Cricket Dataset Banner](https://img1.hscicdn.com/image/upload/f_auto,t_ds_w_1280,q_80/lsci/db/PICTURES/CMS/325900/325966.jpg)

## 🧠 Overview

The objective of this project is to build one of the most **comprehensive open-source cricket datasets**, containing **ball-by-ball data enriched with detailed commentary-based features** such as:

- Ball Line (e.g., outside off, on middle)
- Ball Length (e.g., full, short, good length)
- Shot Played (e.g., drive, sweep, pull)
- Shot Direction (e.g., mid-wicket, third man, long off)

The dataset spans each ball of all International matches across formats and all IPL/WPL matches from **2003 to 2025**, combining traditional sources (like Cricsheet) with scraped and parsed data from **ESPNcricinfo**. This work took **over 3 months** of continuous scraping, cleaning, and validation, from the publicly available data, ensuring ~95% data accuracy.

---

## 🔗 Dataset Source

The base data was sourced and enriched from the following:

- 📊 **Ball-by-ball & match metadata**: [Cricsheet](https://cricsheet.org/)  
- 📋 **Player metadata & commentary**: [ESPNcricinfo](https://www.espncricinfo.com/)

---

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

---

## 🧪 Data Preview
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
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
      <th>player_of_match.1</th>
      <th>ball_length</th>
      <th>ball_line</th>
      <th>shot_played</th>
      <th>shot_direction</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>486669</th>
      <td>1157757</td>
      <td>2018/19</td>
      <td>2018-10-29</td>
      <td>Brabourne Stadium</td>
      <td>1</td>
      <td>0.1</td>
      <td>India</td>
      <td>West Indies</td>
      <td>RG Sharma</td>
      <td>S Dhawan</td>
      <td>KAJ Roach</td>
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
      <td>1.0</td>
      <td>4.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>West Indies tour of India</td>
      <td>4.0</td>
      <td>India</td>
      <td>bat</td>
      <td>RG Sharma</td>
      <td>India</td>
      <td>224.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>ODI</td>
      <td>Intl</td>
      <td>Rohit Gurunath Sharma</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak</td>
      <td>Top order Batter</td>
      <td>India, Mumbai, Mumbai Indians, Air India, Decc...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Kemar Andre Jamal Roach</td>
      <td>West Indies</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast medium</td>
      <td>Bowler</td>
      <td>West Indies, Antigua Hawksbills, Barbados, Bri...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>short</td>
      <td>outside off</td>
      <td>cut</td>
      <td>point</td>
    </tr>
    <tr>
      <th>2666167</th>
      <td>565820</td>
      <td>2012</td>
      <td>2012-09-11</td>
      <td>MA Chidambaram Stadium, Chepauk</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>New Zealand</td>
      <td>G Gambhir</td>
      <td>V Kohli</td>
      <td>KD Mills</td>
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
      <td>1.0</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>New Zealand in India T20I Series</td>
      <td>2.0</td>
      <td>India</td>
      <td>field</td>
      <td>BB McCullum</td>
      <td>New Zealand</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>T20</td>
      <td>Intl</td>
      <td>Gautam Gambhir</td>
      <td>India</td>
      <td>Left hand Bat</td>
      <td>Legbreak</td>
      <td>Top order Batter</td>
      <td>India, Delhi, Delhi Daredevils, Essex, India C...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Kyle David Mills</td>
      <td>New Zealand</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast medium</td>
      <td>Bowler</td>
      <td>New Zealand, Auckland, Kings XI Punjab, Lincol...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>outside off</td>
      <td>NaN</td>
      <td>on side</td>
    </tr>
    <tr>
      <th>1118215</th>
      <td>267708</td>
      <td>2006/07</td>
      <td>2007-01-27</td>
      <td>MA Chidambaram Stadium, Chepauk</td>
      <td>1</td>
      <td>0.1</td>
      <td>India</td>
      <td>West Indies</td>
      <td>RV Uthappa</td>
      <td>G Gambhir</td>
      <td>JE Taylor</td>
      <td>0</td>
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
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>West Indies in India ODI Series</td>
      <td>3.0</td>
      <td>West Indies</td>
      <td>field</td>
      <td>MN Samuels</td>
      <td>West Indies</td>
      <td>NaN</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>ODI</td>
      <td>Intl</td>
      <td>Robin Venu Uthappa</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Medium</td>
      <td>Batter</td>
      <td>India, Air India, Air India Red, Atlanta Rider...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Jerome Everton Taylor</td>
      <td>West Indies</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast</td>
      <td>Bowler</td>
      <td>West Indies, Jamaica, Jamaica Tallawahs, Kings...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>good length</td>
      <td>on off stump</td>
      <td>defense</td>
      <td>off side</td>
    </tr>
    <tr>
      <th>507090</th>
      <td>1172161</td>
      <td>2018/19</td>
      <td>2019-02-25</td>
      <td>Wankhede Stadium</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>England</td>
      <td>JI Rodrigues</td>
      <td>S Mandhana</td>
      <td>KH Brunt</td>
      <td>0</td>
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
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>female</td>
      <td>England Women tour of India</td>
      <td>2.0</td>
      <td>England</td>
      <td>bat</td>
      <td>J Goswami</td>
      <td>India</td>
      <td>NaN</td>
      <td>7.0</td>
      <td>NaN</td>
      <td>ODI</td>
      <td>Intl</td>
      <td>Jemimah Ivan Rodrigues</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak</td>
      <td>Middle order Batter</td>
      <td>Brisbane Heat Women, Delhi Capitals Women, Ind...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Katherine Sciver-Brunt</td>
      <td>England</td>
      <td>Right hand Bat</td>
      <td>Right arm Medium fast</td>
      <td>Bowling Allrounder</td>
      <td>England Women, Trent Rockets (Women)</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>good length</td>
      <td>on off stump</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3289216</th>
      <td>1348652</td>
      <td>2022/23</td>
      <td>2023-02-09</td>
      <td>Vidarbha Cricket Association Stadium, Jamtha, ...</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>Australia</td>
      <td>RG Sharma</td>
      <td>KL Rahul</td>
      <td>PJ Cummins</td>
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
      <td>1.0</td>
      <td>4.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>Australia tour of India</td>
      <td>1.0</td>
      <td>Australia</td>
      <td>bat</td>
      <td>RA Jadeja</td>
      <td>India</td>
      <td>132.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TEST</td>
      <td>Intl</td>
      <td>Rohit Gurunath Sharma</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak</td>
      <td>Top order Batter</td>
      <td>India, Mumbai, Mumbai Indians, Air India, Decc...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Patrick James Cummins</td>
      <td>Australia</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast</td>
      <td>Bowler</td>
      <td>Australia, San Francisco Unicorns, Sunrisers H...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>full</td>
      <td>outside off</td>
      <td>leave</td>
      <td>cover</td>
    </tr>
    <tr>
      <th>4148255</th>
      <td>64100</td>
      <td>2004/05</td>
      <td>2004-10-14</td>
      <td>MA Chidambaram Stadium</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>Australia</td>
      <td>Yuvraj Singh</td>
      <td>V Sehwag</td>
      <td>GD McGrath</td>
      <td>0</td>
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
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>Australia tour of India</td>
      <td>2.0</td>
      <td>Australia</td>
      <td>bat</td>
      <td>A Kumble</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>draw</td>
      <td>TEST</td>
      <td>Intl</td>
      <td>Yuvraj Singh</td>
      <td>India</td>
      <td>Left hand Bat</td>
      <td>Slow Left arm Orthodox</td>
      <td>Middle order Batter</td>
      <td>India, Asia XI, Delhi Daredevils, India A, Kin...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Glenn Donald McGrath</td>
      <td>Australia</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast medium</td>
      <td>Bowler</td>
      <td>Australia, Delhi Daredevils, ICC World XI, Mid...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1842179</th>
      <td>1122285</td>
      <td>2017/18</td>
      <td>2018-02-18</td>
      <td>The Wanderers Stadium</td>
      <td>1</td>
      <td>0.1</td>
      <td>India</td>
      <td>South Africa</td>
      <td>RG Sharma</td>
      <td>S Dhawan</td>
      <td>D Paterson</td>
      <td>0</td>
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
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>India tour of South Africa</td>
      <td>1.0</td>
      <td>South Africa</td>
      <td>field</td>
      <td>B Kumar</td>
      <td>India</td>
      <td>28.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>T20</td>
      <td>Intl</td>
      <td>Rohit Gurunath Sharma</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak</td>
      <td>Top order Batter</td>
      <td>India, Mumbai, Mumbai Indians, Air India, Decc...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Dane Paterson</td>
      <td>South Africa</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast medium</td>
      <td>Bowler</td>
      <td>South Africa, Dolphins, Jamaica Tallawahs, Joz...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>back of length</td>
      <td>outside off</td>
      <td>dab</td>
      <td>point</td>
    </tr>
    <tr>
      <th>378783</th>
      <td>1119500</td>
      <td>2017/18</td>
      <td>2017-10-01</td>
      <td>Vidarbha Cricket Association Stadium, Jamtha</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>Australia</td>
      <td>AM Rahane</td>
      <td>RG Sharma</td>
      <td>PJ Cummins</td>
      <td>0</td>
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
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>Australia tour of India</td>
      <td>5.0</td>
      <td>Australia</td>
      <td>bat</td>
      <td>RG Sharma</td>
      <td>India</td>
      <td>NaN</td>
      <td>7.0</td>
      <td>NaN</td>
      <td>ODI</td>
      <td>Intl</td>
      <td>Ajinkya Madhukar Rahane</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Medium</td>
      <td>Top order Batter</td>
      <td>India, Chennai Super Kings, Mumbai, Delhi Capi...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Patrick James Cummins</td>
      <td>Australia</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast</td>
      <td>Bowler</td>
      <td>Australia, San Francisco Unicorns, Sunrisers H...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>short</td>
      <td>NaN</td>
      <td>defense</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1467623</th>
      <td>578623</td>
      <td>2013</td>
      <td>2013-06-15</td>
      <td>Edgbaston</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>Pakistan</td>
      <td>RG Sharma</td>
      <td>S Dhawan</td>
      <td>Mohammad Irfan</td>
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
      <td>1.0</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>ICC Champions Trophy</td>
      <td>10.0</td>
      <td>India</td>
      <td>field</td>
      <td>B Kumar</td>
      <td>India</td>
      <td>NaN</td>
      <td>8.0</td>
      <td>NaN</td>
      <td>ODI</td>
      <td>Intl</td>
      <td>Rohit Gurunath Sharma</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak</td>
      <td>Top order Batter</td>
      <td>India, Mumbai, Mumbai Indians, Air India, Decc...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Mohammad Irfan</td>
      <td>Pakistan</td>
      <td>Right hand Bat</td>
      <td>Left arm Fast</td>
      <td>Bowler</td>
      <td>Pakistan, Atlanta Riders, Balkh Legends, Baluc...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>full</td>
      <td>outside off</td>
      <td>NaN</td>
      <td>third man</td>
    </tr>
    <tr>
      <th>2639707</th>
      <td>452153</td>
      <td>2010</td>
      <td>2010-06-12</td>
      <td>Harare Sports Club</td>
      <td>2</td>
      <td>0.1</td>
      <td>India</td>
      <td>Zimbabwe</td>
      <td>M Vijay</td>
      <td>NV Ojha</td>
      <td>CB Mpofu</td>
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
      <td>1.0</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>male</td>
      <td>India in Zimbabwe T20I Series</td>
      <td>1.0</td>
      <td>India</td>
      <td>field</td>
      <td>YK Pathan</td>
      <td>India</td>
      <td>NaN</td>
      <td>6.0</td>
      <td>NaN</td>
      <td>T20</td>
      <td>Intl</td>
      <td>Murali Vijay</td>
      <td>India</td>
      <td>Right hand Bat</td>
      <td>Right arm Offbreak</td>
      <td>Opening Batter</td>
      <td>India, Chemplast, Chennai Super Kings, Delhi D...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>Christopher Bobby Mpofu</td>
      <td>Zimbabwe</td>
      <td>Right hand Bat</td>
      <td>Right arm Fast medium</td>
      <td>Bowler</td>
      <td>Zimbabwe, Amakhosi, Mashonaland, Matabeleland,...</td>
      <td>https://img1.hscicdn.com/image/upload/f_auto,t...</td>
      <td>NaN</td>
      <td>steer</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>third man</td>
    </tr>
  </tbody>
</table>
</div>

---

## A Note on Completeness:

Not all matches in the original Cricsheet dataset had commentary, and among those with commentary, not all contained detailed information such as line, length, shot played, or direction. Only about 4,000 matches had these detailed attributes, and even then, not all had all four details.

## 🧠 Tools & Techniques

- **Scraping & Automation**: `BeautifulSoup`, `Selenium`  
- **Parsing & Transformation**: `Python`, `Pandas`, `Regex`  
- **Validation**: Manual reviews and sampling

---

## ✅ Results & Quality

This project delivers one of the most detailed and high-quality cricket datasets available for public use. By combining Cricsheet’s structured ball-by-ball data with commentary-derived features from ESPNcricinfo.

---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## Contact

For any queries or contributions, feel free to reach out to:
- **Ariharasudhan A** – [Email](mailto:ariadaikalam1234@gmail.com)  
- **Harish R** – [Email](mailto:harishsekar2004@gmail.com)

---
