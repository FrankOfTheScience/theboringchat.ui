## TheBoringChat - UI

#### Description:

This is the Frontend for TheBoringChat, a really boring group (or 1:1) chat.

#### Context:

This project was made as a demo, to experiment with `.NET SignalR` library, since I am a Backend Dev the UI has been totally improvised using `React`, so I messed up here and forth specially with `CSS` trying to find workarounds for darkMode for example 😅.

#### State of the project:

This Frontend Project is done, maybe I am going to change some color here and there but major improvements won't be released on this repo until I find new ways to experiment with backend, which is my main focus.

_I would like to publish this project, but for free. Since frontend is a static page I might use GitPages, but for backend I was trying to find free host providers straight forward to use, I don't want to invest too much time on just publish this app, since it is a simple personal project sincerely. Open to suggestion for this!_

#### Backend

You can find the Backend repo [HERE](https://github.com/FrankOfTheScience/TheBoringChat)

## Project Screen Shot(s)

#### Waiting Room:   
**Light Theme:**
![waiting-room-light](https://github.com/FrankOfTheScience/theboringchat.ui/assets/119010269/cd308c13-47a2-46da-86dd-d32c1bf03976)

**Dark Theme:**
![waiting-room-dark](https://github.com/FrankOfTheScience/theboringchat.ui/assets/119010269/72abc670-295b-4d89-a02c-42a9d45ca6fc)

#### Chat Room:   
**Light Theme:**
![chat-room-light](https://github.com/FrankOfTheScience/theboringchat.ui/assets/119010269/50ebf363-3c67-4c39-8be1-323d987056dd)

**Dark Theme:**
![chat-room-dark](https://github.com/FrankOfTheScience/theboringchat.ui/assets/119010269/bb5e822a-a093-4326-9f3a-1c2e78e0bd51)

#### Three Clients Chat Room:   
**Mixed Themes:**
![commo-chat-mixed-themes](https://github.com/FrankOfTheScience/theboringchat.ui/assets/119010269/9b401c7c-26fc-42de-8716-9385ba3a0595)


## Installation and Setup Instructions

### Prerequisites
- [Node.js](https://nodejs.org/) installed on your machine.
- [Git](https://git-scm.com/) installed on your machine.
- [ASP.NET Core SDK](https://dotnet.microsoft.com/download) installed on your machine.
- Powershell or a terminal compatible with bash commands.

### Steps:

1. **Download the frontend repository:**
   - Navigate through Powershell to your destination directory.
   - Run:
   ```powershell
   git clone https://github.com/FrankOfTheScience/theboringchat.ui.git
   ```

2. **Download the backend repository:**
   - Run:
   ```powershell
   git clone https://github.com/FrankOfTheScience/TheBoringChat.git
   ```

3. **Launch the backend project (ASP.NET Core WebApi) locally via Powershell:**
   - Navigate to the backend repository just extracted.
   - Run:
   ```powershell
   dotnet run
   ```

4. **Take note of the localhost:**
   - While running the backend server, take note of the localhost address on which the server is listening. It is usually `http://localhost:5000`.

5. **Configure the frontend to connect to the local backend:**
   - Through Powershell navigate into the directory of the extracted frontend repository.
   - Run:
     ```powershell
     $backendUrl = "<your_backend_localhost>"
     If (-not (Test-Path -Path ".env")) {
         New-Item -ItemType File -Path ".env"
     }
     Set-Content -Path ".env" -Value "REACT_APP_BACKEND_BASE_URL=$backendUrl"

6. **Install npm dependencies:**
   - Run:
     ```powershell
     npm install
     ```

7. **Start the frontend development server:**
   - Run:
     ```powershell
     npm start
     ```

## Functional Instructions

0. **Follow the previous installation and setup instructions**
   
1. **Visit the frontend on localhost:**
   - Open your preferred web browser and go to the address `http://localhost:3000`. Here you will be able to see the frontend app in action.
  
2. **Fill the form:**
   - Nickname is mandatory, Chatroom is optional
   - If Chatroom isn't provided you will be joint to the general chat
   - Provide the same Chatroom name to join a private chat with clients who provided the same Chatroom name

3. **Optional step: Test the chat with multiple clients:**
   - Open another browser or an incognito browsing window.
   - Visit `http://localhost:3000` to create another instance of the frontend and try chatting between the two clients

### Enjoy Boredom!!!


