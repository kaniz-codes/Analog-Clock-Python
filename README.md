# Analog-Clock-Python
The clock face more visually appealing, allow dynamic resizing, and add tick marks for minutes and seconds.

1️⃣ 𝐈𝐦𝐩𝐨𝐫𝐭𝐢𝐧𝐠 𝐌𝐨𝐝𝐮𝐥𝐞𝐬:

![codeimage-snippet_7](https://github.com/kaniz-codes/Analog-Clock-Python/assets/138873297/e8f6a31d-b7cf-44cc-b4b9-97ed1e2d9400)

- The code imports the 𝒕𝒌𝒊𝒏𝒕𝒆𝒓 module for creating GUI applications and the 𝒕𝒊𝒎𝒆 module for handling time-related operations.

2️⃣ 𝐂𝐫𝐞𝐚𝐭𝐢𝐧𝐠 𝐭𝐡𝐞 𝐌𝐚𝐢𝐧 𝐖𝐢𝐧𝐝𝐨𝐰:

![codeimage-snippet_7](https://github.com/kaniz-codes/Analog-Clock-Python/assets/138873297/443bec1b-1484-4d6d-a54f-f0a253acc546)

- The code defines a custom class AdvancedAnalogClock that inherits from tk.Tk.
- This class represents the main application window.

3️⃣ 𝐖𝐢𝐧𝐝𝐨𝐰 𝐑𝐞𝐬𝐢𝐳𝐚𝐛𝐢𝐥𝐢𝐭𝐲 𝐚𝐧𝐝 𝐌𝐢𝐧𝐢𝐦𝐮𝐦 𝐒𝐢𝐳𝐞:

![codeimage-snippet_7 (2)](https://github.com/kaniz-codes/Analog-Clock-Python/assets/138873297/7b274b5d-2ad9-4d42-81bf-3b9339012750)

- This code allows the window to be resized both horizontally and vertically (the first 𝐓𝐫𝐮𝐞 argument) and sets a minimum window size of 300 pixels in width and 100 pixels in height.

4️⃣ 𝐭𝐢𝐦𝐞_𝐮𝐩𝐝𝐚𝐭𝐞() 𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧:

![codeimage-snippet_7 (3)](https://github.com/kaniz-codes/Analog-Clock-Python/assets/138873297/92ec5050-8a30-46d4-ad59-6b1648c620e9)

- 𝒕𝒊𝒎𝒆_𝒖𝒑𝒅𝒂𝒕𝒆 is a function defined to update the time and date displayed in the GUI.
- It gets the current time and date using 𝒍𝒐𝒄𝒂𝒍𝒕𝒊𝒎𝒆() and formats them into strings using strftime().
- The formatted time and date strings are then updated in labels (𝒕𝒊𝒎𝒆_𝒍𝒂𝒃𝒆𝒍 𝒂𝒏𝒅 𝒅𝒂𝒕𝒆_𝒍𝒂𝒃𝒆𝒍)).
- Finally, the function schedules itself to run again after 1000 milliseconds (1 second) using 𝒓𝒐𝒐𝒕.𝒂𝒇𝒕𝒆𝒓(1000, 𝒕𝒊𝒎𝒆_𝒖𝒑𝒅𝒂𝒕𝒆
, ensuring that the time is continuously updated.

5️⃣ 𝐂𝐫𝐞𝐚𝐭𝐢𝐧𝐠 𝐚 𝐅𝐫𝐚𝐦𝐞:

![codeimage-snippet_7 (4)](https://github.com/kaniz-codes/Analog-Clock-Python/assets/138873297/7007fb75-fa7a-4f58-a423-267b3820d6db)

- A frame is created to contain the labels (𝒕𝒊𝒎𝒆_𝒍𝒂𝒃𝒆𝒍 𝒂𝒏𝒅 𝒅𝒂𝒕𝒆_𝒍𝒂𝒃𝒆𝒍).
- The frame has a black background with padding (padx and pady) to provide some spacing around the labels.

6️⃣ 𝐂𝐫𝐞𝐚𝐭𝐢𝐧𝐠 𝐋𝐚𝐛𝐞𝐥𝐬 𝐟𝐨𝐫 𝐓𝐢𝐦𝐞 𝐚𝐧𝐝 𝐃𝐚𝐭𝐞:

