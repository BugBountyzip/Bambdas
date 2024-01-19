### Script Overview:
1. **Endpoint Guessing Logic**: The script uses the OpenAI API to guess potential endpoints based on the path of an HTTP request.
2. **Operating System Compatibility**: It is designed to work on both Windows and Unix-like operating systems (Linux/macOS) by adapting file paths and command execution methods according to the OS.
3. **Curl Command**: The script constructs a curl command to send a request to the OpenAI API, including details about the HTTP request path for endpoint guessing.

### Instructions for Users:
1. **Add Your OpenAI API Key**:
   - Locate the line containing the curl command.
   - Replace `XYZ` in `Authorization: Bearer XYZ` with your actual OpenAI API key.
   - Example: `"-H \"Authorization: Bearer sk-yourapikeyhere\""`

2. **Adjust the File Paths**:
   - The script writes output to specific file paths, which you may need to adjust based on your system.
   - For Windows: Change the paths in these lines:
     ```java
     filePath = "C:\\Users\\User\\Path\\httpRequest.txt";
     endpointsPath = "C:\\Users\\User\\Path\\endpoints.txt";
     ```
   - For Unix/Linux/macOS: Change the paths in these lines:
     ```java
     filePath = "/home/kali/Desktop/httpRequest.txt";
     endpointsPath = "/home/kali/Desktop/endpoints.txt";
     ```
   - Ensure the directories exist or create them as needed.

3. **Ensure Compatibility**:
   - The script detects the operating system and adjusts command execution accordingly. No changes are needed here unless you encounter issues specific to your environment.
