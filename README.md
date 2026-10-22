# meta-ai-study-assistant
Smart study planner and task assistant web app for Meta AI Hackathon
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meta AI Study Assistant</title>
    <!-- Tailwind CSS for Modern UI -->
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-slate-900 text-white min-h-screen flex flex-col items-center justify-center p-4">

    <!-- Header Section -->
    <div class="max-w-2xl w-full bg-slate-800 p-6 rounded-2xl shadow-xl border border-slate-700 text-center">
        <div class="flex justify-center items-center gap-2 mb-2">
            <span class="text-3xl">🦙</span>
            <h1 class="text-3xl font-extrabold text-blue-400">Meta AI Study Assistant</h1>
        </div>
        <p class="text-slate-400 text-sm mb-6">Powered by Meta Llama 3 Model | Built for Hackathon</p>

        <!-- Input Box -->
        <div class="text-left mb-4">
            <label for="studyTopic" class="block text-sm font-medium text-slate-300 mb-2">
                Enter your Engineering Subject / Study Plan / Mathematics Topic:
            </label>
            <textarea id="studyTopic" rows="4" 
                class="w-full p-3 bg-slate-900 border border-slate-600 rounded-xl focus:outline-none focus:ring-2 focus:ring-blue-500 text-slate-100 placeholder-slate-500" 
                placeholder="E.g., Engineering Mathematics Matrices, JavaScript Async Functions, or 3-hour study schedule..."></textarea>
        </div>

        <!-- Action Button -->
        <button onclick="generateLlamaResponse()" 
            class="w-full bg-blue-600 hover:bg-blue-500 text-white font-bold py-3 rounded-xl transition duration-200 shadow-lg flex items-center justify-center gap-2">
            <span>⚡ Generate Llama AI Study Plan</span>
        </button>

        <!-- Result Box -->
        <div id="resultBox" class="mt-6 hidden p-4 bg-slate-900 rounded-xl border border-slate-700 text-left">
            <h2 class="text-lg font-bold text-emerald-400 mb-2 border-b border-slate-700 pb-1">
                📌 Meta Llama 3 Output:
            </h2>
            <div id="aiOutput" class="text-slate-300 text-sm leading-relaxed whitespace-pre-line"></div>
        </div>
    </div>

    <script src="app.js"></script>
</body>
</html>
