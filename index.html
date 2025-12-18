
import React, { useState, useCallback } from 'react';
import Snowfall from './components/Snowfall';
import TypewriterText from './components/TypewriterText';
import { AppState } from './types';
import { generateRomanticMessage } from './services/geminiService';

const App: React.FC = () => {
  const [state, setState] = useState<AppState>(AppState.INITIAL);
  const [extraMessage, setExtraMessage] = useState<string>('');
  const [isLoadingExtra, setIsLoadingExtra] = useState(false);

  const handleStart = () => {
    setState(AppState.TYPING);
  };

  const handleTypingComplete = useCallback(() => {
    setState(AppState.REVEALED);
  }, []);

  const handleGenerateExtra = async () => {
    setIsLoadingExtra(true);
    const msg = await generateRomanticMessage('Robin');
    setExtraMessage(msg);
    setIsLoadingExtra(false);
  };

  return (
    <div className="relative w-full h-screen overflow-hidden flex items-center justify-center bg-[#1a0f0f]">
      {/* Background Layer - Using a warm, tender bokeh Christmas image */}
      <div 
        className="absolute inset-0 bg-cover bg-center transition-all duration-[2000ms] ease-in-out"
        style={{ 
          backgroundImage: `url('https://images.unsplash.com/photo-1512389142860-9c449e58a543?q=80&w=2069&auto=format&fit=crop')`,
          // Baseline blur for a "tender" feel from the start, increasing after click
          filter: state === AppState.INITIAL ? 'blur(2px) brightness(0.8)' : 'blur(8px) brightness(0.5)',
          transform: state === AppState.INITIAL ? 'scale(1)' : 'scale(1.1)'
        }}
      />
      
      {/* Warm glow overlay */}
      <div className={`absolute inset-0 bg-orange-900/10 transition-opacity duration-1000 ${state === AppState.INITIAL ? 'opacity-100' : 'opacity-0'}`} />
      
      {/* Darker overlay for text contrast after click */}
      <div className={`absolute inset-0 bg-black/40 transition-opacity duration-1000 ${state === AppState.INITIAL ? 'opacity-0' : 'opacity-100'}`} />

      <Snowfall />

      {/* Main Content Card */}
      <main className="relative z-20 container mx-auto px-4 flex flex-col items-center">
        {state === AppState.INITIAL && (
          <div className="flex flex-col items-center space-y-8 animate-fadeIn">
            <div className="text-center space-y-2 mb-4">
              <p className="text-white/80 font-serif italic tracking-widest uppercase text-sm">A Special Surprise</p>
            </div>
            <button
              onClick={handleStart}
              className="group relative px-14 py-5 bg-red-600 text-white font-serif text-2xl rounded-full shadow-[0_20px_50px_rgba(220,38,38,0.3)] hover:bg-red-700 transition-all duration-300 transform hover:scale-105 active:scale-95 tracking-wide overflow-hidden"
            >
              <span className="relative z-10 flex items-center gap-3">
                click here
                <svg className="w-5 h-5 animate-bounce" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M19 14l-7 7m0 0l-7-7m7 7V3" />
                </svg>
              </span>
              <div className="absolute inset-0 bg-white/10 translate-y-full group-hover:translate-y-0 transition-transform duration-300" />
            </button>
          </div>
        )}

        {(state === AppState.TYPING || state === AppState.REVEALED) && (
          <div className="max-w-4xl w-full flex flex-col items-center space-y-8 animate-fadeIn">
            <div className="drop-shadow-[0_0_25px_rgba(220,38,38,0.4)]">
              <TypewriterText 
                text={"Merry Christmas\nMy Robin"} 
                speed={150}
                onComplete={handleTypingComplete} 
              />
            </div>

            {state === AppState.REVEALED && (
              <div className="flex flex-col items-center animate-slideUp">
                <div className="bg-white/95 backdrop-blur-md p-10 rounded-2xl shadow-[0_25px_60px_rgba(0,0,0,0.5)] max-w-lg border-t-4 border-red-600">
                  <p className="text-red-800 font-serif text-xl md:text-2xl text-center italic font-semibold leading-relaxed">
                    {extraMessage || "I'm so lucky to have you in my life. You make every season sparkle with your love."}
                  </p>
                </div>
                
                {!extraMessage && (
                  <button
                    onClick={handleGenerateExtra}
                    disabled={isLoadingExtra}
                    className="mt-8 text-red-400 font-bold text-lg underline underline-offset-8 hover:text-red-300 transition-colors disabled:opacity-50 drop-shadow-md"
                  >
                    {isLoadingExtra ? 'Writing a special wish...' : 'Unlock a secret wish for you'}
                  </button>
                )}

                <div className="mt-14 flex items-center gap-8">
                  <div className="w-16 h-px bg-red-600/40" />
                  <span className="font-cursive text-3xl text-red-500 drop-shadow-[0_0_15px_rgba(239,68,68,0.3)]">With all my love</span>
                  <div className="w-16 h-px bg-red-600/40" />
                </div>
              </div>
            )}
          </div>
        )}
      </main>

      <style>{`
        @keyframes fadeIn {
          from { opacity: 0; }
          to { opacity: 1; }
        }
        @keyframes slideUp {
          from { opacity: 0; transform: translateY(40px); }
          to { opacity: 1; transform: translateY(0); }
        }
        .animate-fadeIn {
          animation: fadeIn 1.5s ease-out forwards;
        }
        .animate-slideUp {
          animation: slideUp 1.5s cubic-bezier(0.16, 1, 0.3, 1) 0.5s forwards;
          opacity: 0;
        }
        /* Vibrant Christmas Red for the Cursive Font */
        .font-cursive {
          color: #ef4444 !important; 
          letter-spacing: 0.01em;
        }
        h1.font-cursive {
          color: #dc2626 !important; 
          filter: drop-shadow(0 0 10px rgba(220, 38, 38, 0.3));
        }
      `}</style>
    </div>
  );
};

export default App;
