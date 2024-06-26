- **Package**: `com.example.activities.ptyxiakilauncher.classes`
- **Class Name**: `DateTimeThread`
- **Responsibility**: Manages a background thread to continuously update date and time on a pair of TextViews. It also checks for GPS status and interacts with the LocationHelper class to handle GPS settings.
- **Constructor**:
    - `public DateTimeThread(Handler handler, TextView tv1, TextView tv2)`: Initializes the DateTimeThread with a handler, and two TextViews for displaying date and time.
        - `handler`: Handler to post update tasks.
        - `tv1`: First TextView to display date.
        - `tv2`: Second TextView to display time.
- **Methods**:
    - `start()`: Starts the thread.
    - `run()`: Runs the thread and continuously updates date and time.
    - `isThreadRunning()`: Getter for `threadIsRunning`.
    - `setThreadRunning(boolean threadIsRunning)`: Setter for `threadIsRunning`.
    - `stopThread()`: Stops the thread.
- **Dependencies**:
    - `android.os.Handler`
    - `android.os.PowerManager`
    - `android.widget.TextView`
    - `android.app.Activity`
    - `android.content.Context`
    - `java.text.SimpleDateFormat`
    - `java.util.Date`
    - `java.util.Locale`
    - `com.example.activities.ptyxiakilauncher.classes.LocationHelper`
- **Resource Usage**:
    - No specific resources used.
- **Additional Notes**:
    - Utilizes `LocationHelper` to check GPS status and show GPS settings if GPS is not enabled.
    - Continuously updates date and time on the provided TextViews using a background thread.
    - Checks if the screen is interactive using `PowerManager` and stops updates if it's not.