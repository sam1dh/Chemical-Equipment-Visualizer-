# Chemical-Equipment-Visualizer
# Chemical Equipment Parameter Visualizer 🧪

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Django](https://img.shields.io/badge/Django-4.2-green.svg)
![React](https://img.shields.io/badge/React-18.2-61dafb.svg)
![PyQt5](https://img.shields.io/badge/PyQt5-5.15-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A **hybrid web and desktop application** for visualizing and analyzing chemical equipment parameters. Built with Django REST Framework backend, React web frontend, and PyQt5 desktop application with Matplotlib visualizations.

## 🌟 Features

### 🌐 Web Application (React)
- **Modern UI** with responsive design
- **Interactive dashboards** with real-time data
- **Chart.js visualizations** for equipment analysis
- **CSV upload** with drag & drop
- **PDF report generation**
- **Browser-based** - no installation required

### 🖥️ Desktop Application (PyQt5)
- **Native desktop experience** for Windows, macOS, Linux
- **Matplotlib integration** for publication-quality charts
- **Offline-capable** with local data processing
- **Rich GUI** with tabbed interface
- **File system integration** for easy data management
- **Professional visualizations** with multiple chart types

### 🔧 Backend (Django REST API)
- **RESTful API** serving both frontends
- **Pandas-powered** data analysis
- **SQLite database** for persistent storage
- **History management** - stores last 5 datasets
- **Authentication support**
- **Automatic data validation**

## 📸 Screenshots

### Dashboard View
![Dashboard](https://via.placeholder.com/800x400?text=Dashboard+Screenshot)

### Upload Interface
![Upload](https://via.placeholder.com/800x400?text=Upload+Screenshot)

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend (Web)** | React 18.2 + Chart.js | Interactive web UI |
| **Frontend (Desktop)** | PyQt5 5.15 + Matplotlib | Native desktop application |
| **Backend** | Django 4.2 + DRF | REST API server |
| **Data Processing** | Pandas 2.1 | CSV analysis & statistics |
| **Database** | SQLite | Data persistence |
| **PDF Generation** | ReportLab | Professional reports |
| **HTTP Client** | Requests | Desktop-to-API communication |

## 📋 Prerequisites

- Python 3.8 or higher
- Node.js 16+ and npm
- Git
- pip and virtualenv

## 🚀 Quick Start

### Option 1: Automated Setup (Recommended)

**Linux/Mac:**
```bash
git clone https://github.com/yourusername/chemical-equipment-visualizer.git
cd chemical-equipment-visualizer
chmod +x setup.sh
./setup.sh
```

**Windows:**
```bash
git clone https://github.com/yourusername/chemical-equipment-visualizer.git
cd chemical-equipment-visualizer
setup.bat
```

### Option 2: Manual Setup

#### 1️⃣ Backend (Django)
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

#### 2️⃣ Web Frontend (React)
```bash
cd frontend
npm install
npm start
```

#### 3️⃣ Desktop Application (PyQt5)
```bash
cd desktop
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

### 🎯 Access Applications

- **Backend API**: http://localhost:8000/api/
- **Web App**: http://localhost:3000
- **Admin Panel**: http://localhost:8000/admin/
- **Desktop App**: Launch via `python main.py`

## 📊 Sample Data

A sample CSV file is provided in the repository: `sample_equipment_data.csv`

**Required CSV Format:**
```csv
Equipment Name,Type,Flowrate,Pressure,Temperature
Reactor-A1,Reactor,150.5,25.3,220.0
Heat Exchanger-B2,Heat Exchanger,200.0,15.8,180.5
...
```

## 🔐 Authentication

### Using Django Admin
1. Navigate to `http://localhost:8000/admin/`
2. Login with superuser credentials
3. Session authentication will be active

### API Access
- Session-based authentication
- Token authentication (optional)

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/datasets/` | List last 5 datasets |
| POST | `/api/datasets/upload/` | Upload CSV file |
| GET | `/api/datasets/{id}/` | Get dataset details |
| GET | `/api/datasets/{id}/generate_pdf/` | Download PDF report |

## 🎨 UI Components

### Web Application (React)
<table>
<tr>
<td width="50%">

**Dashboard**
- Summary statistics cards
- Equipment type distribution charts
- Parameter range visualizations
- Interactive data tables

</td>
<td width="50%">

**Features**
- Real-time chart updates
- Responsive design
- Mobile-friendly
- Modern UI with Tailwind

</td>
</tr>
</table>

### Desktop Application (PyQt5)
<table>
<tr>
<td width="50%">

**Tabs**
- 📤 Upload CSV
- 📊 Dashboard
- 📈 Visualizations
- 📋 Data Table
- 🕐 History

</td>
<td width="50%">

**Charts**
- Bar charts (equipment types)
- Pie charts (distribution)
- Multi-parameter comparisons
- Publication-quality exports

</td>
</tr>
</table>

## 🖥️ Desktop Application (PyQt5)

Coming soon! Desktop version with:
- Native OS integration
- Offline functionality
- Matplotlib-based visualizations
- Same backend API

## 📁 Project Structure

```
chemical-equipment-visualizer/
├── backend/                    # Django REST API
│   ├── chemical_equipment/     # Project settings
│   ├── equipment/              # Main app
│   ├── media/                  # Uploaded files
│   ├── manage.py
│   └── requirements.txt
├── frontend/                   # React Web App
│   ├── src/
│   │   ├── App.js             # Main component
│   │   └── index.js
│   ├── package.json
│   └── ...
├── desktop/                    # PyQt5 Desktop App
│   ├── main.py                # Main application
│   ├── requirements.txt
│   ├── run.sh                 # Linux/Mac launcher
│   └── run.bat                # Windows launcher
├── sample_equipment_data.csv   # Test data
├── .gitignore
├── README.md
└── SETUP.md                    # Detailed setup guide
```

## 🧪 Testing

### Backend Tests
```bash
cd backend
python manage.py test
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 🐛 Troubleshooting

### CORS Issues
Ensure `django-cors-headers` is properly configured in `settings.py`

### Port Conflicts
- Backend: `python manage.py runserver 8001`
- Frontend: `PORT=3001 npm start`

### Database Reset
```bash
rm db.sqlite3
python manage.py migrate
python manage.py createsuperuser
```

## 📈 Future Enhancements

- [ ] Real-time data updates with WebSockets
- [ ] Advanced analytics and ML predictions
- [ ] Multi-user support with role-based access
- [ ] Export to Excel and JSON formats
- [ ] Mobile app version
- [ ] Docker containerization
- [ ] CI/CD pipeline
- [ ] Unit test coverage > 80%

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- Your Name - [GitHub](https://github.com/yourusername)

## 🙏 Acknowledgments

- Django REST Framework documentation
- React documentation
- Pandas community
- Tailwind CSS team

## 📞 Contact

- Email: your.email@example.com
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)
- Project Link: [https://github.com/yourusername/chemical-equipment-visualizer](https://github.com/yourusername/chemical-equipment-visualizer)

---

**Made with ❤️ for Chemical Engineering Data Analysis**