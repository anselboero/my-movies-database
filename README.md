# My Movies Database

A simple and intuitive tool designed to help you manage and organize your movies and tv series collection.

## What

My Movies Database (MMD) is a spreadsheet application that allows you to easily add, rate, and analyze your movies.
Through an App Script function, you can easily collect data about the movies from IMDB.
Check out my [personal database](https://docs.google.com/spreadsheets/d/1evnjLFzM3apXph0sUahqcbCwuEKCeAZh6bp3bdshSm4/edit?gid=1990214244#gid=1990214244) to see a live example of what MMD looks like.

## How
### 1. Import the Template
MMD is based on Google Sheets.
- Open the [template file](https://docs.google.com/spreadsheets/d/1-5ViP5Bn0uLv4Wy5vW8PsEq-MTmg-6PiarnHOoRYF4M/edit?usp=sharing) and from the drop-down press `File -> Make a Copy`.
- Feel Free to rename the Spreadsheet according to your preferences, but Changing sheet names is not recommended, due to possible sheet dependencies.

### 2. Get the OMDB Api Key
MMD is relying OMDB Apis to collect data about the movies. You need your personal Key, too. As of today (2025/02/02), Api calls are free, with a 1.000 daily calls limit.
- Go to the [OMDBapi.com](https://omdbapi.com/apikey.aspx) webpage, and follow the instructions.

### 3. ADD the OMDB Api Key & Enable the Script Function
The `AddMovie` sheet contains a button called `ADD MOVIE`, which is making a call to a custom Google Script function. You need to enable this function and add your OMDB Key.

Adding the Api Key:
- From the drop-down menu, go to `Extensions -> Apps Scripts`.
- From the vertical menu, press `Project Settings`.
- From Script Properties, press `Add script property`
- add the following Property: `omdbApiKey`
- Paste the Omdb key on Value.
- Press Save script properties.

Enable The Script:
- Go back to the spreadsheet, to the `AddMovie` sheet and press the `ADD MOVIE` button.
- A popup page from Google will ask you to allow the script. Follow the instructions.

### 4. Try adding your first movie
Congratulations! You have enabled MyMoviesDb! Let's try now to add your first movie.
- Go to [IMDB.Com](https://www.imdb.com/)
- Let's search for a movie. For instance, we'll be looking for [Spider-Man: Homecoming](https://www.imdb.com/title/tt2250912/?ref_=nv_sr_srsg_7_tt_8_nm_0_in_0_q_spiderma).
- From the link we can find for its Imdb ID: `https://www.imdb.com/title/tt2250912/?ref_=nv_sr_srsg_7_tt_8_nm_0_in_0_q_spiderma`. The id is `tt2250912` Copy it and paste it on the cell A2 from the `AddMovie` sheet.
- All you have to do now is pressing the `ADD MOVIE` button.
- Go to the `MoviesDB` sheet. Feel free to add your personal details from the yellow-colored columns: you can add `watching date`, a `Comment`, and your personal `rating`.
- From `Movies - Dashboards` you'll see your statistics about your watched movies.
- Have fun!
