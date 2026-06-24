# ultimate_tracker.py
Project 2 - Custom Management System
<!DOCTYPE html>
<html>
<head>
    <title>Academic Study Tracker Portal</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light p-5">
    <div class="container bg-white p-4 shadow-sm rounded">
        <h2 class="fw-bold text-dark mb-4">📊 Study Tracker Dashboard</h2>
        
        <div class="row g-3 mb-4">
            <div class="col-md-4">
                <div class="p-3 bg-primary text-white rounded">
                    <h6>Total Tracked Runs</h6>
                    <h3>{{ total_count }}</h3>
                </div>
            </div>
        </div>

        <form action="/log-session" method="POST" class="row g-3 mb-4 align-items-end">
            <div class="col-md-4">
                <label class="form-label font-monospace small">Subject Title</label>
                <input type="text" name="subject" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Duration (Mins)</label>
                <input type="number" name="duration" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Execution Date</label>
                <input type="date" name="date" class="form-control" required>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-dark w-100">Log Session</button>
            </div>
        </form>

        <table class="table table-striped border">
            <thead class="table-dark">
                <tr>
                    <th>Date</th>
                    <th>Subject</th>
                    <th>Duration</th>
                </tr>
            </thead>
            <tbody>
                {% for session in sessions %}
                <tr>
                    <td>{{ session.date }}</td>
                    <td><strong>{{ session.subject }}</strong></td>
                    <td>{{ session.duration }} mins</td>
                </tr>
                {% endfor %}
            </tbody>
        </table>
    </div>
</body>
</html><!DOCTYPE html>
<html>
<head>
    <title>Academic Study Tracker Portal</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light p-5">
    <div class="container bg-white p-4 shadow-sm rounded">
        <h2 class="fw-bold text-dark mb-4">📊 Study Tracker Dashboard</h2>
        
        <div class="row g-3 mb-4">
            <div class="col-md-4">
                <div class="p-3 bg-primary text-white rounded">
                    <h6>Total Tracked Runs</h6>
                    <h3>{{ total_count }}</h3>
                </div>
            </div>
        </div>

        <form action="/log-session" method="POST" class="row g-3 mb-4 align-items-end">
            <div class="col-md-4">
                <label class="form-label font-monospace small">Subject Title</label>
                <input type="text" name="subject" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Duration (Mins)</label>
                <input type="number" name="duration" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Execution Date</label>
                <input type="date" name="date" class="form-control" required>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-dark w-100">Log Session</button>
            </div>
        </form>

        <table class="table table-striped border">
            <thead class="table-dark">
                <tr>
                    <th>Date</th>
                    <th>Subject</th>
                    <th>Duration</th>
                </tr>
            </thead>
            <tbody>
                {% for session in sessions %}
                <tr>
                    <td>{{ session.date }}</td>
                    <td><strong>{{ session.subject }}</strong></td>
                    <td>{{ session.duration }} mins</td>
                </tr>
                {% endfor %}
            </tbody>
        </table>
    </div>
</body>
</html><!DOCTYPE html>
<html>
<head>
    <title>Academic Study Tracker Portal</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light p-5">
    <div class="container bg-white p-4 shadow-sm rounded">
        <h2 class="fw-bold text-dark mb-4">📊 Study Tracker Dashboard</h2>
        
        <div class="row g-3 mb-4">
            <div class="col-md-4">
                <div class="p-3 bg-primary text-white rounded">
                    <h6>Total Tracked Runs</h6>
                    <h3>{{ total_count }}</h3>
                </div>
            </div>
        </div>

        <form action="/log-session" method="POST" class="row g-3 mb-4 align-items-end">
            <div class="col-md-4">
                <label class="form-label font-monospace small">Subject Title</label>
                <input type="text" name="subject" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Duration (Mins)</label>
                <input type="number" name="duration" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Execution Date</label>
                <input type="date" name="date" class="form-control" required>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-dark w-100">Log Session</button>
            </div>
        </form>

        <table class="table table-striped border">
            <thead class="table-dark">
                <tr>
                    <th>Date</th>
                    <th>Subject</th>
                    <th>Duration</th>
                </tr>
            </thead>
            <tbody>
                {% for session in sessions %}
                <tr>
                    <td>{{ session.date }}</td>
                    <td><strong>{{ session.subject }}</strong></td>
                    <td>{{ session.duration }} mins</td>
                </tr>
                {% endfor %}
            </tbody>
        </table>
    </div>
</body>
</html><!DOCTYPE html>
<html>
<head>
    <title>Academic Study Tracker Portal</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light p-5">
    <div class="container bg-white p-4 shadow-sm rounded">
        <h2 class="fw-bold text-dark mb-4">📊 Study Tracker Dashboard</h2>
        
        <div class="row g-3 mb-4">
            <div class="col-md-4">
                <div class="p-3 bg-primary text-white rounded">
                    <h6>Total Tracked Runs</h6>
                    <h3>{{ total_count }}</h3>
                </div>
            </div>
        </div>

        <form action="/log-session" method="POST" class="row g-3 mb-4 align-items-end">
            <div class="col-md-4">
                <label class="form-label font-monospace small">Subject Title</label>
                <input type="text" name="subject" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Duration (Mins)</label>
                <input type="number" name="duration" class="form-control" required>
            </div>
            <div class="col-md-3">
                <label class="form-label font-monospace small">Execution Date</label>
                <input type="date" name="date" class="form-control" required>
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-dark w-100">Log Session</button>
            </div>
        </form>

        <table class="table table-striped border">
            <thead class="table-dark">
                <tr>
                    <th>Date</th>
                    <th>Subject</th>
                    <th>Duration</th>
                </tr>
            </thead>
            <tbody>
                {% for session in sessions %}
                <tr>
                    <td>{{ session.date }}</td>
                    <td><strong>{{ session.subject }}</strong></td>
                    <td>{{ session.duration }} mins</td>
                </tr>
                {% endfor %}
            </tbody>
        </table>
    </div>
</body>
</html>
