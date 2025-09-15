NBA Box Score Processor
A Python script for processing NBA basketball game box scores from HTML files, extracting statistical data, and compiling it into a comprehensive dataset for analysis.

Features
HTML Parsing: Extracts game data from box score HTML files

Statistical Processing: Processes both basic and advanced player statistics

Team Comparison: Creates head-to-head comparisons for each game

Error Handling: Robust error handling for incomplete or malformed files

Batch Processing: Efficiently processes large datasets (12,000+ files)

Requirements
Python 3.7+

pandas

BeautifulSoup4

lxml

Installation
bash
pip install pandas beautifulsoup4 lxml
Usage
Basic Usage
python
from your_script import process_box_scores

# Process a directory of box score files
box_scores = ["path/to/box_score_files/*.html"]
games_data = process_box_scores(box_scores)
Main Functions
read_stats(soup, team, stat)
Extracts statistical data from HTML tables.

Parameters:

soup: BeautifulSoup object of the HTML content

team: Team abbreviation (e.g., "LAL", "BOS")

stat: Type of statistics ("basic" or "advanced")

Returns: pandas DataFrame with processed statistics

Main Processing Loop
Processes multiple box score files with comprehensive error handling:

Skips empty files

Handles missing statistical tables

Validates team data completeness

Continues processing despite individual file errors

Data Structure
Output Columns
The processed data includes:

Team Statistics:

Basic stats: points, rebounds, assists, steals, blocks, etc.

Advanced stats: efficiency metrics, shooting percentages

Maximum player stats for each category

Game Context:

Home/Away designation

Opponent statistics (suffixed with _opp)

Season information

Game date

Win/loss indicator

Example Output
python
# Each game produces a DataFrame with:
# - Team 1 stats (basic + advanced + max values)
# - Team 2 stats (with _opp suffix)
# - Game metadata (date, season, result)
Error Handling
The script includes comprehensive error handling for:

Empty HTML files

Missing statistical tables

Incomplete team data

Parsing errors

File reading issues

Files with errors are skipped and logged, allowing batch processing to continue.

Performance
Processes ~100 files per progress update

Handles large datasets efficiently

Memory-optimized with incremental processing

Use Cases
Sports analytics research

Team performance tracking

Player statistics analysis

Game prediction models

Historical data compilation

Notes
Ensure HTML files follow expected NBA box score format

Files should be named with date format YYYYMMDD for proper date parsing

The script assumes standard NBA statistical categories

this thing doesnt work yet and im still trying but im going to shoot myself if i dont get it to work soon
For issues with specific file formats or parsing errors, check the console output for detailed error messages indicating which files were skipped and why.

