# CP3407 Project - Tools & External Libraries Utilised

## Tools
For this project, the team came to a consensus that FeedMe should be developed using WordPress due to its extensive plugin library and the familarity with the platform for the majority of the group. From there, plugins like WooCommerce would streamline the development process, providing tools such as a payment gateway and eCommerce shop functionality, allowing us to transform a simple website into a prominent FoodPanda rival.

Whilst WordPress would be utilised to develop the website, the team had to also decide what software and hardware provider would be best to host the content management system. After discussing options including Microsoft Azure and DigitalOcean, it was determined that Amazon Web Services would be the hosting provider with their EC2 lineup being selected to act as the website server. This was mainly due to the fact that it was cost-effective (free tier) whilst still providing more than sufficient hardware and software required to get the project up and running.

To manage the MariaDB instance that was to be created for the WordPress installation to store data, PHPMyAdmin was also installed onto the AWS EC2 instance due to its simplicity as a result of an easy-to-use user interface and the ability to easily access the software through the server's IP/domain name.

## External Libraries

To transform WordPress from a website builder to an eCommerce food delivery website, external libraries through the use of plugins were utilised. These included the following:

* Astra - theme preset and customisation tools
* Elementor - WYSIWYG website builder tools
* WooCommerce - eCommerce platform tools
