
<html lang="en" class="h-full">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SITANSHU - Profile & Details Cloud Portal</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter Font -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        body { font-family: 'Inter', sans-serif; }
        .slide-up {
            animation: slideUp 0.4s ease-out forwards;
        }
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="h-full bg-slate-900 text-slate-100 flex flex-col justify-center items-center p-4">

    <div class="w-full max-w-lg bg-slate-800 border border-slate-700/60 rounded-2xl shadow-2xl overflow-hidden slide-up my-auto">
        
        <!-- Header Banner -->
        <div class="bg-gradient-to-r from-indigo-600 to-violet-600 p-6 text-center relative">
            <div class="absolute top-4 right-4 bg-white/15 backdrop-blur-md px-3 py-1 rounded-full text-xs font-medium text-indigo-100">
                <i class="fa-solid fa-cloud-arrow-up mr-1"></i> Cloud Sync
            </div>
            <div class="w-16 h-16 bg-white/15 backdrop-blur-md rounded-2xl mx-auto flex items-center justify-center text-3xl text-white mb-3 shadow-inner">
                <i class="fa-solid fa-database"></i>
            </div>
            <h1 class="text-2xl font-bold tracking-tight text-white">SITANSHU PORTAL</h1>
            <p class="text-indigo-200 text-sm mt-1">Mobile Verification & Cloud Storage</p>
        </div>

        <!-- Body Content -->
        <div class="p-6 sm:p-8">

            <!-- STEP 1: Phone Number Input Form -->
            <div id="step-phone" class="space-y-6">
                <div>
                    <label class="block text-sm font-medium text-slate-300 mb-2">Enter Mobile Number</label>
                    <div class="relative flex items-center">
                        <div class="absolute inset-y-0 left-0 flex items-center pl-4 pointer-events-none text-slate-400 font-medium">
                            +91
                        </div>
                        <input type="tel" id="phone-input" maxlength="10" placeholder="9876543210" 
                            class="w-full pl-14 pr-4 py-3.5 bg-slate-900 border border-slate-700 rounded-xl text-white placeholder-slate-500 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:border-transparent text-lg tracking-wider font-medium transition-all">
                    </div>
                    <p class="text-xs text-slate-400 mt-2 flex items-center">
                        <i class="fa-solid fa-circle-info mr-1.5 text-indigo-400"></i> We will send a 6-digit OTP verification code via SMS.
                    </p>
                </div>

                <button onclick="sendOtp()" id="send-btn" class="w-full bg-indigo-600 hover:bg-indigo-500 active:scale-[0.98] text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-indigo-600/30 transition-all flex items-center justify-center space-x-2">
                    <span>Send Verification OTP</span>
                    <i class="fa-solid fa-arrow-right-long text-sm"></i>
                </button>
            </div>

            <!-- STEP 2: OTP Verification Form -->
            <div id="step-otp" class="space-y-6 hidden">
                <div class="text-center">
                    <p class="text-sm text-slate-300">Code sent successfully to</p>
                    <div class="flex items-center justify-center space-x-2 mt-1">
                        <span id="display-phone" class="font-bold text-lg text-white tracking-wide">+91 98765 43210</span>
                        <button onclick="editPhone()" class="text-xs text-indigo-400 hover:text-indigo-300 underline font-medium">Change</button>
                    </div>
                    <!-- Simulation Alert Badge -->
                    <div id="otp-hint-badge" class="mt-3 inline-block bg-amber-500/10 border border-amber-500/30 text-amber-300 px-3 py-1.5 rounded-lg text-xs font-medium">
                        <i class="fa-solid fa-key mr-1"></i> Demo OTP: <strong id="demo-otp-val" class="tracking-widest">123456</strong>
                    </div>
                </div>

                <!-- 6 Digit Input Boxes -->
                <div>
                    <label class="block text-sm font-medium text-slate-300 mb-3 text-center">Enter 6-Digit OTP Code</label>
                    <div class="flex justify-between gap-2 sm:gap-3">
                        <input type="text" maxlength="1" class="otp-input w-12 h-12 text-center text-xl font-bold bg-slate-900 border border-slate-700 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-indigo-500" oninput="handleOtpInput(this, 0)" onkeydown="handleOtpKeyDown(event, 0)">
                        <input type="text" maxlength="1" class="otp-input w-12 h-12 text-center text-xl font-bold bg-slate-900 border border-slate-700 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-indigo-500" oninput="handleOtpInput(this, 1)" onkeydown="handleOtpKeyDown(event, 1)">
                        <input type="text" maxlength="1" class="otp-input w-12 h-12 text-center text-xl font-bold bg-slate-900 border border-slate-700 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-indigo-500" oninput="handleOtpInput(this, 2)" onkeydown="handleOtpKeyDown(event, 2)">
                        <input type="text" maxlength="1" class="otp-input w-12 h-12 text-center text-xl font-bold bg-slate-900 border border-slate-700 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-indigo-500" oninput="handleOtpInput(this, 3)" onkeydown="handleOtpKeyDown(event, 3)">
                        <input type="text" maxlength="1" class="otp-input w-12 h-12 text-center text-xl font-bold bg-slate-900 border border-slate-700 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-indigo-500" oninput="handleOtpInput(this, 4)" onkeydown="handleOtpKeyDown(event, 4)">
                        <input type="text" maxlength="1" class="otp-input w-12 h-12 text-center text-xl font-bold bg-slate-900 border border-slate-700 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-indigo-500" oninput="handleOtpInput(this, 5)" onkeydown="handleOtpKeyDown(event, 5)">
                    </div>
                </div>

                <button onclick="verifyOtp()" id="verify-btn" class="w-full bg-emerald-600 hover:bg-emerald-500 active:scale-[0.98] text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-emerald-600/30 transition-all flex items-center justify-center space-x-2">
                    <span>Verify & Proceed</span>
                    <i class="fa-solid fa-circle-check"></i>
                </button>

                <!-- Resend & Timer -->
                <div class="text-center text-sm text-slate-400">
                    <p id="timer-text">Resend OTP in <span id="countdown" class="font-semibold text-indigo-400">30</span>s</p>
                    <button onclick="resendOtp()" id="resend-btn" class="hidden text-indigo-400 hover:text-indigo-300 font-semibold underline mt-1">Resend New OTP</button>
                </div>
            </div>

            <!-- STEP 3: Success Dashboard with SITANSHU & Short Answer Questions -->
            <div id="step-success" class="space-y-6 hidden">
                <div class="text-center pb-2 border-b border-slate-700 flex justify-between items-center">
                    <div>
                        <h2 class="text-lg font-bold text-white text-left">Welcome, <span class="text-indigo-400 underline decoration-indigo-500/50">SITANSHU</span>!</h2>
                        <p class="text-slate-400 text-xs text-left mt-0.5">Phone: <span id="success-phone" class="font-semibold text-slate-200">+91 9876543210</span></p>
                    </div>
                    <!-- View Cloud Logs Button -->
                    <button onclick="openCloudLogsModal()" class="bg-indigo-600/20 hover:bg-indigo-600/30 border border-indigo-500/40 text-indigo-300 px-3 py-1.5 rounded-xl text-xs font-semibold transition-all flex items-center space-x-1.5">
                        <i class="fa-solid fa-database"></i>
                        <span>View Saved Logs</span>
                    </button>
                </div>

                <!-- Questionnaire Container -->
                <div class="space-y-4 max-h-[380px] overflow-y-auto pr-1">
                    <div class="flex items-center justify-between">
                        <h3 class="text-sm font-bold text-slate-200 uppercase tracking-wider"><i class="fa-solid fa-pen-to-square mr-1.5 text-indigo-400"></i> Details Questionnaire</h3>
                        <span id="quiz-progress" class="text-xs font-medium text-indigo-300 bg-indigo-500/20 px-2.5 py-1 rounded-full">Question 1 of 6</span>
                    </div>

                    <div id="quiz-card" class="bg-slate-900/80 border border-slate-700/60 p-4 rounded-xl space-y-4">
                        <p id="question-text" class="text-sm font-medium text-slate-100 leading-relaxed"></p>
                        <!-- Short text input field -->
                        <div class="space-y-3">
                            <input type="text" id="short-answer-input" placeholder="Type your answer here..." 
                                class="w-full px-4 py-3 bg-slate-800 border border-slate-700 rounded-xl text-white placeholder-slate-500 focus:outline-none focus:ring-2 focus:ring-indigo-500 text-sm font-medium">
                            <button onclick="submitShortAnswer()" class="w-full bg-indigo-600 hover:bg-indigo-500 text-white font-semibold py-3 rounded-xl text-sm transition-all flex items-center justify-center space-x-2">
                                <span id="next-btn-text">Next Question</span>
                                <i class="fa-solid fa-arrow-right text-xs"></i>
                            </button>
                        </div>
                    </div>

                    <div id="quiz-result-box" class="hidden text-center p-4 bg-slate-900/90 border border-emerald-500/30 rounded-xl space-y-3">
                        <h4 class="text-lg font-bold text-emerald-400"><i class="fa-solid fa-cloud-arrow-up mr-1"></i> Saved to Cloud Successfully! 🎉</h4>
                        <p class="text-sm text-slate-300">Your details have been securely saved and submitted to the cloud, SITANSHU:</p>
                        <div id="summary-details" class="bg-slate-800 p-3 rounded-lg text-left text-xs text-slate-300 space-y-1.5 border border-slate-700 max-h-48 overflow-y-auto">
                            <!-- User answers summary injected here -->
                        </div>
                        <div class="flex gap-2 pt-1">
                            <button onclick="openCloudLogsModal()" class="flex-1 bg-indigo-600 hover:bg-indigo-500 text-white font-semibold py-2.5 rounded-xl text-xs transition-all flex items-center justify-center space-x-1">
                                <i class="fa-solid fa-database"></i><span>View All Logs</span>
                            </button>
                            <button onclick="restartQuiz()" class="bg-slate-700 hover:bg-slate-600 text-white font-semibold px-4 py-2.5 rounded-xl text-xs transition-all">
                                Edit Answers
                            </button>
                        </div>
                    </div>
                </div>

                <div class="pt-2">
                    <button onclick="resetApp()" class="w-full bg-slate-700 hover:bg-slate-600 text-white font-semibold py-3 rounded-xl transition-all text-sm">
                        Verify Another Number
                    </button>
                </div>
            </div>

        </div>
    </div>

    <!-- Cloud Logs Viewer Modal -->
    <div id="cloud-logs-modal" class="fixed inset-0 bg-black/75 backdrop-blur-sm flex items-center justify-center p-4 hidden z-50">
        <div class="bg-slate-800 border border-slate-700 rounded-2xl max-w-md w-full p-6 shadow-2xl slide-up space-y-4">
            <div class="flex items-center justify-between border-b border-slate-700 pb-3">
                <h3 class="text-base font-bold text-white flex items-center">
                    <i class="fa-solid fa-cloud text-indigo-400 mr-2"></i> Cloud Submitted Logs
                </h3>
                <button onclick="closeCloudLogsModal()" class="text-slate-400 hover:text-white text-sm">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            <p class="text-xs text-slate-400">Below are all the personal details and answers stored in your cloud database records:</p>
            
            <div id="cloud-logs-container" class="bg-slate-900 border border-slate-700 rounded-xl p-3 max-h-72 overflow-y-auto space-y-3 text-xs text-slate-300">
                <!-- Dynamic logs injected here -->
            </div>

            <button onclick="closeCloudLogsModal()" class="w-full bg-indigo-600 hover:bg-indigo-500 text-white font-semibold py-2.5 rounded-xl text-xs transition-all">
                Close Viewer
            </button>
        </div>
    </div>

    <!-- Custom Modal Message Box -->
    <div id="modal-box" class="fixed inset-0 bg-black/70 backdrop-blur-sm flex items-center justify-center p-4 hidden z-50">
        <div class="bg-slate-800 border border-slate-700 rounded-2xl max-w-sm w-full p-6 text-center shadow-2xl slide-up">
            <div id="modal-icon" class="w-14 h-14 bg-rose-500/10 text-rose-500 rounded-full mx-auto flex items-center justify-center text-2xl mb-4">
                <i class="fa-solid fa-triangle-exclamation"></i>
            </div>
            <h3 id="modal-title" class="text-lg font-bold text-white mb-2">Notice</h3>
            <p id="modal-msg" class="text-sm text-slate-300 mb-6">Please fill in the required field.</p>
            <button onclick="closeModal()" class="w-full bg-indigo-600 hover:bg-indigo-500 text-white font-semibold py-2.5 rounded-xl transition-all">OK</button>
        </div>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, collection, addDoc, getDocs, query, orderBy } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        const appId = typeof __app_id !== 'undefined' ? __app_id : 'sitanshu-default-app';
        const firebaseConfig = JSON.parse(typeof __firebase_config !== 'undefined' ? __firebase_config : '{}');

        let app, db, auth, currentUser = null;

        if (Object.keys(firebaseConfig).length > 0) {
            app = initializeApp(firebaseConfig);
            db = getFirestore(app);
            auth = getAuth(app);

            const initialAuthToken = typeof __initial_auth_token !== 'undefined' ? __initial_auth_token : undefined;
            if (initialAuthToken) {
                signInWithCustomToken(auth, initialAuthToken).catch(() => signInAnonymously(auth));
            } else {
                signInAnonymously(auth);
            }

            onAuthStateChanged(auth, (user) => {
                currentUser = user;
            });
        }

        window.saveDetailsToCloudstore = async function(answersData) {
            // Also store in local storage as reliable backup for viewing anytime
            const allLogs = JSON.parse(localStorage.getItem('sitanshu_cloud_logs') || '[]');
            const newLog = {
                verifiedPhone: currentPhone,
                answers: answersData,
                timestamp: new Date().toLocaleString()
            };
            allLogs.unshift(newLog);
            localStorage.setItem('sitanshu_cloud_logs', JSON.stringify(allLogs));

            if (!db || !currentUser) return;
            try {
                const collectionRef = collection(db, 'artifacts', appId, 'users', currentUser.uid, 'profile_submissions');
                await addDoc(collectionRef, newLog);
            } catch (err) {
                console.error("Cloud save error:", err);
            }
        };

        window.fetchCloudLogs = async function() {
            let logs = [];
            // Retrieve from local storage backup first
            const localLogs = JSON.parse(localStorage.getItem('sitanshu_cloud_logs') || '[]');
            logs = [...localLogs];

            if (db && currentUser) {
                try {
                    const collectionRef = collection(db, 'artifacts', appId, 'users', currentUser.uid, 'profile_submissions');
                    const querySnapshot = await getDocs(collectionRef);
                    querySnapshot.forEach((doc) => {
                        const data = doc.data();
                        // avoid duplicate push if already present
                        if(!logs.some(l => l.timestamp === data.timestamp && l.verifiedPhone === data.verifiedPhone)) {
                            logs.push(data);
                        }
                    });
                } catch (err) {
                    console.log("Using local logs fallback:", err);
                }
            }
            return logs;
        };
    </script>

    <script>
        let currentPhone = "";
        let generatedOtp = "";
        let countdownTimer = null;

        // 6 Questions requiring short text answers
        const quizQuestions = [
            { question: "What is your full Name?", key: "Name", placeholder: "e.g., Sitanshu Kumar" },
            { question: "What is your Age?", key: "Age", placeholder: "e.g., 20" },
            { question: "What is your WhatsApp number?", key: "WhatsApp Number", placeholder: "e.g., 9876543210" },
            { question: "What is your Email address?", key: "Email", placeholder: "e.g., name@gmail.com" },
            { question: "Which State do you belong to?", key: "State", placeholder: "e.g., Bihar" },
            { question: "What is your Date of Birth (DOB)?", key: "Date of Birth", placeholder: "e.g., DD/MM/YYYY" }
        ];

        let currentQuestionIndex = 0;
        let userAnswers = {};

        // Custom Modal Alert Function
        function showAlert(title, message, isError = true) {
            document.getElementById('modal-title').innerText = title;
            document.getElementById('modal-msg').innerText = message;
            const iconDiv = document.getElementById('modal-icon');
            if(isError) {
                iconDiv.className = "w-14 h-14 bg-rose-500/10 text-rose-500 rounded-full mx-auto flex items-center justify-center text-2xl mb-4";
                iconDiv.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i>';
            } else {
                iconDiv.className = "w-14 h-14 bg-emerald-500/10 text-emerald-400 rounded-full mx-auto flex items-center justify-center text-2xl mb-4";
                iconDiv.innerHTML = '<i class="fa-solid fa-circle-check"></i>';
            }
            document.getElementById('modal-box').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('modal-box').classList.add('hi
