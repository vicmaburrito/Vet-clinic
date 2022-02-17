![](https://img.shields.io/badge/Microverse-blueviolet)

# Database Speed Optimization

- This is a database project built for learning purposes.
- In this project, we created a database, set up columns and join tables.
- We populated the list with random informations.
- We improved the queries speed by creating indexes.

## Built With

- PostgreSQL

## Requirements

- You will need [postgreSQL](https://www.postgresql.org/download/) or other SQL management tool installed in your computer.

## Getting Started

1 - On Github, visit the main page of this repository, click the Code button and copy "Clone with HTTPS" by clicking on the copy icon.

* To get a local copy updated and running follow these steps.

2 - open your terminal and clone the project running:

`git clone https://github.com/vicmaburrito/Vet-clinic.git`

3 - start your postgreSQL server on the terminal by running:

`psql`

4 - create a new database by running:

`CREATE DATABASE vetclinic;`

4 - connect to the database:

`\c vetclinic`

5 - run the schema.sql file by running:

`\i [PATH TO THE FILE WHERE YOU CLONED THE REPO]`

6 - run the data.sql file by running:

`\i [PATH TO THE FILE WHERE YOU CLONED THE REPO]`

6 - populate database by running:

`INSERT INTO visits (animal_id, vet_id, date_of_visit) SELECT * FROM (SELECT id FROM animals) animal_ids, (SELECT id FROM vets) vets_ids, generate_series('1980-01-01'::timestamp, '2021-01-01', '4 hours') visit_timestamp;`

and 

`insert into owners (full_name, email) select 'Owner ' || generate_series(1,2500000), 'owner_' || generate_series(1,2500000) || '@mail.com';`

Now you are ready to run the queries!

Check if it is working by using one of the following queries:

`SELECT COUNT(*) FROM visits where animal_id = 4;`
`SELECT * FROM visits where vet_id = 2;`
`SELECT * FROM owners where email = 'owner_18327@mail.com';`

## Author

👤 **Jonathas Tavares**

- GitHub: [jonathastavares](https://github.com/jonathastavares)
- LinkedIn: [Jonathas Tavares](https://www.linkedin.com/in/jonathas-tavares-24b8bba3/)

👤 **Manuel Aldaraca**
GitHub: [@vicmaburrito](https://github.com/vicmaburrito)
LinkedIn: [Manuel Aldaraca](https://www.linkedin.com/in/manuelaldaraca)
Twitter: [@manuelaldaraca](https://twitter.com/manuelaldaraca)

👤 **Abel Lavieri**
GitHub: [@alvp01](https://github.com/alvp01)
LinkedIn: [Abel Lavieri](https://www.linkedin.com/in/abel-lavieri/)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

## Show your support

Give a ⭐️ if you like this project!

## 📝 License

This project is [MIT](./MIT.md) licensed.