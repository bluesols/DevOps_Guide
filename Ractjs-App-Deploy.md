Test your app on localhost if working then build for production
$npm run build
Npm Run Build command will generate build folder for production
Copy build folder accross
/var/www/example.com/html/
scp -r ./build/* user@server_ip_address:/var/www/example.com/html
make sure you place user with your server username and ip address with your server ip address
open your browser and check your app will be live
Now you have created live website and you want to make changes in that app in local VSCode or any toher editor and deploy those changes
A sample script npm script in your package.json file can acheive this
Open you package.json file in editor.
In the scripts section of the JSON add this line below
"deploy-production": "react-scripts build && scp -r ./build/* user@server_ip_address:/var/www/example.com/html"
