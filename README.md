# tsutsujibus-countdown

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A real-time departure countdown web application for the Tsutsuji Bus community bus service in Sabae, Fukui.

The app features a pink-themed interface with dropdown menus to select an origin and destination. It displays a list of the next five departure times with a live countdown to the next bus.

## Demo

**https://code4fukui.github.io/tsutsujibus-countdown/**

## Features

- **Real-time Countdown**: Shows the minutes and seconds until the next departure, updating automatically.
- **Upcoming Departures**: Displays a list of the next 5 scheduled bus times for the selected route.
- **Custom Time Search**: Use the time input field to check for departures at any time of day.
- **Route Swapping**: Instantly swap the origin and destination with a single click.
- **Shareable Links**: The URL updates automatically to reflect your selected route, making it easy to share.

## How to Run Locally

1.  **Prerequisites**: [Deno](https://deno.land/) must be installed.
2.  **Download GTFS Data**: Fetch the latest bus schedule data by running the following command in your terminal:
    ```bash
    deno run --allow-net --allow-write download.js
    ```
    This will download the required `gtfs_sabae.zip` file into the project directory.
3.  **Launch the App**: Open the `index.html` file in your web browser.

## Data, Libraries, and Attribution

-   **Data Source**: [鯖江市コミュニティバスつつじバス (Sabae City Community Bus "Tsutsuji Bus")](https://www.pref.fukui.lg.jp/doc/dx-suishin/opendata/gtfs_jp_d/fil/gtfs_sabae.zip) from the [Fukui Prefecture Open Data portal](https://www.pref.fukui.lg.jp/doc/dx-suishin/opendata/gtfs_jp.html).
-   **Core Library**: [GTFS.js](https://github.com/code4fukui/GTFS) is used for parsing and querying the GTFS schedule data.
-   **Forked from**: This project is a fork of [発車カウントダウン - ハピラインふくい (Departure Countdown - Hapi-Line Fukui)](https://code4fukui.github.io/hapiline-timetable/).

## License

MIT License by Code for FUKUI