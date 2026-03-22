import React, { useState, useEffect } from 'react';

export default function SidebarDashboard() {
  const [time, setTime] = useState(new Date());
  const [tasks, setTasks] = useState([]);
  const [newTask, setNewTask] = useState('');

  // Update time every second
  useEffect(() => {
    const timer = setInterval(() => setTime(new Date()), 1000);
    return () => clearInterval(timer);
  }, []);

  // Load tasks from storage on mount
  useEffect(() => {
    const loadTasks = async () => {
      try {
        const result = await window.storage.get('daily-tasks');
        if (result && result.value) {
          setTasks(JSON.parse(result.value));
        }
      } catch (error) {
        console.log('No saved tasks found');
      }
    };
    loadTasks();
  }, []);

  // Save tasks whenever they change
  useEffect(() => {
    const saveTasks = async () => {
      if (tasks.length > 0 || tasks.length === 0) {
        try {
          await window.storage.set('daily-tasks', JSON.stringify(tasks));
        } catch (error) {
          console.error('Error saving tasks:', error);
        }
      }
    };
    saveTasks();
  }, [tasks]);

  const apps = [
    { name: 'Gmail', url: 'https://mail.google.com', icon: '📧' },
    { name: 'YouTube', url: 'https://youtube.com', icon: '▶️' },
    { name: 'Google', url: 'https://google.com', icon: '🔍' },
    { name: 'Spotify', url: 'https://open.spotify.com', icon: '🎵' },
    { name: 'Meet', url: 'https://meet.google.com', icon: '📹' },
    { name: 'Docs', url: 'https://docs.google.com', icon: '📄' },
  ];

  const formatTime = (date) => {
    return date.toLocaleTimeString('en-AU', { 
      hour: '2-digit', 
      minute: '2-digit',
      hour12: false 
    });
  };

  const formatDate = (date) => {
    return date.toLocaleDateString('en-AU', { 
      weekday: 'long',
      day: 'numeric',
      month: 'long',
      year: 'numeric'
    });
  };

  const addTask = () => {
    if (newTask.trim()) {
      setTasks([...tasks, { id: Date.now(), text: newTask, completed: false }]);
      setNewTask('');
    }
  };

  const toggleTask = (id) => {
    setTasks(tasks.map(task => 
      task.id === id ? { ...task, completed: !task.completed } : task
    ));
  };

  const deleteTask = (id) => {
    setTasks(tasks.filter(task => task.id !== id));
  };

  return (
    <div className="min-h-screen bg-zinc-950 text-zinc-100 p-6 font-mono flex">
      
      {/* Left side - Time & Date (70%) */}
      <div className="w-[70%] flex items-center justify-center">
        <div className="text-center">
          <div className="text-8xl font-light mb-4">{formatTime(time)}</div>
          <div className="text-2xl text-zinc-500">{formatDate(time)}</div>
        </div>
      </div>

      {/* Right side - Apps & Tasks (30%) */}
      <div className="w-[30%] flex flex-col gap-8 pl-8">
        
        {/* Apps Grid */}
        <div>
          <div className="text-xs text-zinc-600 mb-3 uppercase tracking-wider">Quick Access</div>
          <div className="grid grid-cols-2 gap-3">
            {apps.map((app) => (
              <a
                key={app.name}
                href={app.url}
                target="_blank"
                rel="noopener noreferrer"
                className="bg-zinc-900 hover:bg-zinc-800 border border-zinc-800 p-4 rounded transition-colors flex flex-col items-center justify-center gap-2 text-center"
              >
                <span className="text-2xl">{app.icon}</span>
                <span className="text-xs text-zinc-400">{app.name}</span>
              </a>
            ))}
          </div>
        </div>

        {/* Tasks */}
        <div className="flex-1">
          <div className="text-xs text-zinc-600 mb-3 uppercase tracking-wider">Today's Tasks</div>
          
          {/* Add Task Input */}
          <div className="flex gap-2 mb-4">
            <input
              type="text"
              value={newTask}
              onChange={(e) => setNewTask(e.target.value)}
              onKeyPress={(e) => e.key === 'Enter' && addTask()}
              placeholder="Add a task..."
              className="flex-1 bg-zinc-900 border border-zinc-800 rounded px-3 py-2 text-sm focus:outline-none focus:border-zinc-700"
            />
            <button
              onClick={addTask}
              className="bg-zinc-800 hover:bg-zinc-700 border border-zinc-700 px-4 py-2 rounded text-sm transition-colors"
            >
              +
            </button>
          </div>

          {/* Task List */}
          <div className="space-y-2">
            {tasks.length === 0 ? (
              <div className="text-zinc-600 text-sm italic">No tasks yet</div>
            ) : (
              tasks.map((task) => (
                <div
                  key={task.id}
                  className="flex items-center gap-3 bg-zinc-900 border border-zinc-800 rounded px-3 py-2 group"
                >
                  <input
                    type="checkbox"
                    checked={task.completed}
                    onChange={() => toggleTask(task.id)}
                    className="w-4 h-4 cursor-pointer"
                  />
                  <span
                    className={`flex-1 text-sm ${
                      task.completed ? 'line-through text-zinc-600' : 'text-zinc-300'
                    }`}
                  >
                    {task.text}
                  </span>
                  <button
                    onClick={() => deleteTask(task.id)}
                    className="text-zinc-600 hover:text-zinc-400 opacity-0 group-hover:opacity-100 transition-opacity text-xs"
                  >
                    ✕
                  </button>
                </div>
              ))
            )}
          </div>
        </div>

      </div>
    </div>
  );
}
