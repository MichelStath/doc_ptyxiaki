- **Package**: `com.example.activities.ptyxiakilauncher.classes`
- **Class Name**: `CustomAdapter`
- **Responsibility**: Manages the RecyclerView adapter for displaying contacts. It also handles user interactions like deleting contacts.
- **Constructor**:
    - `public CustomAdapter(Context context, ArrayList<Models.Contact> contacts, ContactClickListener listener)`: Initializes the CustomAdapter with the context, list of contacts, and a listener for contact click events.
    - `context`: The context of the calling activity.
    - `contacts`: The list of contacts to display.
    - `listener`: A listener for contact click events.
- **Methods**:
    - `onCreateViewHolder(ViewGroup parent, int viewType)`: Inflates the layout for each contact row.
    - `onBindViewHolder(MyViewHolder holder, int position)`: Binds contact data to the views within each row and sets click listeners.
    - `getItemCount()`: Returns the total number of contacts.
- **Inner Class**:
    - `MyViewHolder`: Represents a single contact row view holder.
        - `contact_id_txt`: TextView for displaying contact ID.
        - `contact_name_txt`: TextView for displaying contact name.
        - `contact_phone_txt`: TextView for displaying contact phone number.
        - `mainLayout`: LinearLayout serving as the root layout for the contact row.
- **Dependencies**:
    - `android.widget.TextView`
    - `android.widget.LinearLayout`
    - `android.widget.Toast`
    - `android.app.AlertDialog`
    - `android.content.Context`
    - `android.content.DialogInterface`
    - `android.view.LayoutInflater`
    - `android.view.View`
    - `android.view.ViewGroup`
    - `androidx.recyclerview.widget.RecyclerView`
    - `com.example.activities.ptyxiakilauncher.FastContactsActivity`
    - `com.example.activities.ptyxiakilauncher.R`
    - `java.util.ArrayList`
    - `java.util.List`
    - `java.util.PrimitiveIterator`
- **Resource Usage**:
    - `R.layout.contact_row`
    - `R.id.contact_id_txt`
    - `R.id.contact_name_txt`
    - `R.id.contact_phone_txt`
    - `R.id.mainLayout`
- **Listener Interface**:
    - `ContactClickListener`: Interface for handling contact delete events.
        - `onDeleteContact(Models.Contact contact)`: Method invoked when a contact is deleted.
- **Additional Notes**:
    - Utilizes a `Helper.ContactDbHelper` for database operations related to contacts.
    - Implements an `AlertDialog` for handling user interactions such as contact deletion.

