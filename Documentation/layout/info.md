1. **ConstraintLayout**: This is the root layout that allows for flexible positioning of its children.
    
2. **LinearLayout**:
    
    - Orientation: Vertical
    - Padding: 10dp
    - Constrained to match the parent's dimensions.
3. **TextView** (`@+id/textView`):
    
    - Displays the title of the activity.
    - Positioned at the top with Aqua color text and bold style.
    - Constrained horizontally with a Button (`@+id/button2`) for editing.
4. **Button** (`@+id/button2`):
    
    - Allows the user to edit the information.
    - Positioned to the right of the title TextView.
    - Calls the `editBTN` method when clicked.
5. **TextViews**:
    
    - Display user information such as name, surname, phone number, AFM, AMKA, and ID number.
    - Each TextView has a label followed by the corresponding user information.
    - Text color is white with a bold style.

**Constraints**:

- The LinearLayout is constrained to match the parent's dimensions, ensuring it fills the entire screen.
- The internal views are positioned vertically, stacked one below the other, maintaining a consistent layout.

**Attributes**:

- Various attributes such as `layout_width`, `layout_height`, `text`, `textColor`, `textSize`, etc., are specified to define the appearance and content of the TextViews and Button.

Overall, this layout provides a simple and clear interface for displaying user information and allowing the user to edit it easily.