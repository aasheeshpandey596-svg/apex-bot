<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>APEX AI Terminal Hub</title>
  <script src="https://unpkg.com" crossorigin></script>
  <script src="https://unpkg.com" crossorigin></script>
  <script src="https://unpkg.com"></script>
</head>
<body style="margin:0; background-color:#12141c; color:#fff; font-family:-apple-system, BlinkMacSystemFont, sans-serif;">
  <div id="root"></div>

  <script type="text/babel">
    function App() {
      const [step, setStep] = React.useState("login");
      const [phone, setPhone] = React.useState("");
      const [enteredOtp, setEnteredOtp] = React.useState("");
      const [generatedOtp, setGeneratedOtp] = React.useState("");
      const [inputValue, setInputValue] = React.useState("");
      const [messages, setMessages] = React.useState([]);
      const [loading, setLoading] = React.useState(false);

      const profile = { name: "Champion", calories: 2200, protein: 145, goal: "Body Recomposition" };

      const handleRequestOTP = async (e) => {
        e.preventDefault();
        if (!phone) return alert("Please type your mobile number first!");

        setLoading(true);
        const code = Math.floor(100000 + Math.random() * 900000).toString();
        setGeneratedOtp(code);

        try {
          const res = await fetch("/api/send-otp", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({ phone: phone, otp: code })
          });
          const data = await res.json();

          if (data.success) {
            setStep("verify");
            if (data.mocked) {
              alert(data.msg);
            } else {
              alert("Real authentication token dispatched to your device! 📲");
            }
          } else {
            alert("Gateway error: " + data.error);
          }
        } catch (err) {
          alert("Could not link to backend network bridge node.");
        }
        setLoading(false);
      };

      const handleVerifyOTP = (e) => {
        e.preventDefault();
        if (enteredOtp === generatedOtp) {
          setStep("dashboard");
          setMessages([{ role: "assistant", content: "Identity authenticated successfully. APEX active coaching console fully loaded! ⚡" }]);
        } else {
          alert("Verification token match error.");
        }
      };

      const handleSendMessage = async (e) => {
        e.preventDefault();
        if (!inputValue.trim()) return;

        const userPrompt = inputValue;
        setMessages(prev => [...prev, { role: "user", content: userPrompt }]);
        setInputValue("");

        try {
          const res = await fetch("/api/chat", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({ prompt: userPrompt, profile: profile })
          });
          const data = await res.json();
          setMessages(prev => [...prev, { role: "assistant", content: data.reply }]);
        } catch (err) {
          setMessages(prev => [...prev, { role: "assistant", content: "System offline. API link broken." }]);
        }
      };

      return (
        <div style={{ display: "flex", justifyContent: "center", alignItems: "center", minHeight: "100vh", padding: "20px", boxSizing: "border-box" }}>
          
          {step === "login" && (
            <form onSubmit={handleRequestOTP} style={{ background: "#161925", padding: "30px", borderRadius: "20px", border: "1px solid rgba(255,255,255,0.05)", maxWidth: "360px", width: "100%" }}>
              <h2 style={{ margin: "0 0 10px 0", color: "#00f2fe" }}>APEX System Sync</h2>
              <p style={{ color: "#6b7280", fontSize: "13px", marginBottom: "20px" }}>Enter mobile phone address to establish a secure cryptographic OTP link.</p>
              <input type="text" placeholder="e.g. +919876543210" value={phone} onChange={(e) => setPhone(e.target.value)} style={{ width: "100%", padding: "14px", borderRadius: "10px", background: "#1e2230", border: "1px solid rgba(255,255,255,0.08)", color: "#fff", marginBottom: "18px", boxSizing: "border-box", outline: "none" }} />
              <button type="submit" disabled={loading} style={{ width: "100%", padding: "14px", background: "linear-gradient(135deg, #00f2fe, #adff2f)", border: "none", borderRadius: "10px", fontWeight: "700", color: "#12141c", cursor: "pointer", fontSize: "14px" }}>
                {loading ? "Routing Node Check..." : "Request Access Token"}
              </button>
            </form>
          )}

          {step === "verify" && (
            <form onSubmit={handleVerifyOTP} style={{ background: "#161925", padding: "30px", borderRadius: "20px", border: "1px solid rgba(255,255,255,0.05)", maxWidth: "360px", width: "100%" }}>
              <h2 style={{ margin: "0 0 10px 0", color: "#adff2f" }}>Enter Security Pin</h2>
              <p style={{ color: "#6b7280", fontSize: "13px", marginBottom: "20px" }}>Type the 6-digit dynamic entry key delivered to your messaging device.</p>
              <input type="text" placeholder="6-Digit OTP" value={enteredOtp} onChange={(e) => setEnteredOtp(e.target.value)} style={{ width: "100%", padding: "14px", borderRadius: "10px", background: "#1e2230", border: "1px solid rgba(255,255,255,0.08)", color: "#fff", marginBottom: "18px", boxSizing: "border-box", textAlign: "center", fontSize: "22px", letterSpacing: "4px", outline: "none" }} />
              <button type="submit" style={{ width: "100%", padding: "14px", background: "linear-gradient(135deg, #00f2fe, #adff2f)", border: "none", borderRadius: "10px", fontWeight: "700", color: "#12141c", cursor: "pointer", fontSize: "14px" }}>Verify Matrix Passkey</button>
            </form>
          )}

          {step === "dashboard" && (
            <div style={{ width: "100%", maxWidth: "680px", height: "600px", background: "#161925", borderRadius: "24px", border: "1px solid rgba(255,255,255,0.05)", display: "flex", flexDirection: "column", overflow: "hidden" }}>
              <div style={{ padding: "14px 24px", borderBottom: "1px solid rgba(255,255,255,0.05)", background: "#141622", display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                <div style={{ color: "#00f2fe", fontWeight: "700", fontSize: "14px" }}>APEX CORE ACTIVE</div>
                <div style={{ color: "#6b7280", fontSize: "12px" }}>User Connected | Targets: 2200 kcal • 145g protein</div>
              </div>

              <div style={{ flex: 1, padding: "24px", overflowY: "auto", display: "flex", flexDirection: "column", gap: "14px" }}>
                {messages.map((m, idx) => {
                  const isU = m.role === 'user';
                  return (
                    <div key={idx} style={{ display: "flex", justifyContent: isU ? "flex-end" : "flex-start" }}>
                      <span style={{ padding: "12px 18px", borderRadius: isU ? "20px 20px 4px 20px" : "20px 20px 24px 4px", background: isU ? "linear-gradient(135deg, #00f2fe, #00b8fe)" : "#1e2230", color: isU ? "#12141c" : "#e2e8f0", fontSize: "14px", maxWidth: "75%", whiteSpace: "pre-wrap", fontWeight: isU ? "600" : "400", lineHeight: "1.5" }}>
                        {m.content}
                      </span>
                    </div>
                  );
                })}
              </div>
              
              <form onSubmit={handleSendMessage} style={{ padding: "18px 24px", borderTop: "1px solid rgba(255,255,255,0.05)", display: "flex", gap: "12px", background: "#141622" }}>
                <input type="text" value={inputValue} onChange={(e) => setInputValue(e.target.value)} placeholder="Message APEX regarding meal adjustments..." style={{ flex: 1, padding: "14px", borderRadius: "12px", background: "#1e2230", border: "1px solid rgba(255,255,255,0.05)", color: "#fff", outline: "none", fontSize: "14px" }} />
                <button type="submit" style={{ padding: "0 24px", background: "linear-gradient(135deg, #00f2fe, #adff2f)", color: "#12141c", border: "none", borderRadius: "12px", fontWeight: "700", cursor: "pointer", fontSize: "14px" }}>Send</button>
              </form>
            </div>
          )}

        </div>
      );
    }

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
  </script>
</body>
</html>
