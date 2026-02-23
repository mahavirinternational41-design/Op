# Op
Op
import React, { useState, useEffect } from 'react';
import { 
  Calculator, 
  DollarSign, 
  TrendingUp, 
  Percent, 
  Truck, 
  Info,
  Lock,
  Key,
  Eye,
  EyeOff,
  Copy,
  Check,
  Settings2,
  RefreshCw
} from 'lucide-react';

const App = () => {
  // --- Core State ---
  const [costPrice, setCostPrice] = useState(100);
  const [overhead, setOverhead] = useState(5);
  const [markupOrMargin, setMarkupOrMargin] = useState(30);
  const [taxRate, setTaxRate] = useState(10);
  const [mode, setMode] = useState('markup'); // 'markup' or 'margin'
  
  // --- Secret Key Logic ---
  const [secretKey, setSecretKey] = useState('BLACKHORSE'); 
  const [showKey, setShowKey] = useState(false);
  const [copied, setCopied] = useState(false);

  // --- Calculation Results ---
  const [results, setResults] = useState({
    sellingPrice: 0,
    profit: 0,
    actualMargin: 0,
    taxAmount: 0,
    totalCost: 0,
    encodedPrice: '',
    encodedCost: ''
  });

  // Helper to encode numbers using the 10-letter key
  const encodeValue = (val, key) => {
    if (!key || key.length < 10) return "INVALID KEY";
    const cleanValue = val.toFixed(2).toString();
    let encoded = "";
    
    for (let char of cleanValue) {
      if (char === '.') {
        encoded += '.'; 
      } else if (!isNaN(parseInt(char))) {
        encoded += key[parseInt(char)].toUpperCase();
      }
    }
    return encoded;
  };

  // Main calculation effect
  useEffect(() => {
    const cp = parseFloat(costPrice) || 0;
    const oh = parseFloat(overhead) || 0;
    const totalCost = cp + oh;
    const target = parseFloat(markupOrMargin) || 0;
    const tax = parseFloat(taxRate) || 0;

    let subtotal = 0;
    if (mode === 'markup') {
      subtotal = totalCost * (1 + target / 100);
    } else {
      const marginDecimal = target / 100;
      subtotal = marginDecimal >= 1 ? totalCost * 10 : totalCost / (1 - marginDecimal);
    }

    const taxAmount = subtotal * (tax / 100);
    const finalPrice = subtotal + taxAmount;
    const profit = subtotal - totalCost;
    const actualMargin = subtotal > 0 ? (profit / subtotal) * 100 : 0;

    setResults({
      sellingPrice: finalPrice,
      profit: profit,
      actualMargin: actualMargin,
      taxAmount: taxAmount,
      totalCost: totalCost,
      encodedPrice: encodeValue(finalPrice, secretKey),
      encodedCost: encodeValue(totalCost, secretKey)
    });
  }, [costPrice, overhead, markupOrMargin, taxRate, mode, secretKey]);

  // UI Handlers
  const copyToClipboard = (text) => {
    const el = document.createElement('textarea');
    el.value = text;
    document.body.appendChild(el);
    el.select();
    document.execCommand('copy');
    document.body.removeChild(el);
    setCopied(true);
    setTimeout(() => setCopied(false), 2000);
  };

  const formatCurrency = (value) => {
    return new Intl.NumberFormat('en-US', {
      style: 'currency',
      currency: 'USD',
    }).format(value);
  };

  return (
    <div className="min-h-screen bg-slate-50 font-sans text-slate-900 pb-12">
      {/* App Header */}
      <header className="bg-white border-b border-slate-200 sticky top-0 z-30 px-4 py-4 md:px-8 shadow-sm">
        <div className="max-w-5xl mx-auto flex items-center justify-between">
          <div className="flex items-center gap-3">
            <div className="p-2 bg-indigo-600 text-white rounded-xl shadow-md">
              <Calculator size={22} />
            </div>
            <h1 className="text-xl font-bold tracking-tight">PriceArchitect</h1>
          </div>
          
          <div className="flex items-center gap-2 bg-slate-100 p-1 rounded-full border border-slate-200">
            <Key size={14} className="ml-2 text-amber-500" />
            <input
              type={showKey ? "text" : "password"}
              maxLength={10}
              value={secretKey}
              onChange={(e) => setSecretKey(e.target.value.toUpperCase().replace(/[^A-Z]/g, ''))}
              className="bg-transparent border-none text-xs font-mono font-bold tracking-widest focus:ring-0 w-24 p-1"
            />
            <button onClick={() => setShowKey(!showKey)} className="p-1.5 hover:bg-white rounded-full transition-colors">
              {showKey ? <EyeOff size={14} /> : <Eye size={14} />}
            </button>
          </div>
        </div>
      </header>

      <main className="max-w-5xl mx-auto px-4 mt-6 grid grid-cols-1 lg:grid-cols-12 gap-6">
        {/* Input Section */}
        <section className="lg:col-span-5 space-y-6">
          <div className="bg-white rounded-3xl p-6 shadow-sm border border-slate-200">
            <h2 className="text-xs font-black uppercase tracking-widest text-slate-400 mb-6 flex items-center gap-2">
              <Settings2 size={14} /> Product Variables
            </h2>

            <div className="space-y-5">
              <div>
                <label className="block text-sm font-semibold text-slate-600 mb-2">Cost Price</label>
                <div className="relative group">
                  <DollarSign className="absolute left-4 top-1/2 -translate-y-1/2 text-slate-400" size={18} />
                  <input
                    type="number"
                    value={costPrice}
                    onChange={(e) => setCostPrice(e.target.value)}
                    className="w-full pl-11 pr-4 py-4 bg-slate-50 border border-slate-200 rounded-2xl focus:ring-4 focus:ring-indigo-500/10 focus:border-indigo-500 outline-none transition-all text-lg font-bold"
                  />
                </div>
              </div>

              <div>
                <label className="block text-sm font-semibold text-slate-600 mb-2">Overheads</label>
                <div className="relative group">
                  <Truck className="absolute left-4 top-1/2 -translate-y-1/2 text-slate-400" size={18} />
                  <input
                    type="number"
                    value={overhead}
                    onChange={(e) => setOverhead(e.target.value)}
                    className="w-full pl-11 pr-4 py-4 bg-slate-50 border border-slate-200 rounded-2xl focus:ring-4 focus:ring-indigo-500/10 focus:border-indigo-500 outline-none transition-all text-lg font-bold"
                  />
                </div>
              </div>

              <div className="pt-4 border-t border-slate-100">
                <div className="flex bg-slate-100 p-1 rounded-2xl mb-6">
                  {['markup', 'margin'].map((m) => (
                    <button
                      key={m}
                      onClick={() => setMode(m)}
                      className={`flex-1 py-3 text-xs font-black uppercase rounded-xl transition-all ${
                        mode === m ? 'bg-white text-indigo-600 shadow-md' : 'text-slate-500'
                      }`}
                    >
                      {m} Strategy
                    </button>
                  ))}
                </div>

                <div className="flex justify-between items-center mb-2 text-sm font-semibold text-slate-600">
                  <label>Target {mode === 'markup' ? 'Markup' : 'Margin'}</label>
                  <span className="text-indigo-600 font-black">{markupOrMargin}%</span>
                </div>
                <input
                  type="range"
                  min="0"
                  max={mode === 'margin' ? "90" : "300"}
                  value={markupOrMargin}
                  onChange={(e) => setMarkupOrMargin(e.target.value)}
                  className="w-full h-2 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-indigo-600"
                />
              </div>

              <div className="pt-2">
                <label className="block text-sm font-semibold text-slate-600 mb-2">Sales Tax (%)</label>
                <div className="relative group">
                  <Percent className="absolute left-4 top-1/2 -translate-y-1/2 text-slate-400" size={18} />
                  <input
                    type="number"
                    value={taxRate}
                    onChange={(e) => setTaxRate(e.target.value)}
                    className="w-full pl-11 pr-4 py-3 bg-slate-50 border border-slate-200 rounded-2xl focus:ring-4 focus:ring-indigo-500/10 focus:border-indigo-500 outline-none transition-all font-bold"
                  />
                </div>
              </div>
            </div>
          </div>

          <div className="bg-slate-900 rounded-3xl p-6 text-white shadow-xl relative overflow-hidden text-center">
            <h3 className="text-xs font-black uppercase tracking-widest text-slate-500 mb-4">Coding Matrix</h3>
            <div className="grid grid-cols-5 gap-2 relative z-10">
              {secretKey.padEnd(10, '?').split('').map((char, i) => (
                <div key={i} className="bg-white/10 rounded-xl p-2 border border-white/5">
                  <div className="text-[10px] text-indigo-400 font-black mb-1">{i}</div>
                  <div className="text-lg font-mono font-black">{char}</div>
                </div>
              ))}
            </div>
          </div>
        </section>

        {/* Results Section */}
        <section className="lg:col-span-7 space-y-6">
          <div className="bg-white rounded-[2.5rem] border-2 border-slate-100 shadow-sm overflow-hidden">
            <div className="p-8 text-center flex flex-col items-center">
              <p className="text-sm font-bold text-slate-400 uppercase tracking-widest mb-2">Retail Price</p>
              <h3 className="text-6xl font-black text-slate-900 tracking-tighter mb-8">
                {formatCurrency(results.sellingPrice)}
              </h3>
              
              <div className="w-full max-w-sm bg-indigo-50 rounded-3xl p-6 border border-indigo-100 relative group shadow-inner">
                <div className="absolute -top-3 left-1/2 -translate-x-1/2 bg-indigo-600 text-white text-[10px] font-black px-4 py-1.5 rounded-full shadow-lg flex items-center gap-1.5">
                  <Lock size={12} /> SECRET TAG CODE
                </div>
                <div className="flex items-center justify-between gap-4 mt-2">
                  <span className="text-4xl md:text-5xl font-mono font-black text-indigo-700 tracking-[0.2em] break-all">
                    {results.encodedPrice}
                  </span>
                  <button 
                    onClick={() => copyToClipboard(results.encodedPrice)}
                    className="p-4 bg-white hover:bg-indigo-600 hover:text-white rounded-2xl transition-all text-indigo-600 shadow-sm border border-indigo-200 flex-shrink-0"
                  >
                    {copied ? <Check size={20} /> : <Copy size={20} />}
                  </button>
                </div>
              </div>
            </div>

            <div className="grid grid-cols-2 md:grid-cols-4 border-t border-slate-50 divide-x divide-slate-50 bg-slate-50/30">
              <div className="p-5 text-center">
                <p className="text-[10px] font-black text-slate-400 uppercase mb-1">Profit</p>
                <p className="text-lg font-bold text-green-600">{formatCurrency(results.profit)}</p>
              </div>
              <div className="p-5 text-center">
                <p className="text-[10px] font-black text-slate-400 uppercase mb-1">Margin</p>
                <p className="text-lg font-bold text-slate-800">{results.actualMargin.toFixed(1)}%</p>
              </div>
              <div className="p-5 text-center">
                <p className="text-[10px] font-black text-slate-400 uppercase mb-1">Tax</p>
                <p className="text-lg font-bold text-slate-800">{formatCurrency(results.taxAmount)}</p>
              </div>
              <div className="p-5 text-center">
                <p className="text-[10px] font-black text-slate-400 uppercase mb-1">Total Cost</p>
                <p className="text-lg font-bold text-slate-800">{formatCurrency(results.totalCost)}</p>
              </div>
            </div>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div className="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm">
              <h4 className="text-xs font-black text-slate-400 uppercase mb-4 flex items-center gap-2">
                <Info size={14} /> Cost Reference
              </h4>
              <div className="space-y-3">
                <div className="flex justify-between items-center p-3 bg-slate-50 rounded-xl border border-slate-100">
                  <span className="text-[10px] font-bold text-slate-500 uppercase">Cost Code</span>
                  <span className="font-mono font-bold text-indigo-600 tracking-widest">{results.encodedCost}</span>
                </div>
                <p className="text-[11px] text-slate-400 italic">
                  Write this code on labels to identify your cost price privately.
                </p>
              </div>
            </div>

            <div className="bg-indigo-600 p-6 rounded-3xl text-white shadow-lg relative overflow-hidden group">
              <RefreshCw className="absolute -right-6 -bottom-6 text-white/10 rotate-12 group-hover:rotate-45 transition-transform duration-700" size={140} />
              <h4 className="text-xs font-black text-indigo-200 uppercase mb-2">Strategy Note</h4>
              <p className="text-sm font-medium leading-relaxed">
                Profit: {formatCurrency(results.profit)}. 
                Using the secret key allows you to display values like your cost without the customer knowing.
              </p>
            </div>
          </div>
        </section>
      </main>
    </div>
  );
};

export default App;

