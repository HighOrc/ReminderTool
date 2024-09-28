# ReminderTool

**ReminderTool** is a simple desktop application built with PyQt5 that allows you to set up daily notifications. The app runs in the background after system startup, and you can access it from the system tray.

## Features

- **Daily Notifications**: Set notifications with a title, message, time, and specific days.
- **System Tray**: The app runs in the background and can be accessed from the system tray.
- **Startup on Boot**: The program starts automatically when Windows boots.
- **Add, Edit, and Delete Notifications**: Manage notifications easily through the user interface.
- **Data Persistence**: Notifications are saved to a file and loaded automatically on startup.

## Installation

### Requirements

- Python 3.6+
- PyQt5
- plyer (for notifications)
- pywin32 (for Windows startup functionality)

### Setup Instructions

1. **Clone the repository** or download the code:

    ```bash
    git clone https://github.com/HighOrc/ReminderTool.git
    cd ReminderTool
    ```

2. **Install the required Python packages**:

    Use pip to install the necessary dependencies:

    ```bash
    pip install -r requirements.txt
    ```

    If you don’t have a `requirements.txt` file, you can install dependencies individually:

    ```bash
    pip install pyqt5 plyer pywin32
    ```

3. **Run the Application**:

    To run the application, use the following command:

    ```bash
    python main.py
    ```

4. **Adding to Startup**:

    The program automatically adds itself to the Windows startup folder, so it runs when your computer starts up.

## Usage

1. **Running the Program**:

    - The program will start minimized in the system tray when launched.
    - Right-click the tray icon to open the program or exit.

2. **Adding a Notification**:

    - Enter a notification title, message, and select the time and days.
    - Click the **Add Notification** button to schedule the notification.
    - The notification will pop up at the selected time on the chosen days.

3. **Editing/Deleting Notifications**:

    - Select an existing notification from the table, then use the **Update Notification** or **Delete Notification** buttons to edit or remove it.

4. **Exiting the Application**:

    - Right-click on the system tray icon and select **Exit** to close the program.

## Customization

### Changing the Icon

Replace the `icon.png` file in the root directory with your desired icon image. Make sure the file path in `main.py` is updated accordingly:

```python
self.tray_icon.setIcon(QIcon("path/to/your/icon.png"))
```

### Customizing Notification Sounds

The application currently uses the default system sound for notifications. To customize, modify the `notification.notify()` call in `notification_manager.py` and use a custom sound file.

## Known Issues

- **No Icon Displayed**: If the tray icon doesn't appear, make sure you have an appropriate `.png` file for the icon and it's in the correct path.
- **Application Not Running on Startup**: Ensure that the `pywin32` library is installed and functioning correctly. If startup is not working, manually check if the shortcut is placed in the startup folder (`shell:startup`).

## Contributing

1. Fork the repository.
2. Create a new branch for your feature:

    ```bash
    git checkout -b feature-name
    ```

3. Commit your changes:

    ```bash
    git commit -m 'Add some feature'
    ```

4. Push to the branch:

    ```bash
    git push origin feature-name
    ```

5. Open a pull request.

## License

This project is licensed under the MIT License.

---
