from flask import Flask, render_template, request, redirect, url_for

app = Flask(__name__)

# Temporary in-memory database
study_sessions = [
    {"date": "2026-06-24", "subject": "Data Structures", "duration": 45},
    {"date": "2026-06-25", "subject": "Python Basics", "duration": 60}
]

@app.route('/')
def index():
    total_count = len(study_sessions)
    return render_template('index.html', total_count=total_count, sessions=study_sessions)

@app.route('/log-session', methods=['POST'])
def log_session():
    subject = request.form.get('subject')
    duration = request.form.get('duration')
    date = request.form.get('date')
    
    if subject and duration and date:
        study_sessions.append({
            "date": date,
            "subject": subject,
            "duration": int(duration)
        })
        
    return redirect(url_for('index'))

if __name__ == '__main__':
    app.run(debug=True)
