import { useState } from "react";

function App() {
  const [data, setData] = useState("");
  const [allData, setAllData] = useState([]);

  const handleSubmit = () => {
    if (data.trim() !== "") {
      const newData = {
        id: Date.now(),
        text: data,
      };
      setAllData([...allData, newData]);
      setData("");
    }
  };

  const deleteHandler = (id) => {
    setAllData(allData.filter((item) => item.id !== id));
  };
  // console.log("alldata", allData);

  return (
    <div className="min-h-screen bg-gradient-to-br from-purple-100 to-blue-100 py-8 px-4">
      <div className="max-w-2xl mx-auto">
        <h1 className="text-4xl font-bold text-center text-gray-800 mb-8">
          To-Do List
        </h1>

        <div className="flex flex-col sm:flex-row gap-2 mb-8">
          <input
            className="flex-1 px-4 py-2 rounded-lg border border-gray-300 focus:border-purple-500 focus:ring-2 focus:ring-purple-200 focus:outline-none transition-colors shadow-sm"
            type="text"
            value={data}
            placeholder="Add a new task"
            onChange={(e) => setData(e.target.value)}
          />
          <button
            className="px-6 py-2 bg-purple-600 text-white rounded-lg hover:bg-purple-700 transition-colors duration-200 shadow-sm font-medium"
            onClick={handleSubmit}
          >
            Add Task
          </button>
        </div>

        <div className="space-y-4  ">
          {allData.map((item) => (
            <div
              key={item.id}
              className="bg-white rounded-lg shadow-sm p-4 flex items-center justify-between animate-fade-in"
            >
              <p className="text-gray-800 font-medium">{item.text}</p>
              <button
                className="px-6 py-3  bg-red-500 text-white rounded-lg hover:bg-red-600 transition-colors duration-200 text-sm font-medium"
                onClick={() => deleteHandler(item.id)}
              >
                Delete
              </button>
              <button className="px-6 py-2 bg-yellow-500 text-white rounded-lg hover:bg-yellow-600 transition-transform transform hover:scale-105 hover:shadow-lg border-2 border-transparent hover:border-yellow-700 font-medium">
                Edit
              </button>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
}

export default App;
