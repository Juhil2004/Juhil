# Juhil
from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/', methods=['GET'])
def home():
    return jsonify({"message": "Welcome to my Flask Web Service!"})

@app.route('/api/users', methods=['GET'])
def get_users():
    users = [
        {"id": 1, "name": "juhil"},
        {"id": 2, "name": "kohli"},
        {"id": 3, "name": "prince"}
        ]
    return jsonify(users), 200

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000, debug=True)
