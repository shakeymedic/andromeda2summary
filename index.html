import React, { useState } from 'react';
import { 
  Activity, Users, Syringe, Scale, CheckCircle, AlertCircle, 
  BookOpen, HeartPulse, ChevronRight, Check, X, ClipboardList, 
  TrendingUp, AlertTriangle, ArrowDown, Zap, 
  Stethoscope, BarChart3, ChevronDown, ChevronUp, Trophy, HelpCircle,
  Timer, BedDouble, Skull
} from 'lucide-react';

// --- Data ---

const summaryData = {
  title: "ANDROMEDA-SHOCK-2",
  subtitle: "Personalised Haemodynamic Resuscitation Targeting Capillary Refill Time in Early Septic Shock",
  published: "JAMA, Dec 2025",
  bluf: "A bedside perfusion-guided resuscitation strategy (targeting Capillary Refill Time) did not reduce mortality compared to usual care, but it successfully reduced the duration of organ support and hospital length of stay.",
  pico: {
    p: {
      title: "Population",
      icon: Users,
      points: [
        "Adults (≥18 years) with early septic shock (<4h from diagnosis).",
        "Lactate ≥2.0 mmol/L + Vasopressors required after >1000 mL fluid.",
        "n = 1467 included."
      ]
    },
    c: {
      title: "Comparator (Usual Care)",
      icon: Scale,
      points: [
        "Management per local protocols & Surviving Sepsis Guidelines.",
        "Fluid responsiveness & echo allowed (not mandated).",
        "CRT measured only at baseline/6hrs."
      ]
    },
    o: {
      title: "Outcome",
      icon: Activity,
      points: [
        "Primary: Hierarchical Composite (Win Ratio) of:",
        "1. All-cause mortality (28 days)",
        "2. Duration of vital support",
        "3. Length of hospital stay"
      ]
    }
  },
  protocol: [
    {
      step: "Target",
      desc: "Normalise Capillary Refill Time (CRT) to ≤ 3 seconds every 30 mins for 6 hours.",
      icon: Activity
    },
    {
      step: "Tier 1: Assessment",
      desc: "Check Pulse Pressure (PP) & Diastolic BP (DAP).",
      substeps: [
        "PP <40 mmHg? → Give Fluid Bolus (if responsive).",
        "DAP <50 mmHg? → Increase Noradrenaline."
      ],
      icon: Stethoscope
    },
    {
      step: "Tier 2: Refractory",
      desc: "If CRT still >3s: Perform Bedside Echo.",
      substeps: [
        "No cardiac dysfunction? → More Fluids.",
        "Goal not met? → MAP Challenge (80-85 mmHg) OR Dobutamine Test."
      ],
      icon: HeartPulse
    }
  ],
  casp: [
    { q: "Did the study address a clearly focused issue?", a: "YES", detail: "Clear population and intervention." },
    { q: "Was assignment randomised?", a: "YES", detail: "Central randomisation with stratification." },
    { q: "Were all patients accounted for?", a: "YES", detail: "Intention-to-treat analysis used." },
    { q: "Were groups similar at start?", a: "YES", detail: "Balanced for age, comorbidities, and SOFA scores." },
    { q: "Were groups treated equally?", a: "MOSTLY", detail: "Intervention group received more intensive monitoring." },
    { q: "Were clinicians 'blind'?", a: "NO", detail: "Impossible to blind clinicians to the protocol." },
    { q: "How large was the effect?", a: "MODEST", detail: "Win ratio of 1.16." },
    { q: "How precise was the estimate?", a: "MODERATE", detail: "95% CI 1.02 to 1.33." }
  ],
  results: {
    primary: {
      val: "1.16",
      label: "Win Ratio",
      ci: "95% CI 1.02-1.33; P=.04",
      interp: "Intervention patients were 16% more likely to have a better outcome."
    },
    secondary: [
      { label: "Mortality (28 days)", res: "NO DIFFERENCE", detail: "26.5% vs 26.6%" },
      { label: "Duration of Vital Support", res: "SHORTER", detail: "Significant reduction" },
      { label: "Fluid Volume (6hrs)", res: "LESS FLUID", detail: "-251 mL difference" }
    ]
  },
  swot: {
    strengths: [
      "Generalisability: Large multicentre trial (86 centres).",
      "Feasibility: Uses standard bedside tools (CRT, Echo).",
      "Process: High adherence to protocol."
    ],
    weaknesses: [
      "Unblinded: Potential performance bias.",
      "Composite Endpoint: 'Win' driven by organ support, not mortality.",
      "Complexity: Labour intensive (hourly checks)."
    ]
  },
  conclusion: "Among patients with early septic shock, a personalised haemodynamic resuscitation protocol targeting CRT was superior to usual care for the primary composite outcome, primarily due to a lower duration of vital support.",
  quiz: [
    {
      q: "What was the lactate threshold for inclusion?",
      options: ["1.0 mmol/L", "2.0 mmol/L", "4.0 mmol/L", "Not a criterion"],
      correct: 1,
      expl: "Inclusion required Lactate ≥ 2.0 mmol/L."
    },
    {
      q: "Which is TRUE regarding 28-day mortality?",
      options: ["Intervention lower", "Usual care lower", "No significant difference", "Not measured"],
      correct: 2,
      expl: "There was no significant difference in mortality (26.5% vs 26.6%)."
    },
    {
      q: "What defined 'abnormal' Capillary Refill Time (CRT)?",
      options: ["> 2 seconds", "> 3 seconds", "> 4 seconds", "> 5 seconds"],
      correct: 1,
      expl: "The target was CRT normalisation (≤ 3 seconds), so >3s is abnormal."
    },
    {
      q: "If Diastolic BP (DAP) < 50 mmHg in Tier 1, what is the action?",
      options: ["500ml Crystalloid", "500ml Colloid", "Titrate Noradrenaline", "Start Dobutamine"],
      correct: 2,
      expl: "Tier 1 mandates titrating Noradrenaline if DAP < 50 mmHg."
    },
    {
      q: "How did fluid resuscitation volume differ at 6 hours?",
      options: ["Intervention received MORE", "Intervention received LESS", "Identical amounts", "Not recorded"],
      correct: 1,
      expl: "The intervention group received a mean of 251 mL LESS fluid."
    }
  ]
};

// --- Components ---

const Card = ({ children, className = "" }) => (
  <div className={`bg-white rounded-2xl shadow-md border border-slate-200 overflow-hidden ${className}`}>
    {children}
  </div>
);

const SectionLabel = ({ text, icon: Icon }) => (
  <div className="flex items-center gap-3 mb-8 border-b-2 border-slate-200 pb-3">
    <div className="bg-blue-600 p-2 rounded-lg text-white shadow-sm">
      {Icon && <Icon size={24} />}
    </div>
    <h2 className="text-2xl md:text-3xl font-black text-slate-900 tracking-tight uppercase">
      {text}
    </h2>
  </div>
);

const Badge = ({ children, type = "neutral" }) => {
  const styles = {
    neutral: "bg-slate-100 text-slate-700 border-slate-200",
    success: "bg-emerald-100 text-emerald-800 border-emerald-200",
    blue: "bg-blue-100 text-blue-800 border-blue-200",
    red: "bg-rose-100 text-rose-800 border-rose-200",
  };
  return (
    <span className={`px-3 py-1.5 rounded-lg border text-sm font-bold uppercase tracking-wider ${styles[type]}`}>
      {children}
    </span>
  );
};

// --- Protocol Component ---
const ProtocolFlow = () => {
  return (
    <div className="relative mt-4">
      <div className="absolute left-8 top-4 bottom-4 w-1.5 bg-slate-200 rounded-full"></div>
      
      <div className="space-y-8">
        {summaryData.protocol.map((step, idx) => {
          const Icon = step.icon;
          return (
            <div key={idx} className="relative pl-24">
              {/* Timeline Node */}
              <div className="absolute left-0 top-0 w-16 h-16 bg-white border-4 border-blue-600 rounded-2xl flex items-center justify-center z-10 shadow-lg">
                <Icon size={28} className="text-blue-600" />
              </div>
              
              <Card className="p-6 bg-slate-50 border-blue-100 hover:border-blue-300 transition-colors">
                <div className="flex flex-col mb-3">
                   <span className="text-sm font-black text-blue-600 uppercase tracking-widest mb-1">Step {idx + 1}</span>
                   <h3 className="text-xl font-bold text-slate-900 leading-tight">{step.step}</h3>
                </div>
                <p className="text-lg text-slate-700 mb-4 font-medium">{step.desc}</p>
                {step.substeps && (
                  <div className="bg-white p-4 rounded-xl border border-slate-200 space-y-3 shadow-sm">
                     {step.substeps.map((sub, sIdx) => (
                       <div key={sIdx} className="flex gap-3 items-start">
                         <div className="mt-1.5 w-2 h-2 rounded-full bg-blue-500 shrink-0" />
                         <span className="text-base text-slate-700 font-medium">{sub}</span>
                       </div>
                     ))}
                  </div>
                )}
              </Card>
            </div>
          );
        })}
      </div>
    </div>
  );
};

// --- Win Ratio Explainer Section ---
const WinRatioDeepDive = () => {
  return (
    <div className="bg-slate-50 rounded-3xl border border-slate-200 p-6 md:p-8">
       <div className="flex items-start gap-4 mb-6">
          <div className="bg-amber-100 p-3 rounded-xl text-amber-700">
             <HelpCircle size={32} />
          </div>
          <div>
            <h3 className="text-2xl font-black text-slate-900 uppercase tracking-wide">Understanding the Win Ratio</h3>
            <p className="text-slate-600 font-medium mt-1">Why use it? And what does 1.16 actually mean?</p>
          </div>
       </div>

       <div className="grid md:grid-cols-2 gap-8">
          
          {/* Explanation Column */}
          <div className="space-y-6">
             <Card className="p-5 border-l-4 border-l-amber-400">
                <h4 className="font-bold text-slate-800 mb-2 flex items-center gap-2">
                   <Users size={18} /> The Concept: "Patient Pairs"
                </h4>
                <p className="text-sm text-slate-600 leading-relaxed">
                   Imagine taking every patient in the intervention group and pairing them against every patient in the control group. The algorithm decides a "Winner" for each pair based on a hierarchy of events.
                </p>
             </Card>

             <Card className="p-5 border-l-4 border-l-amber-400">
                <h4 className="font-bold text-slate-800 mb-2 flex items-center gap-2">
                   <BarChart3 size={18} /> The Calculation
                </h4>
                <p className="text-sm text-slate-600 leading-relaxed mb-3">
                   <code className="bg-slate-100 px-2 py-1 rounded font-bold">Wins (Intervention) ÷ Wins (Control)</code>
                </p>
                <ul className="space-y-2 text-sm text-slate-600">
                   <li className="flex gap-2"><ArrowDown size={14} className="mt-1"/> <b>Ratio {'>'} 1.0:</b> Intervention is better.</li>
                   <li className="flex gap-2"><ArrowDown size={14} className="mt-1"/> <b>Ratio {'<'} 1.0:</b> Control is better.</li>
                </ul>
             </Card>
          </div>

          {/* Visual Hierarchy Column */}
          <div className="relative">
             <div className="absolute left-6 top-4 bottom-4 w-1 bg-amber-200 rounded-full"></div>
             
             <div className="space-y-4">
                <div className="relative pl-14">
                   <div className="absolute left-2 top-2 w-8 h-8 bg-white border-2 border-slate-300 rounded-full flex items-center justify-center z-10">
                      <span className="text-xs font-bold text-slate-400">1</span>
                   </div>
                   <div className="bg-white p-3 rounded-xl border border-slate-200 shadow-sm opacity-50">
                      <div className="flex justify-between items-center mb-1">
                         <span className="text-xs font-bold uppercase text-slate-400">Highest Priority</span>
                         <Skull size={16} className="text-slate-400" />
                      </div>
                      <p className="font-bold text-slate-500">Mortality</p>
                      <p className="text-xs text-slate-400">Did one patient survive while the other died?</p>
                      <div className="mt-2 text-xs bg-slate-100 p-1 px-2 rounded inline-block">Result: TIE (No diff)</div>
                   </div>
                </div>

                <div className="relative pl-14">
                   <div className="absolute left-0 top-1 w-12 h-12 bg-amber-500 border-4 border-white rounded-full flex items-center justify-center z-10 shadow-lg">
                      <Trophy size={20} className="text-white" />
                   </div>
                   <div className="bg-white p-4 rounded-xl border-2 border-amber-400 shadow-md transform scale-105 origin-left">
                      <div className="flex justify-between items-center mb-1">
                         <span className="text-xs font-bold uppercase text-amber-600">The Decider</span>
                         <Timer size={18} className="text-amber-500" />
                      </div>
                      <p className="font-black text-slate-800 text-lg">Duration of Vital Support</p>
                      <p className="text-sm text-slate-600">If both survived, who needed vasopressors/ventilation for less time?</p>
                      <div className="mt-2 text-xs font-bold text-amber-700 bg-amber-100 p-1 px-2 rounded inline-flex items-center gap-1">
                         <Check size={12} /> Intervention Won Here
                      </div>
                   </div>
                </div>

                <div className="relative pl-14">
                   <div className="absolute left-2 top-2 w-8 h-8 bg-white border-2 border-slate-300 rounded-full flex items-center justify-center z-10">
                      <span className="text-xs font-bold text-slate-400">3</span>
                   </div>
                   <div className="bg-white p-3 rounded-xl border border-slate-200 shadow-sm opacity-75">
                      <div className="flex justify-between items-center mb-1">
                         <span className="text-xs font-bold uppercase text-slate-400">Lowest Priority</span>
                         <BedDouble size={16} className="text-slate-400" />
                      </div>
                      <p className="font-bold text-slate-500">Length of Hospital Stay</p>
                      <p className="text-xs text-slate-400">If support time was equal, who went home sooner?</p>
                   </div>
                </div>
             </div>
          </div>

       </div>
    </div>
  );
};

// --- Win Ratio Visual Component ---
const WinRatioVisual = () => {
  return (
    <div className="mt-6 p-6 bg-slate-100 rounded-xl border border-slate-200">
      <div className="flex justify-between text-xs font-bold text-slate-500 mb-3 uppercase tracking-widest">
        <span>Control (1.0)</span>
        <span className="text-emerald-600">Intervention (+16%)</span>
      </div>
      <div className="flex h-16 w-full rounded-xl overflow-hidden relative shadow-inner bg-slate-200">
        <div className="w-1/2 flex items-center justify-center text-slate-400 font-bold border-r-2 border-slate-300 text-lg">
          Reference
        </div>
        <div className="bg-emerald-500 w-1/2 flex items-center justify-center text-white font-black text-2xl relative overflow-hidden">
          <div className="absolute inset-0 bg-white/20 w-[16%] border-r border-white/30"></div> 
          <span className="relative z-10 drop-shadow-md">1.16</span>
        </div>
      </div>
      <p className="text-sm text-center mt-4 text-slate-500 font-medium">
        Intervention group: <span className="text-emerald-600 font-bold">16% higher probability</span> of a better outcome.
      </p>
    </div>
  );
};

// --- Accordion ---
const CaspAccordion = () => {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div className="border-2 border-slate-200 rounded-2xl overflow-hidden bg-white shadow-sm">
      <button 
        onClick={() => setIsOpen(!isOpen)}
        className="w-full p-6 flex items-center justify-between bg-slate-50 hover:bg-blue-50 transition-colors group"
      >
        <div className="flex items-center gap-4">
          <div className="bg-blue-100 p-2 rounded-lg text-blue-700 group-hover:bg-blue-200 transition-colors">
             <ClipboardList size={28} />
          </div>
          <div className="text-left">
            <h3 className="text-xl font-bold text-slate-900">CASP Critical Appraisal</h3>
            <p className="text-sm text-slate-500 font-medium">Click to {isOpen ? 'collapse' : 'expand'} checklist</p>
          </div>
        </div>
        {isOpen ? <ChevronUp size={24} className="text-slate-400" /> : <ChevronDown size={24} className="text-slate-400" />}
      </button>

      {isOpen && (
        <div className="divide-y divide-slate-100 animate-in slide-in-from-top-2 duration-200">
          {summaryData.casp.map((item, i) => (
            <div key={i} className="p-5 flex flex-col sm:flex-row sm:items-start justify-between gap-4">
              <div className="flex-1">
                 <div className="flex gap-3 mb-1">
                    <span className="text-slate-300 font-black text-lg">{i + 1}.</span>
                    <h3 className="text-lg font-bold text-slate-800 leading-tight">{item.q}</h3>
                 </div>
                 <p className="text-base text-slate-600 pl-8">{item.detail}</p>
              </div>
              <div className="pl-8 sm:pl-0">
                <Badge type={item.a === "YES" ? "success" : item.a === "NO" ? "red" : "neutral"}>
                    {item.a}
                </Badge>
              </div>
            </div>
          ))}
        </div>
      )}
    </div>
  );
};

const QuizComponent = ({ questions }) => {
  const [currentQ, setCurrentQ] = useState(0);
  const [selected, setSelected] = useState(null);
  const [showResult, setShowResult] = useState(false);
  const [score, setScore] = useState(0);
  const [finished, setFinished] = useState(false);

  const handleAnswer = (idx) => {
    if (showResult) return;
    setSelected(idx);
    setShowResult(true);
    if (idx === questions[currentQ].correct) {
      setScore(s => s + 1);
    }
  };

  const nextQuestion = () => {
    if (currentQ < questions.length - 1) {
      setCurrentQ(c => c + 1);
      setSelected(null);
      setShowResult(false);
    } else {
      setFinished(true);
    }
  };

  const reset = () => {
    setCurrentQ(0);
    setSelected(null);
    setShowResult(false);
    setScore(0);
    setFinished(false);
  };

  if (finished) {
    return (
      <Card className="p-10 text-center bg-gradient-to-br from-blue-50 to-indigo-100 border-2 border-blue-200">
        <div className="mx-auto w-20 h-20 bg-white rounded-full flex items-center justify-center shadow-md mb-6">
          <Activity className="text-blue-600" size={40} />
        </div>
        <h3 className="text-3xl font-black text-slate-900 mb-2">Quiz Complete!</h3>
        <p className="text-xl text-slate-600 mb-8 font-medium">You scored <span className="font-bold text-blue-600">{score}</span> / {questions.length}</p>
        <button 
          onClick={reset}
          className="bg-blue-600 text-white px-8 py-4 rounded-xl font-bold text-lg hover:bg-blue-700 transition-colors shadow-lg shadow-blue-200"
        >
          Retake Quiz
        </button>
      </Card>
    );
  }

  const q = questions[currentQ];

  return (
    <Card className="overflow-visible border-2 border-slate-200">
      <div className="p-6 bg-slate-50 border-b border-slate-200 flex justify-between items-center">
        <h3 className="text-lg font-bold text-slate-700 uppercase tracking-wider">Knowledge Check</h3>
        <span className="text-sm font-bold text-slate-600 bg-white px-3 py-1 rounded-lg border border-slate-200 shadow-sm">
          {currentQ + 1} / {questions.length}
        </span>
      </div>
      <div className="p-6 md:p-8">
        <p className="text-xl md:text-2xl font-bold text-slate-900 mb-8 leading-snug">{q.q}</p>
        <div className="space-y-4">
          {q.options.map((opt, i) => {
            let stateClass = "border-slate-200 bg-white hover:border-blue-400 hover:shadow-md";
            const isSelected = selected === i;
            const isCorrect = i === q.correct;
            
            if (showResult) {
              if (isCorrect) stateClass = "border-emerald-500 bg-emerald-50 ring-2 ring-emerald-500";
              else if (isSelected && !isCorrect) stateClass = "border-rose-500 bg-rose-50";
              else stateClass = "border-slate-100 opacity-50 bg-slate-50";
            } else if (isSelected) {
              stateClass = "border-blue-600 bg-blue-50 ring-2 ring-blue-600";
            }

            return (
              <button
                key={i}
                onClick={() => handleAnswer(i)}
                disabled={showResult}
                className={`w-full text-left p-5 rounded-xl border-2 transition-all duration-200 flex justify-between items-center group ${stateClass}`}
              >
                <span className={`text-lg font-medium ${showResult && isCorrect ? 'text-emerald-900' : 'text-slate-700'}`}>{opt}</span>
                {showResult && isCorrect && <Check size={24} className="text-emerald-600" />}
                {showResult && isSelected && !isCorrect && <X size={24} className="text-rose-600" />}
              </button>
            );
          })}
        </div>
        
        {showResult && (
          <div className="mt-8 animate-in fade-in slide-in-from-bottom-4 duration-300">
            <div className="bg-blue-50 p-6 rounded-xl text-base text-slate-700 mb-6 border border-blue-100 flex gap-4">
              <div className="bg-blue-200 p-2 rounded-full h-fit text-blue-700 shrink-0"><BookOpen size={20} /></div>
              <div>
                <span className="font-bold text-blue-900 block mb-1">Explanation</span>
                {q.expl}
              </div>
            </div>
            <button 
              onClick={nextQuestion}
              className="w-full bg-slate-900 text-white py-4 rounded-xl font-bold text-lg hover:bg-slate-800 transition-colors flex items-center justify-center gap-3 shadow-lg"
            >
              {currentQ === questions.length - 1 ? "Finish Quiz" : "Next Question"}
              <ChevronRight size={24} />
            </button>
          </div>
        )}
      </div>
    </Card>
  );
};

// --- Main Layout ---

export default function App() {
  return (
    <div className="min-h-screen bg-slate-100 font-sans text-slate-900 pb-20">
      
      {/* --- HERO HEADER --- */}
      <div className="bg-white border-b border-slate-200 pb-12 pt-8 px-4 mb-10 shadow-sm">
        <div className="max-w-4xl mx-auto text-center">
          
          {/* Logo Section */}
          <div className="flex justify-center mb-6">
            <img 
              src="https://iili.io/KGQOvkl.md.png" 
              alt="WMEBEM Logo" 
              className="h-20 object-contain"
            />
          </div>

          <div className="flex items-center justify-center gap-3 mb-6">
            <span className="px-4 py-1.5 bg-slate-900 text-white text-sm font-bold rounded-full uppercase tracking-widest">Journal Club</span>
            <span className="text-sm text-slate-500 font-bold border border-slate-200 px-3 py-1.5 rounded-full">EMCRIT SUMMARY</span>
          </div>
          <h1 className="text-5xl md:text-7xl font-black tracking-tighter text-slate-900 leading-none mb-6">
            ANDROMEDA<br /><span className="text-blue-600">SHOCK-2</span>
          </h1>
          <p className="text-xl md:text-2xl text-slate-600 max-w-3xl mx-auto leading-relaxed mb-8 font-medium">
            Personalised Haemodynamic Resuscitation Targeting Capillary Refill Time in Early Septic Shock
          </p>
           <div className="inline-flex flex-wrap justify-center gap-4 text-sm font-bold bg-slate-50 border border-slate-200 p-4 rounded-2xl text-slate-600 shadow-sm">
             <span className="flex items-center gap-2"><BookOpen size={18} className="text-blue-500"/> JAMA 2025</span>
             <span className="text-slate-300">|</span>
             <span>RCT</span>
             <span className="text-slate-300">|</span>
             <span>n=1467</span>
          </div>
        </div>
      </div>

      <main className="max-w-4xl mx-auto px-4 space-y-16">
        
        {/* --- BOTTOM LINE UP FRONT --- */}
        <section>
          <div className="bg-slate-900 text-white rounded-3xl p-8 md:p-12 shadow-2xl relative overflow-hidden ring-4 ring-slate-200">
             <div className="absolute -right-6 -top-6 opacity-10 text-white">
                <Activity size={250} />
              </div>
            <h2 className="text-sm font-black uppercase tracking-[0.2em] text-blue-400 mb-4 flex items-center gap-2">
              <Zap size={16} /> Bottom Line Up Front
            </h2>
            <p className="text-2xl md:text-3xl font-bold leading-relaxed relative z-10 text-white">
              {summaryData.bluf}
            </p>
          </div>
        </section>

        {/* --- PROTOCOL --- */}
        <section>
          <SectionLabel text="Intervention Protocol" icon={Syringe} />
          <div className="grid md:grid-cols-2 gap-10">
            <div className="md:col-span-1 flex flex-col gap-6">
              <div className="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm">
                 <h3 className="font-black text-slate-900 mb-2 uppercase tracking-wide text-sm">Concept</h3>
                 <p className="text-lg text-slate-700 leading-relaxed">
                   The experimental group received a structured, protocolised resuscitation strategy driven by peripheral perfusion (CRT) rather than just MAP/Lactate.
                 </p>
              </div>
              <div className="bg-blue-600 p-6 rounded-2xl shadow-lg text-white">
                 <h3 className="font-black mb-4 uppercase tracking-wide text-sm border-b border-blue-400 pb-2">Population Criteria</h3>
                 <ul className="space-y-4">
                    {summaryData.pico.p.points.map((pt, i) => (
                      <li key={i} className="flex gap-3 text-lg font-medium leading-snug">
                        <CheckCircle size={24} className="shrink-0 text-blue-300" />
                        {pt}
                      </li>
                    ))}
                 </ul>
              </div>
            </div>
            <div className="md:col-span-1">
               <ProtocolFlow />
            </div>
          </div>
        </section>

        {/* --- RESULTS --- */}
        <section>
          <SectionLabel text="Key Results" icon={BarChart3} />
          <div className="grid gap-8">
            
            {/* Primary Outcome Highlight - REDESIGNED */}
            <div className="bg-white rounded-3xl shadow-lg border border-slate-200 overflow-hidden">
              <div className="bg-slate-50 border-b border-slate-100 p-5 flex items-center gap-3">
                 <Trophy className="text-emerald-500" size={24} />
                 <h3 className="font-black text-slate-600 uppercase tracking-widest text-sm">Primary Hierarchical Composite</h3>
              </div>
              
              <div className="p-6 md:p-10">
                <div className="flex flex-col md:flex-row gap-8 items-center justify-between mb-8">
                   {/* The Number */}
                   <div className="text-center md:text-left">
                      <div className="text-7xl md:text-8xl font-black text-emerald-600 tracking-tighter leading-none mb-2">
                        {summaryData.results.primary.val}
                      </div>
                      <div className="text-slate-400 font-bold uppercase tracking-wide text-sm pl-2">Win Ratio</div>
                   </div>

                   {/* The Stats Box */}
                   <div className="bg-slate-50 rounded-2xl p-6 border border-slate-200 w-full md:w-auto min-w-[240px] shadow-sm">
                      <div className="flex justify-between items-center mb-3 border-b border-slate-200 pb-3">
                         <span className="text-xs font-bold text-slate-400 uppercase">P-Value</span>
                         <span className="font-mono font-bold text-slate-700 text-lg">0.04</span>
                      </div>
                      <div className="flex justify-between items-center">
                         <span className="text-xs font-bold text-slate-400 uppercase">95% CI</span>
                         <span className="font-mono font-bold text-slate-700 text-lg">1.02 - 1.33</span>
                      </div>
                   </div>
                </div>
                
                <div className="bg-emerald-50/50 rounded-xl p-6 border border-emerald-100 mb-2">
                   <p className="text-slate-800 text-lg font-medium leading-relaxed">
                     {summaryData.results.primary.interp}
                   </p>
                </div>

                <WinRatioVisual />
              </div>
            </div>

            {/* Win Ratio Deep Dive */}
            <WinRatioDeepDive />

            {/* Secondary Results Grid */}
            <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
              {summaryData.results.secondary.map((res, i) => (
                <Card key={i} className="p-6 flex flex-col justify-between h-full bg-white border-t-8 border-t-slate-200 hover:border-t-blue-600 transition-all hover:-translate-y-1 duration-300">
                  <h4 className="text-xs font-black text-slate-400 uppercase mb-3 pb-3 border-b border-slate-100">{res.label}</h4>
                  <div className="mb-2">
                     <p className="text-slate-900 font-black leading-tight text-2xl uppercase">{res.res}</p>
                  </div>
                  <p className="text-slate-500 font-medium text-sm">{res.detail}</p>
                </Card>
              ))}
            </div>
          </div>
        </section>

        {/* --- STRENGTHS & WEAKNESSES --- */}
        <section>
          <SectionLabel text="Critical Appraisal" icon={Scale} />
          <div className="grid md:grid-cols-2 gap-8">
            <div className="bg-white rounded-3xl shadow-sm border-2 border-emerald-100 overflow-hidden">
              <div className="p-6 bg-emerald-50 border-b border-emerald-100 text-emerald-900 font-black text-xl flex items-center gap-3">
                <TrendingUp size={24} className="text-emerald-600"/> Strengths
              </div>
              <ul className="p-8 space-y-4">
                {summaryData.swot.strengths.map((s, i) => (
                  <li key={i} className="text-lg text-slate-700 flex gap-4 leading-snug">
                    <CheckCircle size={24} className="text-emerald-500 mt-0.5 shrink-0" />
                    <span>{s}</span>
                  </li>
                ))}
              </ul>
            </div>

            <div className="bg-white rounded-3xl shadow-sm border-2 border-rose-100 overflow-hidden">
              <div className="p-6 bg-rose-50 border-b border-rose-100 text-rose-900 font-black text-xl flex items-center gap-3">
                <AlertTriangle size={24} className="text-rose-600"/> Weaknesses
              </div>
              <ul className="p-8 space-y-4">
                {summaryData.swot.weaknesses.map((w, i) => (
                  <li key={i} className="text-lg text-slate-700 flex gap-4 leading-snug">
                    <AlertCircle size={24} className="text-rose-500 mt-0.5 shrink-0" />
                    <span>{w}</span>
                  </li>
                ))}
              </ul>
            </div>
          </div>
        </section>

        {/* --- CASP CHECKLIST --- */}
        <section>
          <CaspAccordion />
        </section>

        {/* --- AUTHORS CONCLUSION --- */}
        <section>
           <div className="bg-gradient-to-r from-blue-50 to-indigo-50 p-10 rounded-3xl border-2 border-blue-100 shadow-sm relative text-center">
              <div className="mx-auto w-16 h-16 bg-white rounded-full flex items-center justify-center mb-6 text-blue-600 shadow-md">
                <HeartPulse size={32} />
              </div>
              <h3 className="text-sm font-black uppercase text-slate-400 mb-4 tracking-[0.2em]">Authors' Conclusion</h3>
              <p className="text-slate-800 italic text-2xl md:text-3xl leading-relaxed font-serif">
                "{summaryData.conclusion}"
              </p>
           </div>
        </section>

        {/* --- QUIZ --- */}
        <section>
          <SectionLabel text="Interactive Quiz" icon={Zap} />
          <QuizComponent questions={summaryData.quiz} />
        </section>

      </main>

      <footer className="text-center py-16 text-slate-400 text-sm border-t border-slate-200 bg-white mt-20">
        <p className="font-black text-slate-600 mb-2 tracking-wide uppercase">Summarised for Emergency Medicine Trainees (UK)</p>
        <p className="font-medium">Data Source: ANDROMEDA-SHOCK-2 Trial (JAMA 2025)</p>
      </footer>
    </div>
  );
}
