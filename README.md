# Git-hub
// File: src/App.js import React from 'react'; import Header from './components/Header'; import Sidebar from './components/Sidebar'; import DashboardMainContent from './components/DashboardMainContent'; import './styles/App.css';

function App() { return ( <div className="app-container"> <Sidebar /> <div className="main-content"> <Header /> <DashboardMainContent /> </div> </div> ); }

export default App;

// File: src/components/Header.js import React from 'react'; import './Header.css'; import { Bell, Plus } from 'lucide-react';

function Header() { return ( <header className="header"> <div className="logo">Healthcare.</div> <div className="search-bar"><input type="text" placeholder="Search..." disabled /></div> <div className="header-actions"> <Bell /> <div className="user-profile"> <img src="/assets/avatar.png" alt="User" /> <span>John Doe</span> </div> <button className="add-button"><Plus /></button> </div> </header> ); }

export default Header;

// File: src/components/Sidebar.js import React from 'react'; import './Sidebar.css'; import { navLinks } from '../data/navigation';

function Sidebar() { return ( <aside className="sidebar"> <h3>General</h3> <ul> {navLinks.map(link => ( <li key={link.label}><link.icon /> {link.label}</li> ))} </ul> </aside> ); }

export default Sidebar;

// File: src/components/DashboardMainContent.js import React from 'react'; import DashboardOverview from './DashboardOverview'; import AnatomySection from './AnatomySection'; import HealthStatusCards from './HealthStatusCards'; import CalendarView from './CalendarView'; import UpcomingSchedule from './UpcomingSchedule'; import ActivityFeed from './ActivityFeed'; import './DashboardMainContent.css';

function DashboardMainContent() { return ( <main className="dashboard-main"> <DashboardOverview /> <div className="main-grid"> <AnatomySection /> <HealthStatusCards /> <CalendarView /> <UpcomingSchedule /> <ActivityFeed /> </div> </main> ); }

export default DashboardMainContent;

// You will also create the remaining components: DashboardOverview, AnatomySection, HealthStatusCards, CalendarView, UpcomingSchedule, ActivityFeed, SimpleAppointmentCard

// File: src/data/navigation.js import { LayoutDashboard, Clock, Calendar, ClipboardList, BarChart2, Activity, MessageSquare, HelpCircle, Settings } from 'lucide-react';

