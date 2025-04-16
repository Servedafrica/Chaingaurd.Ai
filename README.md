import React from "react";
import { motion } from "framer-motion";

export default function ChainGuardLandingPage() {
  return (
    <div className="bg-gray-950 text-white min-h-screen">
      <header className="flex justify-between items-center p-6 max-w-7xl mx-auto">
        <h1 className="text-2xl font-bold">ChainGuard AI</h1>
        <nav className="space-x-4">
          <a href="#product" className="hover:underline">Product</a>
          <a href="#how" className="hover:underline">How It Works</a>
          <a href="#token" className="hover:underline">Token</a>
          <a href="#faq" className="hover:underline">FAQ</a>
          <a href="#cta" className="bg-blue-600 px-4 py-2 rounded hover:bg-blue-700">Join Waitlist</a>
        </nav>
      </header>

      <motion.section
        className="text-center py-20 px-4"
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.6 }}
      >
        <h2 className="text-4xl font-extrabold mb-4">Your Web3 Security & Privacy Guardian</h2>
        <p className="text-lg max-w-2xl mx-auto mb-6">
          AI-powered protection against scams, phishing, and malicious smart contracts — all while keeping you anonymous and in control.
        </p>
        <div className="space-x-4">
          <button className="bg-blue-600 px-6 py-3 rounded text-lg hover:bg-blue-700">Join Waitlist</button>
          <button className="border border-white px-6 py-3 rounded text-lg hover:bg-white hover:text-gray-950">Watch Demo</button>
        </div>
      </motion.section>

      <section id="how" className="bg-gray-900 py-20 px-6">
        <motion.div
          className="max-w-5xl mx-auto grid gap-12 md:grid-cols-2"
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true }}
          transition={{ staggerChildren: 0.2 }}
          variants={{
            visible: { transition: { staggerChildren: 0.2 } },
            hidden: {},
          }}
        >
          {[
            {
              title: "Smart Contract Scanner",
              desc: "Get real-time risk scores and plain English explanations before signing any contract."
            },
            {
              title: "Phishing Detection",
              desc: "Surf safely with browser alerts for scam sites and malicious links."
            },
            {
              title: "Community-Powered Defense",
              desc: "Threats are verified on-chain. Earn $GUARD tokens by helping protect others."
            },
            {
              title: "Privacy-Preserving AI",
              desc: "Your wallet behavior stays private — our AI learns without exposing your data."
            }
          ].map((item, idx) => (
            <motion.div
              key={idx}
              className="p-4"
              initial={{ opacity: 0, y: 30 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.5 }}
            >
              <h3 className="text-2xl font-bold mb-2">{item.title}</h3>
              <p>{item.desc}</p>
            </motion.div>
          ))}
        </motion.div>
      </section>

      <section id="token" className="text-center py-20 px-6">
        <h3 className="text-3xl font-bold mb-6">Introducing $GUARD Token</h3>
        <p className="max-w-3xl mx-auto mb-6">
          Use $GUARD to access premium scans, earn rewards, vote on security decisions, and stake for advanced features.
        </p>
        <p className="font-mono text-lg">Total Supply: 1B | Launch: Q3 2025</p>
      </section>

      <section id="faq" className="bg-gray-900 py-20 px-6">
        <div className="max-w-4xl mx-auto space-y-8">
          <div>
            <h4 className="text-xl font-bold">Do I need to connect my wallet?</h4>
            <p>No — read-only access is enough to get started.</p>
          </div>
          <div>
            <h4 className="text-xl font-bold">Is this open-source?</h4>
            <p>Yes, our scanning models and threat database are community-auditable.</p>
          </div>
          <div>
            <h4 className="text-xl font-bold">Is it free?</h4>
            <p>Yes, with premium features available via $GUARD or subscription.</p>
          </div>
        </div>
      </section>

      <section id="cta" className="text-center py-20 px-6">
        <h3 className="text-3xl font-bold mb-4">Protect your wallet. Empower your Web3 journey.</h3>
        <button className="bg-blue-600 px-8 py-4 rounded text-xl hover:bg-blue-700">Join Waitlist</button>
      </section>

      <section className="bg-gray-950 py-20 px-6">
        <div className="max-w-2xl mx-auto">
          <h3 className="text-2xl font-bold mb-4 text-center">Contact Us</h3>
          <form className="space-y-4">
            <input type="text" placeholder="Your Name" className="w-full p-3 rounded bg-gray-800 text-white" />
            <input type="email" placeholder="Your Email" className="w-full p-3 rounded bg-gray-800 text-white" />
            <textarea placeholder="Message" rows="5" className="w-full p-3 rounded bg-gray-800 text-white"></textarea>
            <button type="submit" className="bg-blue-600 px-6 py-3 rounded hover:bg-blue-700">Send Message</button>
          </form>
        </div>
      </section>

      <footer className="bg-gray-950 text-center py-6 text-sm border-t border-gray-800">
        ChainGuard AI — Decentralized Web3 Security | Whitepaper | Docs | Twitter | Discord
      </footer>
    </div>
  );
}
