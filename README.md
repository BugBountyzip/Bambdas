## ChatGPT_API_Predictor.bambda

### Script Overview:
1. **Endpoint Guessing Logic**: The script uses the OpenAI API to guess potential endpoints based on the path of an HTTP request.
2. **Selecting a Request for Analysis**: It identifies the request to analyze based on a specific annotation ("aaa") added to a request in Burp Suite's history.
3. **Operating System Compatibility**: Designed to work on both Windows and Unix-like operating systems (Linux/macOS) by adapting file paths and command execution methods according to the OS.
4. **Curl Command**: Constructs a curl command to send a request to the OpenAI API, including details about the HTTP request path for endpoint guessing.

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

3. **Marking and Changing Requests for Analysis**:
   - In Burp Suite's history, add a note containing "aaa" to any request you wish to analyze with this script.
   - To analyze a different request, first remove or change the "aaa" note from the currently marked request, then add "aaa" to the new request you want to analyze.
   - This method allows you to selectively process requests from Burp Suite's history.

4. **Ensure Compatibility**:
   - The script detects the operating system and adjusts command execution accordingly. No changes are needed here unless you encounter issues specific to your environment.
  
     _____________________
     
## JS Route Inspector :


### Script Overview:
1. **JavaScript Route Exploration**: This script is designed to discover and analyze JavaScript routes and endpoints. It scans JavaScript files to detect hidden or non-standard endpoints, aiding in thorough exploration of web assets.
2. **Duplicate Removal and Customization**: The script includes features for duplicate removal, customizable scan types ('Balanced', 'Deep', 'Custom'), and highlighting of key terms within JavaScript files.
3. **User-Defined Patterns and Annotations**: Users can define their own regex patterns for more targeted scanning and annotate results with custom words for enhanced visibility.
4. **Endpoint File Handling**: It writes discovered endpoints to a file and ensures uniqueness by removing duplicates and empty lines.

### Instructions for Users:

1. **Adjust the File Paths**:
   - The script writes output to specific file paths, which you may need to adjust based on your system.
   
   For Windows:
   ```java
   String dataFilePath = "C:\\Users\\YourUsername\\Desktop\\File.txt";
   ```
   
   For Unix/Linux/macOS:
   ```java
   String dataFilePath = "/home/yourusername/Desktop/File.txt";
   ```
   - Ensure the directories specified in the paths exist or create them as needed.

2. **Customize Your Scan**:
   - Set the `scanType` variable to your desired scan type: 'High', 'Deep', or 'Custom'.
   - If using 'Custom', define your custom regex pattern in the `customRegex` variable.

3. **Enable or Disable Highlighting**:
   - The `manualColorHighlightEnabled` variable is set to `true` by default to enable manual color highlighting of high-value words. Change this to `false` to disable highlighting.

4. **Add High-Value Words**:
   - Add any high-value words you want to check for within the `highValueWords` array.
   - Example:
   ```java
   String[] highValueWords = {"debug", "admin", "test", "config", "secret", "token"};
   ```

### Example Adjustments for Different Operating Systems

**For Windows**:
```java
String dataFilePath = "C:\\Users\\YourUsername\\Desktop\\File.txt";
```

**For Unix/Linux/macOS**:
```java
String dataFilePath = "/home/yourusername/Desktop/File.txt";
```

### Running the Script:
1. Set up your Burp Suite to capture the necessary traffic.
2. Customize the script parameters as per your needs (file paths, scan type, regex patterns, high-value words).
3. Run the script to analyze JavaScript routes and endpoints.
4. Check the output file (`File.txt`) in the specified path for the results.

