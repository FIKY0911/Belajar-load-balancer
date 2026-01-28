# Documentation for Running the Project with Docker

## Step 1: Start Docker
Make sure Docker is running on your machine.

## Step 2: Open Terminal Root
Open your terminal (Command Prompt, PowerShell, or WSL).

## Step 3: Create a Folder
Create a new folder in the terminal root:
```bash
mkdir <folder_name>
```
Replace `<folder_name>` with your desired folder name.

## Step 4: Copy Project Files
Copy all project files into the newly created folder:
```bash
cp -r /path/to/project/* <folder_name>/
```
Replace `/path/to/project/` with the actual path to your project files.

## Step 5: Create Docker Container
Navigate to the folder you just created:
```bash
cd <folder_name>
```
Then run the following command to create the Docker container:
```bash
docker-compose up -d
```

## Step 6: Monitor the Server
To monitor the server, run:
```bash
watch -n 1 curl -s localhost:9999
```

## Step 7: Open a New Terminal in VS Code
You can either use the existing terminal or open a new terminal in VS Code, ensuring you are in the same folder created earlier.

## Step 8: View Docker Logs
Run the following command to view the logs of the server:
```bash
docker compose logs -f
```
Make sure to adjust the server name according to the upstream backends defined in your `nginx.conf`.

## Step 9: Stop a Specific Server
If you want to stop a specific server, use the following command:
```bash
docker rm -f <container_name>
```
Replace `<container_name>` with the name of the container you wish to stop.
