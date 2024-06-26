- **Class Name**: `AddFastMessageActivity`
- **Extends**: `AppCompatActivity`
- **Responsibility**: Manages the UI and functionality for adding a new fast message to the database.
- **Attributes**:
    - `db`: Instance of `Helper.MessageDbHelper` for interacting with the message database.
    - `messTitle`: EditText field for entering the message title.
    - `messContent`: EditText field for entering the message content.
- **Methods**:
    - `onCreate(Bundle savedInstanceState)`: Initializes the activity, sets the layout, and initializes UI components.
    - `addNewMessageToDB(View view)`: Called when the "Add Message" button is clicked. Validates input fields and adds a new message to the database.
    - `finishAndReturn()`: Sets the result of the activity as `RESULT_OK` and finishes the activity, indicating that the operation was successful.
- **Additional Notes**:
    - The activity layout (`R.layout.activity_add_fast_message`) contains EditText fields for entering the message title and content, as well as a button for adding the message.
    - Input filters are applied to the message content EditText to limit the number of lines and characters allowed.
    - When the "Add Message" button is clicked, the activity checks if both the title and content fields are filled. If so, it adds the message to the database using the `db.addMessage()` method from `Helper.MessageDbHelper` and finishes the activity.
    - If any field is empty, a toast message is displayed prompting the user to fill all the fields.