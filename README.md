<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Academic Study Tracker Portal</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light p-4">
    <div class="container">
        <h2>📊 Study Tracker Dashboard</h2>

        # 📊 Academic Study Tracker Portal

A simple, browser-based dashboard to log and keep track of study session lengths and subjects over time.

## 🚀 Features
* Log study subjects, completion dates, and total minutes.
* Automated run tracking counters.
* Saves historical sessions automatically via browser `localStorage`.

        <div class="row g-3 mb-4 mt-2">
            <div class="col-md-4">
                <div class="p-3 bg-primary text-white rounded">
                    <h6>Total Tracked Runs</h6>
                    <h3 id="total-count">0</h3>
                </div>
            </div>
        </div>

        <form id="session-form" class="row g-3 mb-4 align-items-end">
            <div class="col-md-4">
                <label class="form-label font-monospace small">Subject Title</label>
                <input type="text" id="subject" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Duration (Mins)</label>
                <input type="number" id="duration" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Execution Date</label>
                <input type="date" id="date" class="form-control" required>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-dark w-100">Log Session</button>
            </div>
        </form>

        <table class="table table-striped border bg-white">
            <thead class="table-dark">
                <tr>
                    <th>Date</th>
                    <th>Subject</th>
                    <th>Duration</th>
                </tr>
            </thead>
            <tbody id="sessions-table-body">
                </tbody>
        </table>
    </div>

    <script>
        // Load existing sessions from localStorage or start with default data
        let studySessions = JSON.parse(localStorage.getItem('studySessions')) || [
            {date: "2026-06-24", subject: "Data Structures", duration: 45},
            {date: "2026-06-25", subject: "Python Basics", duration: 60}
        ];

        const form = document.getElementById('session-form');
        const tableBody = document.getElementById('sessions-table-body');
        const totalCountEl = document.getElementById('total-count');

        function updateUI() {
            // Clear current table contents
            tableBody.innerHTML = '';
            
            // Populate rows
            studySessions.forEach(session => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${session.date}</td>
                    <td><strong>${session.subject}</strong></td>
                    <td>${session.duration} mins</td>
                `;
                tableBody.appendChild(row);
            });

            // Update counter
            totalCountEl.textContent = studySessions.length;
            
            // Save data locally in browser
            localStorage.setItem('studySessions', JSON.stringify(studySessions));
        }

        // Handle form submission
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const newSession = {
                subject: document.getElementById('subject').value,
                duration: parseInt(document.getElementById('duration').value),
                date: document.getElementById('date').value
            };

            studySessions.push(newSession);
            updateUI();
            form.reset();
        });

        // Initial render
        updateUI();
    </script>
</body>
</html>
