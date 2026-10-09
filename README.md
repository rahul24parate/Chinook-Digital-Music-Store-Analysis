# Business Optimisation Analysis of Chinook Digital Music Store

## 📌 Project Overview

This project focuses on analysing the Chinook Digital Music Store database using SQL to identify business opportunities, improve sales performance, and support data-driven decision-making.

Chinook is a fictional digital music store that sells music tracks across different genres, artists, and countries. By analysing its sales, customers, employees, and music catalogue, this project aims to identify actionable insights that can help optimise business performance.

## 🎯 Project Objectives

* Identify the most profitable music genres.
* Evaluate the performance of sales support agents.
* Recommend marketing strategies for countries with lower sales.
* Identify the best city to organise a music festival.
* Evaluate purchasing strategies to reduce costs.
* Identify top-performing artists to develop sales-boosting strategies.
* Recommend concert types and artists to maximise audience participation.
* Develop a customer reward strategy for top spenders in each country.

## 📊 Importance of Business Optimisation

Business optimisation is the process of improving an organisation's efficiency, productivity, and overall performance. It involves continuously identifying opportunities for improvement and implementing strategies to achieve better business outcomes.

Key elements of business optimisation include:

* Measuring productivity, efficiency, and performance.
* Identifying areas that require improvement.
* Introducing new methods, processes, and systems.
* Measuring and comparing results.
* Continuously monitoring and improving business performance.

Examples of business optimisation include:

* Reducing turnaround time through improved processes.
* Lowering operational costs while maintaining performance.
* Automating repetitive tasks.
* Increasing sales by improving customer satisfaction.
* Using data analysis to make informed business decisions.

## 🗄️ Dataset and Data Source

The Chinook database represents a digital media store and contains information about artists, albums, tracks, customers, employees, invoices, and playlists.

The dataset includes:

* **Music Catalogue Data:** Artists, albums, tracks, genres, and media types.
* **Customer Data:** Customer details, locations, and assigned sales representatives.
* **Sales Data:** Invoices, invoice line items, quantities, and prices.
* **Employee Data:** Employee details and reporting relationships.
* **Playlist Data:** Playlists and their associated tracks.

The music-related data was created using real data from an iTunes library. Customer and employee information was generated using fictional details, while sales information was randomly generated for a four-year period.

## 🧰 Tools and Technologies

* **SQL:** Querying, joining, and analysing relational data.
* **Relational Database:** Understanding database tables, relationships, and schema design.
* **GitHub:** Project documentation and version control.

## 🧩 Database Schema

The Chinook database contains 11 tables representing relationships between customers, music, employees, and sales transactions.

**Schema Diagram:** [View Database Schema]()

### Database Tables

| Table           | Description                                                                                  |
| --------------- | -------------------------------------------------------------------------------------------- |
| `Album`         | Stores album details and associated artist IDs.                                              |
| `Artist`        | Contains artist IDs and names.                                                               |
| `Customer`      | Stores customer information, contact details, locations, and assigned sales representatives. |
| `Employee`      | Contains employee information and reporting relationships.                                   |
| `Genre`         | Stores music genre IDs and names.                                                            |
| `Invoice`       | Contains invoice dates, customer IDs, billing information, and total amounts.                |
| `InvoiceLine`   | Stores individual invoice items, track IDs, quantities, and unit prices.                     |
| `MediaType`     | Contains media type IDs and names.                                                           |
| `Playlist`      | Stores playlist IDs and names.                                                               |
| `PlaylistTrack` | Connects playlists with their associated tracks.                                             |
| `Track`         | Contains track details, album and genre IDs, composers, durations, file sizes, and prices.   |

### Table Structures

<details>
<summary><strong>1. Album</strong></summary>

| Column     | Description                                 |
| ---------- | ------------------------------------------- |
| `AlbumId`  | Unique identifier for each album.           |
| `Title`    | Name of the album.                          |
| `ArtistId` | ID of the artist associated with the album. |

</details>

<details>
<summary><strong>2. Artist</strong></summary>

| Column     | Description                        |
| ---------- | ---------------------------------- |
| `ArtistId` | Unique identifier for each artist. |
| `Name`     | Name of the artist.                |

</details>

<details>
<summary><strong>3. Customer</strong></summary>

| Column         | Description                              |
| -------------- | ---------------------------------------- |
| `CustomerId`   | Unique identifier for each customer.     |
| `FirstName`    | Customer's first name.                   |
| `LastName`     | Customer's last name.                    |
| `Company`      | Customer's company, if available.        |
| `Address`      | Customer's address.                      |
| `City`         | Customer's city.                         |
| `State`        | Customer's state.                        |
| `Country`      | Customer's country.                      |
| `PostalCode`   | Customer's postal code.                  |
| `Phone`        | Customer's phone number.                 |
| `Fax`          | Customer's fax number, if available.     |
| `Email`        | Customer's email address.                |
| `SupportRepId` | ID of the assigned sales representative. |

</details>

<details>
<summary><strong>4. Employee</strong></summary>

| Column       | Description                                  |
| ------------ | -------------------------------------------- |
| `EmployeeId` | Unique identifier for each employee.         |
| `FirstName`  | Employee's first name.                       |
| `LastName`   | Employee's last name.                        |
| `Title`      | Employee's job title.                        |
| `ReportsTo`  | ID of the employee's manager, if applicable. |
| `BirthDate`  | Employee's date of birth.                    |
| `Address`    | Employee's address.                          |
| `City`       | Employee's city.                             |
| `State`      | Employee's state.                            |
| `Country`    | Employee's country.                          |
| `PostalCode` | Employee's postal code.                      |
| `Phone`      | Employee's phone number.                     |
| `Fax`        | Employee's fax number, if available.         |
| `Email`      | Employee's email address.                    |

</details>

<details>
<summary><strong>5. Genre</strong></summary>

| Column    | Description                       |
| --------- | --------------------------------- |
| `GenreId` | Unique identifier for each genre. |
| `Name`    | Name of the music genre.          |

</details>

<details>
<summary><strong>6. Invoice</strong></summary>

| Column              | Description                               |
| ------------------- | ----------------------------------------- |
| `InvoiceId`         | Unique identifier for each invoice.       |
| `CustomerId`        | ID of the customer who made the purchase. |
| `InvoiceDate`       | Date of the purchase.                     |
| `BillingAddress`    | Billing address.                          |
| `BillingCity`       | Billing city.                             |
| `BillingState`      | Billing state.                            |
| `BillingCountry`    | Billing country.                          |
| `BillingPostalCode` | Billing postal code.                      |
| `Total`             | Total amount of the invoice.              |

</details>

<details>
<summary><strong>7. InvoiceLine</strong></summary>

| Column          | Description                              |
| --------------- | ---------------------------------------- |
| `InvoiceLineId` | Unique identifier for each invoice line. |
| `InvoiceId`     | ID of the associated invoice.            |
| `TrackId`       | ID of the purchased track.               |
| `UnitPrice`     | Price per track.                         |
| `Quantity`      | Quantity purchased.                      |

</details>

<details>
<summary><strong>8. MediaType</strong></summary>

| Column        | Description                            |
| ------------- | -------------------------------------- |
| `MediaTypeId` | Unique identifier for each media type. |
| `Name`        | Name of the media type.                |

</details>

<details>
<summary><strong>9. Playlist</strong></summary>

| Column       | Description                          |
| ------------ | ------------------------------------ |
| `PlaylistId` | Unique identifier for each playlist. |
| `Name`       | Name of the playlist.                |

</details>

<details>
<summary><strong>10. PlaylistTrack</strong></summary>

| Column       | Description                               |
| ------------ | ----------------------------------------- |
| `PlaylistId` | ID of the associated playlist.            |
| `TrackId`    | ID of the track included in the playlist. |

</details>

<details>
<summary><strong>11. Track</strong></summary>

| Column         | Description                                 |
| -------------- | ------------------------------------------- |
| `TrackId`      | Unique identifier for each track.           |
| `Name`         | Name of the track.                          |
| `AlbumId`      | ID of the album containing the track.       |
| `MediaTypeId`  | ID of the track's media type.               |
| `GenreId`      | ID of the track's genre.                    |
| `Composer`     | Name of the track's composer, if available. |
| `Milliseconds` | Duration of the track in milliseconds.      |
| `Bytes`        | File size of the track in bytes.            |
| `UnitPrice`    | Price of the track.                         |

</details>

## 🔍 Business Questions

This project explores the following business questions through SQL analysis:

1. Which music genres generate the highest sales?
2. How do sales support agents perform in terms of revenue?
3. Which countries could benefit from targeted marketing campaigns?
4. Which city is the best candidate for hosting a music festival?
5. How can purchasing strategies be optimised to reduce costs?
6. Which artists generate the most sales?
7. Which artists and music genres could attract the largest concert audience?
8. Who are the highest-spending customers in each country?

## 💡 Expected Business Value

The analysis aims to help the business:

* Identify revenue-generating genres and artists.
* Understand customer purchasing behaviour.
* Evaluate sales performance.
* Discover potential growth opportunities in different markets.
* Make informed decisions about marketing and event planning.
* Improve customer retention through targeted rewards.
* Support cost optimisation and revenue growth.

*Note: Specific findings and recommendations should be added after running the SQL queries and validating the results.*

## 📁 Project Structure

```text
Chinook-Business-Optimisation/
│
├── README.md
├── schema_diagram.png
├── dataset/
│   └── chinook_database
│
└── sql_queries/
    ├── genre_sales.sql
    ├── sales_agent_performance.sql
    ├── country_marketing.sql
    ├── best_festival_city.sql
    ├── purchasing_strategy.sql
    ├── top_artists.sql
    ├── concert_recommendations.sql
    └── customer_rewards.sql
```

*Update the folder and file names to match your actual repository.*

## 🚀 Conclusion

The Chinook Digital Music Store analysis demonstrates how SQL and relational database analysis can be used to investigate business performance and identify opportunities for optimisation.

By examining sales transactions, customer behaviour, music preferences, and employee performance, this project aims to develop practical recommendations that support data-driven business decisions.

## 📚 References

* [Chinook Database Repository](https://github.com/lerocha/chinook-database)
* [Luis Rocha's GitHub Profile](https://github.com/lerocha)
* [Original Schema Diagram](https://github.com/Rafsan7238/Data-Analysis_Data-Science_Projects/raw/main/SQL%20Projects/Chinook%20Digital%20Music%20Store%20Analysis/schema_diagram.png)
