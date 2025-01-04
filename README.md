# Want to create an schedule page for for you website where you can have the post just like shown blow then your in click download the schedule.html and get the code 

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estimated Schedule</title>
    <style>
        /* Styling the Schedule Section */
        #schedule-container {
            padding: 20px;
            background-color: #1c1c2b;
            /* Dark background */
            color: #fff;
            font-family: Arial, sans-serif;
            border-radius: 10px;
            max-width: 800px;
            margin: 20px auto;
        }

        #current-time {
            text-align: right;
            margin-bottom: 20px;
            font-size: 1rem;
            color: #aaa;
        }

        .day-buttons {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-bottom: 20px;
        }

        .day-button {
            padding: 10px 15px;
            background-color: #333;
            color: #fff;
            border: 1px solid #444;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .day-button:hover,
        .day-button.active {
            background-color: #ff5ea2;
            border-color: transparent;
        }

        .schedule-list {
            font-size: 1rem;
        }

        .schedule-item {
            margin: 10px 0;
            display: flex;
            justify-content: space-between;
            padding: 10px;
            background-color: #2c2c3b;
            border-radius: 5px;
        }

        .schedule-item .time {
            font-weight: bold;
            color: #ff5ea2;
        }

        .schedule-item .title {
            flex-grow: 1;
            margin-left: 10px;
        }

        .schedule-item .episode {
            color: #aaa;
        }
    </style>
</head>

<body>
    <div id="schedule-container">
        <!-- Current Time -->
        <div id="current-time"></div>

        <!-- Day Buttons -->
        <div id="day-buttons" class="day-buttons"></div>

        <!-- Schedule List -->
        <div id="schedule-list" class="schedule-list"></div>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", () => {
            const scheduleContainer = document.getElementById("schedule-container");
            const currentTimeEl = document.getElementById("current-time");
            const dayButtonsEl = document.getElementById("day-buttons");
            const scheduleListEl = document.getElementById("schedule-list");

            // Example JSON Data (Replace this with server-fetching logic)
            const data = {
                "currentTime": "2025-01-04T01:22:44+05:00", // Server time in ISO format
                "days": ["Sat", "Sun", "Mon", "Tue", "Wed", "Thu", "Fri"],
                "schedule": {
                    "Sat": [
                        { "time": "06:00", "title": "Himitsu no AiPri", "episode": "Episode 38" },
                        { "time": "08:00", "title": "Hamidashi Creative", "episode": "Episode 12" },
                        { "time": "14:00", "title": "Beheneko: The Elf-Girl's Cat is Secretly an S-Ranked Monster!", "episode": "Episode 13" }
                    ],
                    "Sun": [
                        { "time": "06:00", "title": "Tonbo! Season 2", "episode": "Episode 2" },
                        { "time": "17:30", "title": "Case Closed", "episode": "Episode 1148" }
                    ]
                }
            };

            // Convert server time to user's local time
            const serverTime = new Date(data.currentTime); // Server-provided time
            const userTimeOffset = new Date().getTimezoneOffset() * 60000; // User's timezone offset in ms
            const localTime = new Date(serverTime.getTime() - userTimeOffset); // Adjusted to user's local timezone

            // Update the current time dynamically
            const updateTime = () => {
                const now = new Date();
                currentTimeEl.textContent = `(${now.toLocaleTimeString()} ${Intl.DateTimeFormat().resolvedOptions().timeZone}) ${now.toDateString()}`;
            };
            updateTime();
            setInterval(updateTime, 1000);

            // Render day buttons
            data.days.forEach((day) => {
                const button = document.createElement("button");
                button.textContent = day;
                button.className = "day-button";
                button.onclick = () => renderSchedule(day);
                dayButtonsEl.appendChild(button);
            });

            // Render the schedule for the first day
            renderSchedule(data.days[0]);

            function renderSchedule(day) {
                // Highlight active day button
                document.querySelectorAll(".day-button").forEach((btn) => btn.classList.remove("active"));
                document.querySelector(`.day-button:nth-child(${data.days.indexOf(day) + 1})`).classList.add("active");

                // Update the schedule list
                scheduleListEl.innerHTML = "";
                (data.schedule[day] || []).forEach((item) => {
                    const scheduleItem = document.createElement("div");
                    scheduleItem.className = "schedule-item";
                    scheduleItem.innerHTML = `
                        <span class="time">${item.time}</span>
                        <span class="title">${item.title}</span>
                        <span class="episode">${item.episode}</span>
                    `;
                    scheduleListEl.appendChild(scheduleItem);
                });
            }
        });
    </script>
</body>

</html>


# 4D-Results
The 4D Result a place to learn about the lottery Results
<body>
    <a rel="follow" title="4D Result" target="_blank" href="https://4dresult.cfd">
        <img alt="' . $imageAlt . '" style="width: 15px;float: left;margin-right: 3px;" src="https://cdn-icons-png.flaticon.com/128/724/724816.png">
        4D Result
    </a>
</body>
</html>

looking to how to check your Lesco Bill download Lesco-Bill or want to pay the bills look no further as you can do so at 
<body>
    <a rel="follow" title="Lesco Bill" target="_blank" href="http://lesco-bill.org.pk/">
        <img alt="' . $imageAlt . '" style="width: 15px;float: left;margin-right: 3px;" src="https://cdn-icons-png.flaticon.com/128/724/724816.png">
        Lesco Bill
    </a>
</body>
</html>
