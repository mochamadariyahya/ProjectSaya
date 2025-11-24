import React, { useMemo, useState } from "react";

/**
 * RupiahPercentageCalculator
 * Clean, defensive implementation that guarantees a single enclosing JSX root
 * and includes a small example Jest test (commented) you can paste into a test file.
 */
export default function RupiahPercentageCalculator() {
  const [raw, setRaw] = useState("");

  // parse input to integer rupiah value (ignore non-digits)
  const value = useMemo(() => {
    const digits = String(raw || "").replace(/[^0-9]/g, "");
    return digits === "" ? 0 : parseInt(digits, 10);
  }, [raw]);

  const fmt = (v) =>
    new Intl.NumberFormat("id-ID", { style: "currency", currency: "IDR", maximumFractionDigits: 0 }).format(v);

  const results = useMemo(() => {
    return {
      original: value,
      p11: Math.round(value * 0.11),
      p16: Math.round(value * 0.16),
      p5: Math.round(value * 0.05),
      minus5: Math.round(value * 0.95),
      plus10: Math.round(value * 1.10),
    };
  }, [value]);

  function handleChange(e) {
    // accept pasted or typed values that may include separators; keep only digits internally
    const input = e && e.target && typeof e.target.value === "string" ? e.target.value : "";
    const cleaned = input.replace(/[^0-9]/g, "");
    setRaw(cleaned);
  }

  function formatInputForDisplay(s) {
    const digits = (s || "").replace(/[^0-9]/g, "");
    if (!digits) return "";
    return new Intl.NumberFormat("id-ID").format(parseInt(digits, 10));
  }

  // SINGLE enclosing root (div) to avoid 'adjacent JSX elements' errors
  return (
    <div className="max-w-2xl mx-auto p-6 bg-white rounded-2xl shadow-lg">
      <h1 className="text-2xl font-semibold mb-4">RG Cibarusah Kota</h1>

      <label className="block text-sm font-medium mb-2">Masukkan nilai (IDR)</label>
      <div className="flex gap-2 items-center mb-4">
        <input
          aria-label="nilai rupiah"
          value={formatInputForDisplay(raw)}
          onChange={handleChange}
          placeholder="0"
          className="flex-1 p-3 border rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-indigo-300"
        />
        <button
          type="button"
          onClick={() => setRaw("")}
          className="px-3 py-2 bg-gray-100 rounded-lg text-sm"
        >
          Reset
        </button>
        <button
          type="button"
          onClick={() => setRaw((prev) => `${prev || ""}000`)}
          className="px-3 py-2 bg-gray-100 rounded-lg text-sm"
        >
          +000
        </button>
      </div>

      <div className="grid grid-cols-2 gap-4">

        <section className="p-4 rounded-lg border">
          <div className="text-xs text-gray-500">Diskon Tarif 50%</div>
          <div className="mt-2 text-lg font-medium">{fmt(results.p5)}</div>
          <div className="text-xs text-gray-500">Total</div>
          <div className="mt-2 text-lg font-medium">{fmt(results.minus5)}</div>
        </section>     
      
        <section className="p-4 rounded-lg border">
          <div className="text-xs text-gray-500">Perpanjang Normal</div>
          <div className="mt-2 text-lg font-medium">{fmt(results.p11)}</div>
        </section>

        <section className="p-4 rounded-lg border">
          <div className="text-xs text-gray-500">Perpanjang Lewat Tempo</div>
          <div className="mt-2 text-lg font-medium">{fmt(results.p16)}</div>
        </section>

        <section className="col-span-2 p-4 rounded-lg border">
          <div className="text-xs text-gray-500">Tebus lewat tempo</div>
          <div className="mt-2 text-lg font-medium">{fmt(results.plus10)}</div>
        </section>
      </div>

      <footer className="mt-6 text-sm text-gray-600">by ari</footer>
    </div>
  );
}

/*
Example Jest + React Testing Library test (copy to e.g. RupiahPercentageCalculator.test.jsx):

import React from 'react';
import { render, screen, fireEvent } from '@testing-library/react';
import RupiahPercentageCalculator from './RupiahPercentageCalculator';

test('renders and calculates percentages correctly', () => {
  render(<RupiahPercentageCalculator />);
  const input = screen.getByLabelText(/nilai rupiah/i);

  // type 100000 (Rp 100.000)
  fireEvent.change(input, { target: { value: '100000' } });

  // expect displayed formatted value
  expect(screen.getByText(/Rp/)).toBeInTheDocument();

  // check 11% of 100000 = 11000
  expect(screen.getByText('Rp11.000')).toBeInTheDocument();

  // check 5% of 100000 = 5000
  expect(screen.getByText('Rp5.000')).toBeInTheDocument();
});
*/
            
