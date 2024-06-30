# Project Details:
<ul>
  <li>Angular frontend with Bootstrap and TS</li>
  <li>Spring boot backend with Spring Data JPA and Hibernate</li>
  <li>A relational DB using MySQL</li>
</ul>
<br>

# Here's a demo of the UI:

![Screenshot 2024-07-01 021949](https://github.com/rengoku33/witcher-alchemy/assets/89008619/ccdc2cb7-a488-425f-8873-bf828a7841cc)

![Screenshot 2024-07-01 022038](https://github.com/rengoku33/witcher-alchemy/assets/89008619/27c1690f-38f4-4251-a6f9-27b20a7ec128)

<br>

# Must Read:
Alright, lets address the elephant in the room,
<h3>why isn't this project live?</h3>
Hey! calm down and hear me out,<br>This project is divided into 3 parts (frontend, backend, DB) and containerized using Docker. My primary choice was AWS and secondary was a mix of cloud providers, but it turns out they are not free

## Case 1: AWS
<ul>
  <li>Frontend: S3 ($$$ if more than 3000 GET or 2000 PUT requests per months/ also free for 12 months only)</li>
  <li>Backend: AWS lambda (Actually free with limited usage)</li>
  <li>Server for DB: RDS ($$$ if server runs for more than 750hrs or exceeds 20GB storage/ also free for 12 months only)</li>
</ul>
Now, when the limit gets crosseed AWS does not halt the service, instead they prefer extortion<br>
Which translates to: you get DDoSed in S3 or RDS = you are screwed

## Case 2: Hybrid of cloud providers
<ul>
  <li>Frontend: Vercel or Netlify (Free with limited usage)</li>
  <li>Backend: AWS lambda (Free with limited usage)</li>
  <li>Remote DB: Firebase or AWS dynamoDB (Free with limited usage)</li>
</ul>
Now, you might wonder: well, why not proceed with this?<br>
3 different providers for 1 app is not a good practice and a nightmare to integrate and maintain<br>
Even if I proceed with this, both the remote DB mentioned are NoSQL, which means I have to compromise my relational DB 

## Case 3: Turn my PC into a server
Nawww, this aint even an option with my PC

