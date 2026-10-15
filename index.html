import React, { useState, useEffect, useRef } from 'react';

const customStyles = `
  @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800&display=swap');

  :root {
    --primary: #2563eb; /* Royal Blue */
    --primary-light: #60a5fa;
    --secondary: #7c3aed; /* Deep Violet */
    --bg-light: #f8fafc; /* Very Light Slate */
    --text-main: #0f172a;
    --text-muted: #475569;
    --glass-bg: rgba(255, 255, 255, 0.85);
    --glass-border: rgba(255, 255, 255, 0.5);
    --card-shadow: 0 10px 40px -10px rgba(0,0,0,0.08);
  }

  body {
    font-family: 'Cairo', sans-serif;
    background-color: var(--bg-light);
    color: var(--text-main);
    overflow-x: hidden;
    direction: rtl;
    margin: 0;
  }

  /* Animated Light Background */
  .bg-animated {
    background: radial-gradient(circle at top left, #e0f2fe, #f8fafc, #ede9fe);
    background-size: 400% 400%;
    animation: gradientBG 15s ease infinite;
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    z-index: -1;
  }

  @keyframes gradientBG {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  /* Light Glassmorphism */
  .glass-card {
    background: var(--glass-bg);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid var(--glass-border);
    box-shadow: var(--card-shadow);
    border-radius: 1.5rem;
  }

  .glass-input {
    background: rgba(255, 255, 255, 0.9);
    border: 1px solid #e2e8f0;
    color: var(--text-main);
    transition: all 0.3s ease;
    box-shadow: inset 0 2px 4px rgba(0,0,0,0.02);
  }
  .glass-input:focus {
    outline: none;
    border-color: var(--primary);
    box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.2);
    background: #ffffff;
  }

  /* Custom Scrollbar */
  ::-webkit-scrollbar { width: 8px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 10px; }
  ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }

  /* Animations */
  .fade-in { animation: fadeIn 0.8s cubic-bezier(0.4, 0, 0.2, 1) forwards; }
  .slide-up { animation: slideUp 0.6s cubic-bezier(0.4, 0, 0.2, 1) forwards; }
  .scale-in { animation: scaleIn 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards; }

  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  @keyframes slideUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  @keyframes scaleIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }

  .floating {
    animation: floating 4s ease-in-out infinite;
  }
  @keyframes floating {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-12px); }
    100% { transform: translateY(0px); }
  }
  
  .loader {
    border: 3px solid #e2e8f0;
    border-bottom-color: var(--primary);
    border-radius: 50%;
    display: inline-block;
    box-sizing: border-box;
    animation: rotation 1s linear infinite;
  }
  @keyframes rotation {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }

  /* Flashcard Flip Animations */
  .flip-card-inner {
    transition: transform 0.6s cubic-bezier(0.4, 0.2, 0.2, 1);
    transform-style: preserve-3d;
  }
  .flip-card.flipped .flip-card-inner {
    transform: rotateY(180deg);
  }
  .flip-card-front, .flip-card-back {
    backface-visibility: hidden;
    -webkit-backface-visibility: hidden;
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
  }
  .flip-card-back {
    transform: rotateY(180deg);
  }
`;

// Inject Styles
const styleSheet = document.createElement("style");
styleSheet.innerText = customStyles;
document.head.appendChild(styleSheet);

const API_KEY = "AQ.Ab8RN6IEJFRnbSIz-OwPXOsMLeyl9MyCUEZg7576ClzwlX55qA";

const Icons = {
  Brain: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" /></svg>,
  Book: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" /></svg>,
  Timer: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>,
  Folder: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" /></svg>,
  Send: () => <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8" /></svg>,
  Image: () => <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" /></svg>,
  Check: () => <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M5 13l4 4L19 7" /></svg>,
  User: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" /></svg>,
  Shield: () => <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" /></svg>,
  Cards: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 002-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" /></svg>,
  List: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01" /></svg>,
  Calculator: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 11h.01M12 11h.01M9 11h.01M7 21h10a2 2 0 002-2V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2z" /></svg>,
  Flask: () => <svg className="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z" /></svg>,
  Trash: () => <svg className="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" /></svg>
};

const callGemini = async (prompt, systemInstruction = "", imageDataBase64 = null, jsonMode = false) => {
  const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-3-flash-preview:generateContent?key=${API_KEY}`;
  
  // STRICT DOMAIN RESTRICTION TO SAVE API QUOTA
  const baseSystemPrompt = `
    أنت مساعد ذكي وطبيب خبير متواجد في منصة MedAI. 
    **قاعدة صارمة جداً:** يجب عليك رفض الإجابة على أي سؤال أو طلب خارج النطاق الطبي، أو الدراسي الجامعي، أو تطوير الذات للطلاب.
    إذا سألك المستخدم عن السياسة، الرياضة، الفن، البرمجة، الطبخ، أو أي موضوع غير متعلق بدراسة الطب، أجب بالصيغة التالية فقط:
    "عذراً دكتور، تمت برمجتي للإجابة على الأسئلة الطبية والدراسية فقط للحفاظ على الموارد والتركيز. يرجى طرح سؤال طبي."
    ${systemInstruction}
  `;

  let parts = [{ text: prompt }];
  if (imageDataBase64) {
    parts.push({
      inlineData: {
        mimeType: "image/jpeg",
        data: imageDataBase64.split(',')[1]
      }
    });
  }

  const payload = {
    contents: [{ role: "user", parts }],
    systemInstruction: { parts: [{ text: baseSystemPrompt }] },
  };

  if (jsonMode) {
    payload.generationConfig = { responseMimeType: "application/json" };
  }

  try {
    const response = await fetch(url, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(payload)
    });
    const data = await response.json();
    if (data.candidates && data.candidates.length > 0) {
      return data.candidates[0].content.parts[0].text;
    }
    throw new Error("Invalid response from AI");
  } catch (error) {
    console.error("Gemini Error:", error);
    return "عذراً، حدث خطأ في الاتصال بالذكاء الاصطناعي. يرجى المحاولة مرة أخرى.";
  }
};

const fileToBase64 = (file) => {
  return new Promise((resolve, reject) => {
    const reader = new FileReader();
    reader.readAsDataURL(file);
    reader.onload = () => resolve(reader.result);
    reader.onerror = error => reject(error);
  });
};

const LoginScreen = ({ onLogin }) => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    if(email && password) onLogin({ name: email.split('@')[0] });
  };

  return (
    <div className="min-h-screen flex flex-col items-center justify-center p-4 relative z-10 fade-in">
      <div className="glass-card p-10 w-full max-w-md relative overflow-hidden scale-in">
        {/* Soft Decorative Elements */}
        <div className="absolute -top-20 -right-20 w-56 h-56 bg-blue-100 rounded-full blur-3xl opacity-60"></div>
        <div className="absolute -bottom-20 -left-20 w-56 h-56 bg-purple-100 rounded-full blur-3xl opacity-60"></div>
        
        <div className="text-center mb-10 relative z-10">
          <div className="flex justify-center mb-6">
            <div className="w-24 h-24 bg-gradient-to-br from-blue-500 to-indigo-600 rounded-3xl flex items-center justify-center shadow-[0_10px_20px_rgba(37,99,235,0.3)] floating text-white">
               <Icons.Brain />
            </div>
          </div>
          <h1 className="text-4xl font-extrabold bg-clip-text text-transparent bg-gradient-to-r from-blue-700 to-purple-600 tracking-tight">
            MedAI Platform
          </h1>
          <p className="text-slate-500 mt-3 text-sm font-medium">المنصة الطبية الأذكى والأرقى لطلاب الطب</p>
        </div>

        <form onSubmit={handleSubmit} className="space-y-6 relative z-10">
          <div>
            <label className="block text-sm font-semibold text-slate-700 mb-2">البريد الجامعي</label>
            <input 
              type="email" 
              required
              className="w-full glass-input px-5 py-3.5 rounded-xl text-lg font-sans"
              placeholder="student@med.edu"
              value={email}
              onChange={(e) => setEmail(e.target.value)}
            />
          </div>
          <div>
            <label className="block text-sm font-semibold text-slate-700 mb-2">كلمة المرور</label>
            <input 
              type="password" 
              required
              className="w-full glass-input px-5 py-3.5 rounded-xl text-lg font-sans"
              placeholder="••••••••"
              value={password}
              onChange={(e) => setPassword(e.target.value)}
            />
          </div>
          <button 
            type="submit" 
            className="w-full py-4 mt-2 rounded-xl bg-gradient-to-r from-blue-600 to-indigo-600 text-white font-bold text-lg shadow-lg hover:shadow-blue-500/40 transition-all duration-300 transform hover:-translate-y-1"
          >
            تسجيل الدخول
          </button>
        </form>

        <div className="mt-10 text-center border-t border-slate-200 pt-5 relative z-10">
          <p className="text-sm text-slate-500 font-medium flex flex-col justify-center items-center gap-1">
            <span>تطوير وتصميم بكل فخامة بواسطة</span>
            <span className="font-extrabold text-blue-600 text-lg tracking-wide bg-blue-50 px-3 py-1 rounded-lg mt-1 border border-blue-100">
              يمان قدحات Yaman Gadhat
            </span>
          </p>
        </div>
      </div>
    </div>
  );
};

const OnboardingScreen = ({ user, onComplete }) => {
  const [step, setStep] = useState(1);
  const [year, setYear] = useState('');
  const [advice, setAdvice] = useState('');
  const [loadingAdvice, setLoadingAdvice] = useState(false);

  const handleYearSelect = async (selectedYear) => {
    setYear(selectedYear);
    setStep(2);
    setLoadingAdvice(true);
    
    const prompt = `طالب طب انضم للتو لمنصة دراسية وهو في السنة ${selectedYear}. أعطه نصيحتين ذهبيتين قصيرتين جداً تناسب مرحلته (أجب باللغة العربية بأسلوب راقي ومختصر جداً لتقليل استهلاك الـ API).`;
    const response = await callGemini(prompt);
    setAdvice(response);
    setLoadingAdvice(false);
  };

  const finishOnboarding = () => onComplete({ ...user, year });

  return (
    <div className="min-h-screen flex flex-col items-center justify-center p-4 relative z-10 fade-in">
      <div className="glass-card p-10 w-full max-w-2xl text-center slide-up">
        
        {step === 1 && (
          <div className="fade-in">
            <h2 className="text-3xl font-extrabold mb-4 text-slate-800">أهلاً بك يا دكتور <span className="text-blue-600">{user.name}</span> 👋</h2>
            <p className="text-slate-500 mb-8 text-lg">لتهيئة الذكاء الاصطناعي بدقة، في أي سنة دراسية أنت؟</p>
            
            <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
              {['سنة أولى (Basic)', 'سنة ثانية', 'سنة ثالثة (Pre-clinical)', 'سنة رابعة (Clinical)', 'سنة خامسة', 'سنة سادسة (امتياز)'].map((y, idx) => (
                <button 
                  key={idx}
                  onClick={() => handleYearSelect(y)}
                  className="p-4 rounded-2xl border-2 border-slate-100 text-slate-700 bg-white hover:border-blue-500 hover:bg-blue-50 transition-all font-bold text-lg shadow-sm hover:shadow-md transform hover:-translate-y-1"
                >
                  {y}
                </button>
              ))}
            </div>
          </div>
        )}

        {step === 2 && (
          <div className="fade-in">
             <div className="mb-8">
               <div className="inline-block p-4 rounded-full bg-blue-100 text-blue-600 mb-4 floating shadow-sm">
                  <Icons.Brain />
               </div>
               <h2 className="text-2xl font-bold text-slate-800">بناءً على ملفات درايف الدفعات السابقة..</h2>
             </div>

             {loadingAdvice ? (
               <div className="flex flex-col items-center justify-center py-10">
                 <div className="loader w-10 h-10 mb-4 border-slate-200 border-b-blue-600"></div>
                 <p className="text-slate-500 font-medium">نستخلص أهم النصائح لدفعتك...</p>
               </div>
             ) : (
               <div className="bg-slate-50 p-6 rounded-2xl border border-slate-200 text-right mb-8 leading-relaxed shadow-inner">
                 <p className="whitespace-pre-line text-lg text-slate-700 font-medium">{advice}</p>
               </div>
             )}

            <button 
              onClick={finishOnboarding}
              disabled={loadingAdvice}
              className="px-10 py-4 rounded-2xl bg-gradient-to-r from-blue-600 to-indigo-600 text-white font-bold text-lg hover:shadow-xl hover:shadow-blue-500/30 transition-all transform hover:-translate-y-1 disabled:opacity-50 disabled:transform-none"
            >
              ابدأ رحلتك الدراسية 🚀
            </button>
          </div>
        )}
      </div>
    </div>
  );
};

const AIChat = ({ user }) => {
  const [messages, setMessages] = useState([
    { role: 'model', text: `أهلاً بك دكتور ${user.name}. أنا متصل بملفات الـ Drive لدفعتك (${user.year}).\nتذكر: أنا مبرمج للإجابة على الأسئلة الطبية والدراسية فقط لضمان أعلى جودة وتقليل التشتت. كيف أساعدك؟` }
  ]);
  const [input, setInput] = useState('');
  const [loading, setLoading] = useState(false);
  const [imageFile, setImageFile] = useState(null);
  const [imageBase64, setImageBase64] = useState(null);
  const chatEndRef = useRef(null);

  const scrollToBottom = () => chatEndRef.current?.scrollIntoView({ behavior: "smooth" });
  useEffect(scrollToBottom, [messages]);

  const handleImageUpload = async (e) => {
    const file = e.target.files[0];
    if (file) {
      setImageFile(file);
      const base64 = await fileToBase64(file);
      setImageBase64(base64);
    }
  };

  const handleSend = async () => {
    if (!input.trim() && !imageBase64) return;

    const userMsg = { role: 'user', text: input, image: imageBase64 };
    setMessages(prev => [...prev, userMsg]);
    setInput('');
    setImageFile(null);
    setImageBase64(null);
    setLoading(true);

    const specificInstruction = `الطالب في السنة ${user.year}. استخدم المصطلحات الطبية الإنجليزية في الشرح العربي. إذا أرسل صورة لشريحة اشرحها للامتحان.`;

    const aiResponse = await callGemini(userMsg.text || "اشرح هذه الصورة الطبية", specificInstruction, userMsg.image);
    
    setMessages(prev => [...prev, { role: 'model', text: aiResponse }]);
    setLoading(false);
  };

  return (
    <div className="flex flex-col h-[calc(100vh-100px)] glass-card slide-up overflow-hidden shadow-sm border border-slate-200">
      <div className="bg-white/80 backdrop-blur-md border-b border-slate-200 p-5 flex justify-between items-center shadow-sm z-10">
        <div>
          <h2 className="text-xl font-extrabold text-blue-700 flex items-center gap-2">
            <Icons.Brain /> MedAI Tutor
          </h2>
          <p className="text-xs text-slate-500 font-bold mt-1 flex items-center gap-1">
             <Icons.Shield /> حماية النطاق مفعلة (طبي فقط)
          </p>
        </div>
        <div className="flex gap-2">
           <button onClick={() => setInput('لخّص لي أهم نقاط محاضرة الـ Anatomy الأخيرة')} className="text-sm bg-blue-50 text-blue-700 hover:bg-blue-100 border border-blue-200 px-4 py-2 rounded-xl transition font-semibold">ملخص سريع</button>
           <button onClick={() => setInput('اشرح لي هذا المفهوم كأنني طالب سنة أولى')} className="text-sm bg-indigo-50 text-indigo-700 hover:bg-indigo-100 border border-indigo-200 px-4 py-2 rounded-xl transition font-semibold">تبسيط المفهوم</button>
        </div>
      </div>

      <div className="flex-1 overflow-y-auto p-6 space-y-6 bg-slate-50/50">
        {messages.map((msg, idx) => (
          <div key={idx} className={`flex ${msg.role === 'user' ? 'justify-start' : 'justify-end'} scale-in`} style={{animationDelay: '0.1s'}}>
            <div className={`max-w-[80%] p-5 rounded-2xl shadow-sm text-lg ${
              msg.role === 'user' 
                ? 'bg-blue-600 text-white rounded-tr-none' 
                : 'bg-white text-slate-700 rounded-tl-none border border-slate-200 shadow-[0_5px_15px_rgba(0,0,0,0.05)]'
            }`}>
              {msg.image && <img src={msg.image} alt="uploaded" className="max-w-full h-auto rounded-xl mb-4 border border-slate-200 shadow-sm" />}
              <p className="whitespace-pre-wrap leading-relaxed font-medium">{msg.text}</p>
            </div>
          </div>
        ))}
        {loading && (
          <div className="flex justify-end fade-in">
            <div className="bg-white text-slate-500 p-4 rounded-2xl rounded-tl-none border border-slate-200 flex items-center gap-3 shadow-sm">
              <div className="loader w-5 h-5 border-slate-200 border-b-blue-600"></div>
              <span className="text-sm font-bold">MedAI يحلل الداتا...</span>
            </div>
          </div>
        )}
        <div ref={chatEndRef} />
      </div>

      <div className="p-4 border-t border-slate-200 bg-white/80 backdrop-blur-md">
        {imageFile && (
           <div className="mb-3 flex items-center gap-2 text-sm text-blue-700 bg-blue-50 border border-blue-100 w-fit px-4 py-2 rounded-xl shadow-sm">
             <Icons.Check /> تم إرفاق: {imageFile.name}
             <button onClick={() => {setImageFile(null); setImageBase64(null)}} className="ml-3 text-red-500 hover:bg-red-50 rounded-full p-1 transition">✕</button>
           </div>
        )}
        <div className="flex items-center gap-3">
          <label className="p-4 bg-slate-100 rounded-2xl cursor-pointer hover:bg-slate-200 transition-all text-slate-500 shadow-inner">
            <Icons.Image />
            <input type="file" accept="image/*" className="hidden" onChange={handleImageUpload} />
          </label>
          <input 
            type="text" 
            value={input}
            onChange={(e) => setInput(e.target.value)}
            onKeyPress={(e) => e.key === 'Enter' && handleSend()}
            placeholder="اسأل MedAI أو اطلب تلخيصاً طبياً..."
            className="flex-1 glass-input px-5 py-4 rounded-2xl text-lg shadow-sm"
          />
          <button 
            onClick={handleSend}
            disabled={loading || (!input.trim() && !imageBase64)}
            className="p-4 bg-blue-600 rounded-2xl hover:bg-blue-700 transition-all text-white shadow-md disabled:opacity-50 disabled:transform-none transform hover:-translate-y-1 flex items-center justify-center"
          >
            <Icons.Send />
          </button>
        </div>
      </div>
    </div>
  );
};

const QuizGenerator = () => {
  const [topic, setTopic] = useState('');
  const [loading, setLoading] = useState(false);
  const [quiz, setQuiz] = useState(null);
  const [userAnswers, setUserAnswers] = useState({});
  const [showResults, setShowResults] = useState(false);

  const generateQuiz = async () => {
    if (!topic.trim()) return;
    setLoading(true);
    setQuiz(null);
    setUserAnswers({});
    setShowResults(false);

    // Prompt optimized to restrict context and demand JSON only
    const prompt = `أنت بروفيسور طبي. إنشاء 3 أسئلة خيارات متعددة (MCQ) باللغة الإنجليزية حول موضوع طبي: "${topic}". 
    إذا كان الموضوع غير طبي، قم بإرجاع مصفوفة فارغة [].
    قم بإرجاع الرد بصيغة JSON حصراً:
    [{"question": "Q?", "options": ["A", "B", "C", "D"], "correctAnswerIndex": 0, "explanation": "Explanation in Arabic"}]`;

    const response = await callGemini(prompt, "", null, true);
    try {
      const cleanedJson = response.replace(/```json/g, '').replace(/```/g, '').trim();
      const parsedQuiz = JSON.parse(cleanedJson);
      if (parsedQuiz.length === 0) {
        alert("الموضوع المدخل غير طبي أو خارج النطاق. يرجى إدخال موضوع طبي.");
      } else {
        setQuiz(parsedQuiz);
      }
    } catch (e) {
      console.error("JSON Error:", e);
      alert("حدث خطأ، تأكد من كتابة موضوع طبي واضح.");
    }
    setLoading(false);
  };

  const calculateScore = () => {
    let score = 0;
    quiz.forEach((q, idx) => { if (userAnswers[idx] === q.correctAnswerIndex) score++; });
    return score;
  };

  return (
    <div className="glass-card p-8 min-h-[calc(100vh-100px)] slide-up border border-slate-200">
      <div className="mb-10 text-center">
        <h2 className="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-700 to-indigo-600 mb-3">اختبر معلوماتك بدقة AI</h2>
        <p className="text-slate-500 font-medium">تدرب على أسئلة نمط USMLE مصممة خصيصاً لك.</p>
      </div>

      <div className="flex gap-3 max-w-2xl mx-auto mb-10 bg-white p-2 rounded-2xl shadow-sm border border-slate-100">
        <input 
          type="text" 
          placeholder="مثال: Myocardial Infarction, Kreb's Cycle..." 
          className="flex-1 bg-transparent px-4 py-3 rounded-xl focus:outline-none text-slate-800 font-sans text-lg dir-ltr"
          value={topic}
          onChange={(e) => setTopic(e.target.value)}
        />
        <button 
          onClick={generateQuiz}
          disabled={loading || !topic}
          className="px-8 py-3 bg-indigo-600 rounded-xl font-bold text-white hover:bg-indigo-700 transition-all flex items-center gap-2 shadow-md disabled:opacity-50"
        >
          {loading ? <div className="loader w-5 h-5 border-2 border-indigo-200 border-b-white"></div> : <Icons.Book />}
          توليد
        </button>
      </div>

      {quiz && (
        <div className="max-w-3xl mx-auto space-y-8 fade-in">
          {quiz.map((q, qIndex) => (
            <div key={qIndex} className="bg-white p-8 rounded-3xl border border-slate-200 shadow-sm hover:shadow-md transition-shadow">
              <h3 className="text-xl font-bold mb-6 font-sans text-left dir-ltr text-slate-800">{qIndex + 1}. {q.question}</h3>
              <div className="space-y-3 font-sans dir-ltr text-left">
                {q.options.map((opt, optIndex) => {
                  let btnClass = "w-full text-left p-4 rounded-xl border-2 transition-all font-medium text-lg ";
                  
                  if (showResults) {
                    if (optIndex === q.correctAnswerIndex) btnClass += "bg-green-50 border-green-500 text-green-800";
                    else if (userAnswers[qIndex] === optIndex) btnClass += "bg-red-50 border-red-500 text-red-800";
                    else btnClass += "bg-slate-50 border-slate-200 text-slate-400";
                  } else {
                    if (userAnswers[qIndex] === optIndex) btnClass += "bg-blue-50 border-blue-500 text-blue-800";
                    else btnClass += "bg-white border-slate-200 hover:border-blue-300 text-slate-700 hover:bg-slate-50";
                  }

                  return (
                    <button key={optIndex} onClick={() => !showResults && setUserAnswers(prev => ({ ...prev, [qIndex]: optIndex }))} className={btnClass}>
                      {opt}
                    </button>
                  );
                })}
              </div>
              
              {showResults && (
                <div className="mt-6 p-5 bg-blue-50 border border-blue-100 rounded-xl text-blue-800 text-sm leading-relaxed">
                  <strong className="text-blue-900 block mb-1 font-extrabold">توضيح الذكاء الاصطناعي:</strong> {q.explanation}
                </div>
              )}
            </div>
          ))}

          {!showResults ? (
            <button 
              onClick={() => setShowResults(true)}
              className="w-full py-5 bg-gradient-to-r from-green-500 to-emerald-600 rounded-2xl font-bold text-xl text-white shadow-lg hover:shadow-green-500/30 transition-all transform hover:-translate-y-1"
            >
              عرض النتيجة وتقييم الإجابات
            </button>
          ) : (
            <div className="text-center p-10 bg-white rounded-3xl border-2 border-green-500 shadow-xl shadow-green-100 scale-in">
              <h3 className="text-4xl font-extrabold mb-3 text-slate-800">النتيجة: <span className="text-green-600">{calculateScore()} / {quiz.length}</span></h3>
              <p className="text-slate-600 text-xl font-medium">
                {calculateScore() === quiz.length ? 'ممتاز دكتور! جاهز للامتحان 🥇' : 'استمر بالدراسة والتدريب! 💪'}
              </p>
            </div>
          )}
        </div>
      )}
    </div>
  );
};

const FocusTimer = () => {
  const [timeLeft, setTimeLeft] = useState(25 * 60);
  const [isActive, setIsActive] = useState(false);
  const [mode, setMode] = useState('focus');

  useEffect(() => {
    let interval = null;
    if (isActive && timeLeft > 0) {
      interval = setInterval(() => setTimeLeft(t => t - 1), 1000);
    } else if (timeLeft === 0 && isActive) {
      setIsActive(false);
      const audio = new Audio('https://assets.mixkit.co/active_storage/sfx/2869/2869-preview.mp3');
      audio.play().catch(e => console.log("Audio play prevented"));
    }
    return () => clearInterval(interval);
  }, [isActive, timeLeft]);

  const toggleTimer = () => setIsActive(!isActive);
  const resetTimer = (newMode = 'focus') => {
    setIsActive(false);
    setMode(newMode);
    setTimeLeft(newMode === 'focus' ? 25 * 60 : 5 * 60);
  };

  const minutes = Math.floor(timeLeft / 60);
  const seconds = timeLeft % 60;
  const progress = mode === 'focus' ? ((25*60 - timeLeft) / (25*60)) * 100 : ((5*60 - timeLeft) / (5*60)) * 100;

  return (
    <div className="flex items-center justify-center h-[calc(100vh-100px)] slide-up">
      <div className="bg-white p-12 rounded-3xl shadow-[0_20px_50px_-12px_rgba(0,0,0,0.1)] border border-slate-100 text-center relative overflow-hidden max-w-md w-full">
        <div className={`absolute inset-0 bg-gradient-to-b ${mode==='focus'?'from-rose-50 to-transparent':'from-emerald-50 to-transparent'} transition-colors duration-1000`}></div>
        
        <div className="relative z-10">
          <Icons.Timer className="w-14 h-14 mx-auto text-slate-300 mb-6" />
          <h2 className="text-3xl font-extrabold mb-3 text-slate-800">وضع الانعزال والتركيز</h2>
          <p className="text-slate-500 text-sm mb-10 font-medium">أغلق المشتتات.. وركز في بناء مستقبلك.</p>

          <div className="flex justify-center gap-4 mb-10 bg-slate-50 p-2 rounded-2xl border border-slate-100">
            <button onClick={() => resetTimer('focus')} className={`px-6 py-3 rounded-xl text-sm font-bold transition-all ${mode === 'focus' ? 'bg-white text-rose-600 shadow-sm border border-slate-200' : 'text-slate-500 hover:bg-slate-100'}`}>
              دراسة (25 د)
            </button>
            <button onClick={() => resetTimer('break')} className={`px-6 py-3 rounded-xl text-sm font-bold transition-all ${mode === 'break' ? 'bg-white text-emerald-600 shadow-sm border border-slate-200' : 'text-slate-500 hover:bg-slate-100'}`}>
              استراحة (5 د)
            </button>
          </div>

          <div className="relative w-64 h-64 mx-auto mb-10 flex items-center justify-center">
            <svg className="absolute inset-0 w-full h-full transform -rotate-90 drop-shadow-md">
              <circle cx="128" cy="128" r="116" stroke="currentColor" strokeWidth="8" fill="transparent" className="text-slate-100" />
              <circle 
                cx="128" cy="128" r="116" 
                stroke="currentColor" strokeWidth="8" fill="transparent" 
                strokeDasharray="728.8" strokeDashoffset={728.8 - (728.8 * progress) / 100}
                className={`transition-all duration-1000 ${mode==='focus' ? 'text-rose-500' : 'text-emerald-500'}`}
                strokeLinecap="round"
              />
            </svg>
            <div className="text-7xl font-black font-sans dir-ltr tracking-tighter text-slate-800">
              {minutes.toString().padStart(2, '0')}:{seconds.toString().padStart(2, '0')}
            </div>
          </div>

          <button 
            onClick={toggleTimer}
            className={`w-full py-5 rounded-2xl font-black text-xl transition-all shadow-lg transform hover:-translate-y-1 ${isActive ? 'bg-slate-100 text-slate-700 hover:bg-slate-200 border border-slate-200 shadow-none' : (mode === 'focus' ? 'bg-rose-500 hover:bg-rose-600 text-white shadow-rose-500/30' : 'bg-emerald-500 hover:bg-emerald-600 text-white shadow-emerald-500/30')}`}
          >
            {isActive ? 'إيقاف مؤقت' : 'ابدأ التركيز 🚀'}
          </button>
        </div>
      </div>
    </div>
  );
};

const DriveFiles = ({ user }) => {
  const folders = [
    { name: 'Anatomy', arabic: 'علم التشريح', count: 24, color: 'text-rose-600', bg: 'bg-rose-50', border: 'border-rose-100' },
    { name: 'Physiology', arabic: 'وظائف الأعضاء', count: 18, color: 'text-blue-600', bg: 'bg-blue-50', border: 'border-blue-100' },
    { name: 'Biochemistry', arabic: 'الكيمياء الحيوية', count: 15, color: 'text-amber-600', bg: 'bg-amber-50', border: 'border-amber-100' },
    { name: 'Pathology', arabic: 'علم الأمراض', count: 30, color: 'text-purple-600', bg: 'bg-purple-50', border: 'border-purple-100' },
    { name: 'Pharmacology', arabic: 'علم الأدوية', count: 22, color: 'text-emerald-600', bg: 'bg-emerald-50', border: 'border-emerald-100' },
    { name: 'Past Papers', arabic: 'أسئلة سنوات', count: 50, color: 'text-slate-600', bg: 'bg-slate-100', border: 'border-slate-200' },
  ];

  return (
    <div className="p-8 slide-up bg-white rounded-3xl border border-slate-200 shadow-sm min-h-[calc(100vh-100px)]">
      <div className="flex flex-col md:flex-row justify-between items-start md:items-end mb-10 border-b border-slate-100 pb-6 gap-4">
        <div>
          <h2 className="text-3xl font-extrabold text-slate-800 mb-3">مكتبة الدفعات (Drive)</h2>
          <p className="text-slate-500 font-medium text-lg">مصادر {user.year} منظمة ومربوطة بالذكاء الاصطناعي لسهولة الاسترجاع.</p>
        </div>
        <div className="bg-blue-50 text-blue-700 px-5 py-3 rounded-xl text-sm font-bold flex items-center gap-2 border border-blue-100 shadow-sm">
          <Icons.Shield /> متصل وحصري للنطاق الطبي
        </div>
      </div>

      <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        {folders.map((folder, idx) => (
          <div key={idx} className={`${folder.bg} ${folder.border} border p-6 rounded-3xl cursor-pointer hover:-translate-y-2 transition-all duration-300 group shadow-sm hover:shadow-md relative overflow-hidden`}>
            <div className="bg-white w-14 h-14 rounded-2xl flex items-center justify-center mb-5 shadow-sm">
              <Icons.Folder className={`w-8 h-8 ${folder.color}`} />
            </div>
            <h3 className={`text-xl font-extrabold mb-1 ${folder.color} font-sans dir-ltr text-left`}>{folder.name}</h3>
            <p className="text-slate-600 font-bold mb-3">{folder.arabic}</p>
            <p className="text-slate-500 text-sm font-medium">{folder.count} ملفات • محدث</p>
            <div className="mt-5 pt-5 border-t border-black/5 flex justify-end opacity-0 group-hover:opacity-100 transition-opacity">
              <span className="text-xs bg-white px-3 py-1.5 rounded-lg shadow-sm font-bold text-slate-700">اطلب الشرح من AI →</span>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
};

const Flashcards = () => {
  const [topic, setTopic] = useState('');
  const [loading, setLoading] = useState(false);
  const [cards, setCards] = useState([]);
  const [flippedIndex, setFlippedIndex] = useState(null);

  const generateFlashcards = async () => {
    if (!topic.trim()) return;
    setLoading(true);
    setCards([]);
    setFlippedIndex(null);

    const prompt = `أنت بروفيسور طبي. قم بإنشاء 5 بطاقات ذاكرة (Flashcards) لمراجعة سريعة حول الموضوع الطبي: "${topic}".
    يجب أن تحتوي كل بطاقة على مصطلح أو سؤال قصير في الجهة الأمامية (front) وتعريف أو إجابة دقيقة في الجهة الخلفية (back) باللغة الإنجليزية مع ترجمة عربية بسيطة.
    إذا كان الموضوع غير طبي، قم بإرجاع مصفوفة فارغة [].
    قم بإرجاع الرد بصيغة JSON حصراً:
    [{"front": "Term/Question", "back": "Definition/Answer"}]`;

    const response = await callGemini(prompt, "", null, true);
    try {
      const cleanedJson = response.replace(/```json/g, '').replace(/```/g, '').trim();
      const parsedCards = JSON.parse(cleanedJson);
      if (parsedCards.length === 0) {
        alert("الموضوع المدخل غير طبي أو خارج النطاق.");
      } else {
        setCards(parsedCards);
      }
    } catch (e) {
      console.error("JSON Error:", e);
      alert("حدث خطأ في التوليد.");
    }
    setLoading(false);
  };

  return (
    <div className="glass-card p-8 min-h-[calc(100vh-100px)] slide-up border border-slate-200">
      <div className="mb-10 text-center">
        <h2 className="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-700 to-indigo-600 mb-3">بطاقات الذاكرة (Flashcards)</h2>
        <p className="text-slate-500 font-medium">ولد بطاقات ذكية للحفظ والمراجعة السريعة باستخدام الذكاء الاصطناعي.</p>
      </div>

      <div className="flex gap-3 max-w-2xl mx-auto mb-10 bg-white p-2 rounded-2xl shadow-sm border border-slate-100">
        <input 
          type="text" 
          placeholder="مثال: Cranial Nerves, Penicillin..." 
          className="flex-1 bg-transparent px-4 py-3 rounded-xl focus:outline-none text-slate-800 font-sans text-lg dir-ltr"
          value={topic}
          onChange={(e) => setTopic(e.target.value)}
        />
        <button 
          onClick={generateFlashcards}
          disabled={loading || !topic}
          className="px-8 py-3 bg-indigo-600 rounded-xl font-bold text-white hover:bg-indigo-700 transition-all flex items-center gap-2 shadow-md disabled:opacity-50"
        >
          {loading ? <div className="loader w-5 h-5 border-2 border-indigo-200 border-b-white"></div> : <Icons.Cards />}
          توليد البطاقات
        </button>
      </div>

      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 fade-in perspective-1000">
        {cards.map((card, idx) => (
          <div 
            key={idx} 
            className={`flip-card w-full h-64 cursor-pointer relative ${flippedIndex === idx ? 'flipped' : ''}`}
            onClick={() => setFlippedIndex(flippedIndex === idx ? null : idx)}
          >
            <div className="flip-card-inner w-full h-full relative">
              {/* Front */}
              <div className="flip-card-front bg-white border-2 border-blue-100 rounded-3xl p-6 flex items-center justify-center text-center shadow-md hover:border-blue-300 transition-colors">
                <div>
                  <span className="text-xs font-bold text-blue-500 uppercase tracking-widest mb-3 block">Tap to Flip</span>
                  <h3 className="text-2xl font-bold text-slate-800 font-sans">{card.front}</h3>
                </div>
              </div>
              {/* Back */}
              <div className="flip-card-back bg-gradient-to-br from-blue-600 to-indigo-700 rounded-3xl p-6 flex items-center justify-center text-center shadow-lg text-white">
                <p className="text-lg font-medium leading-relaxed font-sans">{card.back}</p>
              </div>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
};

const StudyPlanner = () => {
  const [tasks, setTasks] = useState([
    { id: 1, text: 'مراجعة محاضرة Anatomy رقم 5', completed: false },
    { id: 2, text: 'حل 20 سؤال UWorld', completed: true },
  ]);
  const [newTask, setNewTask] = useState('');

  const addTask = (e) => {
    e.preventDefault();
    if (!newTask.trim()) return;
    setTasks([...tasks, { id: Date.now(), text: newTask, completed: false }]);
    setNewTask('');
  };

  const toggleTask = (id) => {
    setTasks(tasks.map(t => t.id === id ? { ...t, completed: !t.completed } : t));
  };

  const deleteTask = (id) => {
    setTasks(tasks.filter(t => t.id !== id));
  };

  return (
    <div className="glass-card p-8 min-h-[calc(100vh-100px)] slide-up border border-slate-200 max-w-4xl mx-auto">
      <div className="mb-10 text-center">
        <h2 className="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-700 to-indigo-600 mb-3 flex items-center justify-center gap-3">
          <Icons.List /> خطة الدراسة والمهام
        </h2>
        <p className="text-slate-500 font-medium">نظم وقتك ومحاضراتك بدقة (لا يستهلك رصيد الذكاء الاصطناعي).</p>
      </div>

      <form onSubmit={addTask} className="flex gap-3 mb-8 bg-white p-2 rounded-2xl shadow-sm border border-slate-100">
        <input 
          type="text" 
          placeholder="أضف مهمة دراسية جديدة..." 
          className="flex-1 bg-transparent px-4 py-3 rounded-xl focus:outline-none text-slate-800 text-lg"
          value={newTask}
          onChange={(e) => setNewTask(e.target.value)}
        />
        <button type="submit" className="px-8 py-3 bg-blue-600 rounded-xl font-bold text-white hover:bg-blue-700 transition-all shadow-md">
          إضافة
        </button>
      </form>

      <div className="space-y-3">
        {tasks.map(task => (
          <div key={task.id} className={`flex items-center justify-between p-4 rounded-2xl border transition-all ${task.completed ? 'bg-slate-50 border-slate-200' : 'bg-white border-blue-100 shadow-sm hover:shadow-md'}`}>
            <div className="flex items-center gap-4 cursor-pointer flex-1" onClick={() => toggleTask(task.id)}>
              <div className={`w-6 h-6 rounded-full border-2 flex items-center justify-center transition-colors ${task.completed ? 'bg-green-500 border-green-500 text-white' : 'border-slate-300'}`}>
                {task.completed && <Icons.Check />}
              </div>
              <span className={`text-lg font-medium transition-all ${task.completed ? 'text-slate-400 line-through' : 'text-slate-800'}`}>
                {task.text}
              </span>
            </div>
            <button onClick={() => deleteTask(task.id)} className="text-red-400 hover:bg-red-50 p-2 rounded-xl transition-colors">
              <Icons.Trash />
            </button>
          </div>
        ))}
        {tasks.length === 0 && (
          <div className="text-center py-10 text-slate-400 font-medium">
            لا توجد مهام حالياً. استمتع بوقتك أو أضف محاضرة جديدة!
          </div>
        )}
      </div>
    </div>
  );
};

const MedicalCalculators = () => {
  const [calcType, setCalcType] = useState('bmi');
  const [inputs, setInputs] = useState({ weight: '', height: '', sbp: '', dbp: '' });

  const calculateBMI = () => {
    const w = parseFloat(inputs.weight);
    const h = parseFloat(inputs.height) / 100;
    if (w && h) return (w / (h * h)).toFixed(1);
    return '-';
  };

  const calculateMAP = () => {
    const s = parseFloat(inputs.sbp);
    const d = parseFloat(inputs.dbp);
    if (s && d) return ((s + (2 * d)) / 3).toFixed(1);
    return '-';
  };

  return (
    <div className="glass-card p-8 min-h-[calc(100vh-100px)] slide-up border border-slate-200 max-w-4xl mx-auto">
      <div className="mb-8 text-center">
        <h2 className="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-700 to-indigo-600 mb-3 flex items-center justify-center gap-3">
          <Icons.Calculator /> حاسبات طبية سريعة
        </h2>
        <p className="text-slate-500 font-medium">أدوات إكلينيكية مفيدة للحساب السريع (لا تستهلك إنترنت).</p>
      </div>

      <div className="flex justify-center gap-4 mb-8">
        <button onClick={() => setCalcType('bmi')} className={`px-6 py-2 rounded-xl font-bold transition-all ${calcType === 'bmi' ? 'bg-blue-600 text-white shadow-md' : 'bg-slate-100 text-slate-600 hover:bg-slate-200'}`}>BMI (مؤشر كتلة الجسم)</button>
        <button onClick={() => setCalcType('map')} className={`px-6 py-2 rounded-xl font-bold transition-all ${calcType === 'map' ? 'bg-blue-600 text-white shadow-md' : 'bg-slate-100 text-slate-600 hover:bg-slate-200'}`}>MAP (متوسط الضغط)</button>
      </div>

      <div className="bg-white p-8 rounded-3xl border border-slate-100 shadow-sm">
        {calcType === 'bmi' && (
          <div className="fade-in space-y-6">
            <div className="grid grid-cols-2 gap-6">
              <div>
                <label className="block text-sm font-bold text-slate-700 mb-2">الوزن (kg)</label>
                <input type="number" className="w-full glass-input px-4 py-3 rounded-xl text-xl dir-ltr text-center font-sans" placeholder="70" value={inputs.weight} onChange={e => setInputs({...inputs, weight: e.target.value})} />
              </div>
              <div>
                <label className="block text-sm font-bold text-slate-700 mb-2">الطول (cm)</label>
                <input type="number" className="w-full glass-input px-4 py-3 rounded-xl text-xl dir-ltr text-center font-sans" placeholder="175" value={inputs.height} onChange={e => setInputs({...inputs, height: e.target.value})} />
              </div>
            </div>
            <div className="p-6 bg-blue-50 border border-blue-100 rounded-2xl text-center">
              <span className="block text-slate-500 mb-2 font-bold">النتيجة (BMI)</span>
              <span className="text-5xl font-black text-blue-700 font-sans">{calculateBMI()}</span>
            </div>
          </div>
        )}

        {calcType === 'map' && (
          <div className="fade-in space-y-6">
            <div className="grid grid-cols-2 gap-6">
              <div>
                <label className="block text-sm font-bold text-slate-700 mb-2">الضغط الانقباضي Systolic (mmHg)</label>
                <input type="number" className="w-full glass-input px-4 py-3 rounded-xl text-xl dir-ltr text-center font-sans" placeholder="120" value={inputs.sbp} onChange={e => setInputs({...inputs, sbp: e.target.value})} />
              </div>
              <div>
                <label className="block text-sm font-bold text-slate-700 mb-2">الضغط الانبساطي Diastolic (mmHg)</label>
                <input type="number" className="w-full glass-input px-4 py-3 rounded-xl text-xl dir-ltr text-center font-sans" placeholder="80" value={inputs.dbp} onChange={e => setInputs({...inputs, dbp: e.target.value})} />
              </div>
            </div>
            <div className="p-6 bg-emerald-50 border border-emerald-100 rounded-2xl text-center">
              <span className="block text-slate-500 mb-2 font-bold">النتيجة (MAP)</span>
              <span className="text-5xl font-black text-emerald-600 font-sans">{calculateMAP()}</span>
              <span className="text-sm font-bold text-emerald-800 ml-2">mmHg</span>
            </div>
          </div>
        )}
      </div>
    </div>
  );
};

const LabValues = () => {
  const labs = [
    { name: "Hemoglobin (Hb) - Male", value: "13.5 - 17.5 g/dL", color: "text-red-600", bg: "bg-red-50" },
    { name: "Hemoglobin (Hb) - Female", value: "12.0 - 15.5 g/dL", color: "text-red-600", bg: "bg-red-50" },
    { name: "White Blood Cells (WBC)", value: "4,500 - 11,000 /mcL", color: "text-slate-600", bg: "bg-slate-100" },
    { name: "Platelets", value: "150,000 - 450,000 /mcL", color: "text-amber-600", bg: "bg-amber-50" },
    { name: "Sodium (Na)", value: "135 - 145 mEq/L", color: "text-blue-600", bg: "bg-blue-50" },
    { name: "Potassium (K)", value: "3.5 - 5.0 mEq/L", color: "text-blue-600", bg: "bg-blue-50" },
    { name: "Creatinine", value: "0.6 - 1.2 mg/dL", color: "text-purple-600", bg: "bg-purple-50" },
    { name: "Fasting Glucose", value: "70 - 99 mg/dL", color: "text-emerald-600", bg: "bg-emerald-50" },
  ];

  return (
    <div className="glass-card p-8 min-h-[calc(100vh-100px)] slide-up border border-slate-200">
      <div className="mb-10 text-center">
        <h2 className="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-700 to-indigo-600 mb-3 flex items-center justify-center gap-3">
          <Icons.Flask /> مرجع القيم المخبرية
        </h2>
        <p className="text-slate-500 font-medium">قيم مختبرية شائعة للرجوع السريع في الكلينيكال.</p>
      </div>

      <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
        {labs.map((lab, idx) => (
          <div key={idx} className={`p-5 rounded-2xl border ${lab.bg} border-white/50 shadow-sm flex justify-between items-center transition-transform hover:-translate-y-1`}>
            <span className="font-bold text-slate-700 font-sans text-lg">{lab.name}</span>
            <span className={`font-black font-sans text-lg ${lab.color}`}>{lab.value}</span>
          </div>
        ))}
      </div>
    </div>
  );
};

const MainApp = ({ user }) => {
  const [activeTab, setActiveTab] = useState('chat');

  const navItems = [
    { id: 'chat', label: 'المساعد الذكي AI', icon: <Icons.Brain /> },
    { id: 'quiz', label: 'اختبارات التدريب', icon: <Icons.Book /> },
    { id: 'flashcards', label: 'بطاقات الذاكرة', icon: <Icons.Cards /> },
    { id: 'planner', label: 'خطة الدراسة', icon: <Icons.List /> },
    { id: 'calculators', label: 'حاسبات طبية', icon: <Icons.Calculator /> },
    { id: 'labs', label: 'القيم المخبرية', icon: <Icons.Flask /> },
    { id: 'drive', label: 'ملفات الدفعة', icon: <Icons.Folder /> },
    { id: 'focus', label: 'وضع التركيز', icon: <Icons.Timer /> },
  ];

  return (
    <div className="flex h-screen overflow-hidden relative z-10 bg-slate-50">
      {/* Sidebar */}
      <aside className="w-72 bg-white border-l border-slate-200 flex flex-col z-20 shadow-[5px_0_15px_rgba(0,0,0,0.02)] overflow-y-auto">
        <div className="p-8 border-b border-slate-100 text-center shrink-0">
          <div className="w-20 h-20 bg-blue-50 text-blue-600 rounded-3xl mx-auto mb-4 flex items-center justify-center shadow-inner border border-blue-100">
             <Icons.User />
          </div>
          <h2 className="text-2xl font-extrabold text-slate-800">{user.name}</h2>
          <p className="text-sm text-blue-600 font-bold mt-2 bg-blue-50 inline-block px-3 py-1 rounded-lg border border-blue-100">{user.year}</p>
        </div>
        
        <nav className="flex-1 p-5 space-y-2">
          {navItems.map(item => (
            <button
              key={item.id}
              onClick={() => setActiveTab(item.id)}
              className={`w-full flex items-center gap-4 px-4 py-3.5 rounded-2xl transition-all font-bold text-base ${
                activeTab === item.id 
                  ? 'bg-blue-600 text-white shadow-lg shadow-blue-500/30 transform scale-[1.02]' 
                  : 'text-slate-500 hover:bg-slate-50 hover:text-blue-600 border border-transparent hover:border-slate-200'
              }`}
            >
              <div className={activeTab === item.id ? 'animate-pulse' : ''}>{item.icon}</div>
              {item.label}
            </button>
          ))}
        </nav>
        
        <div className="p-6 border-t border-slate-100 text-center bg-slate-50 shrink-0">
          <div className="text-sm font-bold text-slate-800 mb-1">MedAI Platform</div>
          <div className="text-xs text-slate-500 font-medium">
             تطوير: <span className="text-blue-600 font-extrabold block mt-1 text-sm bg-white border border-blue-100 rounded-lg py-1">Yaman Gadhat<br/>يمان قدحات</span>
          </div>
        </div>
      </aside>

      {/* Main Content Area */}
      <main className="flex-1 overflow-y-auto p-4 md:p-8">
        {activeTab === 'chat' && <AIChat user={user} />}
        {activeTab === 'quiz' && <QuizGenerator />}
        {activeTab === 'flashcards' && <Flashcards />}
        {activeTab === 'planner' && <StudyPlanner />}
        {activeTab === 'calculators' && <MedicalCalculators />}
        {activeTab === 'labs' && <LabValues />}
        {activeTab === 'focus' && <FocusTimer />}
        {activeTab === 'drive' && <DriveFiles user={user} />}
      </main>
    </div>
  );
};

export default function App() {
  const [appState, setAppState] = useState('login');
  const [user, setUser] = useState(null);

  const handleLogin = (userData) => {
    setUser(userData);
    setAppState('onboarding');
  };

  const handleOnboardingComplete = (fullUserData) => {
    setUser(fullUserData);
    setAppState('main');
  };

  return (
    <>
      <div className="bg-animated"></div>
      {appState === 'login' && <LoginScreen onLogin={handleLogin} />}
      {appState === 'onboarding' && <OnboardingScreen user={user} onComplete={handleOnboardingComplete} />}
      {appState === 'main' && <MainApp user={user} />}
    </>
  );
}
