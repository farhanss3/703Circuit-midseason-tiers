<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>703 Circuit · Mid-Season Re-Tier</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
<style>
  :root{
    --bg: #f8f9fb;
    --surface: #ffffff;
    --surface-2: #f3f5f9;
    --surface-3: #e8ecf3;
    --border: #e3e7ee;
    --border-strong: #c9d1dd;
    --ink: #16181d;
    --ink-2: #3a3f48;
    --muted: #6b7280;
    --muted-2: #9aa3b0;

    --brand: #ff6b35;
    --brand-soft: #fff1ea;
    --brand-deep: #d94e1f;
    --accent: #1a73e8;
    --accent-soft: #e8f0fe;
    --success: #137333;
    --success-soft: #e6f4ea;
    --warn: #b06000;
    --warn-soft: #fef7e0;
    --danger: #c5221f;
    --danger-soft: #fce8e6;

    --t1: #ff6b35;  --t1-soft: #fff1ea;
    --t2: #f9ab00;  --t2-soft: #fef7e0;
    --t3: #34a853;  --t3-soft: #e6f4ea;
    --t4: #1a73e8;  --t4-soft: #e8f0fe;
    --t5: #9334e6;  --t5-soft: #f3e8fd;

    --shadow-1: 0 1px 2px rgba(60,64,67,.08), 0 1px 3px 1px rgba(60,64,67,.05);
    --shadow-2: 0 2px 6px rgba(60,64,67,.10), 0 1px 2px rgba(60,64,67,.06);
    --shadow-3: 0 4px 16px rgba(60,64,67,.14), 0 2px 6px rgba(60,64,67,.08);
    --shadow-4: 0 12px 32px rgba(60,64,67,.18), 0 4px 12px rgba(60,64,67,.10);

    --r-sm: 8px; --r-md: 12px; --r-lg: 18px; --r-xl: 24px; --r-pill: 999px;
  }

  *{box-sizing:border-box;margin:0;padding:0}
  html,body{
    background:var(--bg);color:var(--ink);
    font-family:'Inter',-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif;
    min-height:100vh;font-size:14px;line-height:1.5;
    -webkit-font-smoothing:antialiased;text-rendering:optimizeLegibility;
  }
  body{
    background-image:
      radial-gradient(circle at 0% 0%, rgba(255,107,53,0.04), transparent 50%),
      radial-gradient(circle at 100% 100%, rgba(26,115,232,0.04), transparent 50%);
    background-attachment:fixed;
  }
  .page{max-width:1200px;margin:0 auto;padding:24px 24px 100px}
  h1,h2,h3,h4{font-family:'Plus Jakarta Sans',sans-serif;letter-spacing:-0.01em;color:var(--ink)}

  /* App bar */
  .app-bar{
    background:var(--surface);border-radius:var(--r-xl);
    padding:16px 24px;margin-bottom:24px;
    display:flex;align-items:center;justify-content:space-between;gap:16px;
    box-shadow:var(--shadow-1);border:1px solid var(--border);
  }
  .brand{display:flex;align-items:center;gap:14px}
  .brand-mark{
    width:44px;height:44px;border-radius:14px;
    background:linear-gradient(135deg, var(--brand), var(--brand-deep));
    display:flex;align-items:center;justify-content:center;
    color:white;font-weight:800;font-size:14px;font-family:'Plus Jakarta Sans',sans-serif;
    box-shadow:0 4px 12px rgba(255,107,53,0.35), inset 0 1px 0 rgba(255,255,255,0.2);
    position:relative;letter-spacing:-0.02em;
  }
  .brand-mark::after{
    content:'';position:absolute;inset:8px;border-radius:50%;
    border:1.5px solid rgba(255,255,255,0.5);
  }
  .brand-text h1{font-size:18px;font-weight:700;line-height:1.2}
  .brand-text .sub{font-size:12px;color:var(--muted);font-weight:500;margin-top:1px}
  .session-chip{
    display:flex;align-items:center;gap:8px;
    background:var(--surface-2);padding:8px 14px 8px 8px;border-radius:var(--r-pill);
    font-size:13px;font-weight:500;color:var(--ink-2);
  }
  .session-avatar{
    width:30px;height:30px;border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    color:white;font-weight:700;font-size:12px;
    font-family:'Plus Jakarta Sans',sans-serif;flex-shrink:0;letter-spacing:-0.02em;
  }
  .session-chip button{
    background:transparent;border:none;cursor:pointer;
    color:var(--muted);font-size:12px;padding:2px 8px;
    margin-left:4px;border-radius:var(--r-pill);transition:all .15s;
  }
  .session-chip button:hover{background:var(--surface-3);color:var(--ink)}

  /* Buttons */
  .btn{
    display:inline-flex;align-items:center;justify-content:center;gap:8px;
    background:var(--surface);color:var(--ink);
    border:1px solid var(--border-strong);
    padding:10px 20px;border-radius:var(--r-pill);
    font-family:inherit;font-size:14px;font-weight:500;
    cursor:pointer;transition:all .18s cubic-bezier(.2,.0,.2,1);
    text-decoration:none;line-height:1;white-space:nowrap;
  }
  .btn:hover{background:var(--surface-2);box-shadow:var(--shadow-1)}
  .btn:active{transform:scale(0.98)}
  .btn.primary{background:var(--brand);color:white;border-color:transparent;box-shadow:0 2px 6px rgba(255,107,53,0.30)}
  .btn.primary:hover{background:var(--brand-deep);box-shadow:0 4px 14px rgba(255,107,53,0.40)}
  .btn.accent{background:var(--accent);color:white;border-color:transparent;box-shadow:0 2px 6px rgba(26,115,232,0.25)}
  .btn.accent:hover{background:#1557b0;box-shadow:0 4px 14px rgba(26,115,232,0.35)}
  .btn.success{background:var(--success);color:white;border-color:transparent}
  .btn.success:hover{background:#0d5d27}
  .btn.ghost{background:transparent;border-color:transparent;color:var(--ink-2)}
  .btn.ghost:hover{background:var(--surface-2)}
  .btn.danger{background:transparent;color:var(--danger);border-color:var(--danger)}
  .btn.danger:hover{background:var(--danger-soft)}
  .btn.sm{padding:6px 14px;font-size:13px}
  .btn:disabled{opacity:0.45;cursor:not-allowed;pointer-events:none}
  .btn .icon{font-size:16px;line-height:1}

  /* Login */
  .login-shell{display:grid;grid-template-columns:minmax(320px, 460px);justify-content:center;padding-top:40px}
  .login-card{background:var(--surface);border-radius:var(--r-xl);padding:36px 32px;box-shadow:var(--shadow-2);border:1px solid var(--border)}
  .login-card .hero{text-align:center;margin-bottom:28px}
  .login-card .hero h2{font-size:24px;font-weight:700;margin-bottom:6px}
  .login-card .hero p{color:var(--muted);font-size:14px}
  .login-meta{
    display:flex;align-items:center;justify-content:center;gap:8px;
    font-size:12px;color:var(--muted);margin-bottom:24px;
    padding:10px 14px;background:var(--surface-2);border-radius:var(--r-md);
  }
  .login-meta .dot-live{width:6px;height:6px;border-radius:50%;background:var(--success);animation:pulse 2s infinite}
  .login-meta strong{color:var(--ink);font-weight:600}
  @keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:0.5;transform:scale(0.8)}}
  .captain-list{display:flex;flex-direction:column;gap:6px}
  .captain-btn{
    background:var(--surface);border:1px solid var(--border);border-radius:var(--r-md);
    padding:12px 14px;cursor:pointer;
    display:flex;align-items:center;justify-content:space-between;gap:12px;
    transition:all .15s;text-align:left;font-family:inherit;font-size:14px;color:var(--ink);
  }
  .captain-btn:hover{background:var(--surface-2);border-color:var(--border-strong);transform:translateY(-1px);box-shadow:var(--shadow-1)}
  .captain-btn.submitted{background:var(--success-soft);border-color:#b8dec0}
  .captain-btn-info{display:flex;align-items:center;gap:12px}
  .team-avatar{
    width:34px;height:34px;border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    color:white;font-size:11px;font-weight:700;flex-shrink:0;
    font-family:'Plus Jakarta Sans',sans-serif;letter-spacing:-0.02em;
  }
  .captain-btn .name{font-weight:600;color:var(--ink)}
  .captain-btn .team-line{font-size:12px;color:var(--muted);margin-top:1px}
  .captain-btn .status{
    font-size:11px;font-weight:600;letter-spacing:0.02em;
    padding:4px 9px;border-radius:var(--r-pill);
    background:var(--surface-3);color:var(--muted);flex-shrink:0;
  }
  .captain-btn.submitted .status{background:var(--success);color:white}
  .login-divider{display:flex;align-items:center;gap:12px;margin:24px 0 16px;color:var(--muted);font-size:12px}
  .login-divider::before,.login-divider::after{content:'';flex:1;height:1px;background:var(--border)}
  .login-actions{display:flex;flex-direction:column;gap:8px}

  /* Status banner */
  .status-banner{
    background:var(--surface);border-radius:var(--r-lg);
    padding:18px 22px;margin-bottom:20px;
    box-shadow:var(--shadow-1);border:1px solid var(--border);
    display:flex;align-items:center;justify-content:space-between;gap:20px;flex-wrap:wrap;
  }
  .status-banner .title{font-family:'Plus Jakarta Sans',sans-serif;font-size:17px;font-weight:700}
  .status-banner .sub{font-size:13px;color:var(--muted);margin-top:2px}
  .progress-pills{display:flex;gap:6px;flex-wrap:wrap}
  .pp{width:30px;height:8px;border-radius:var(--r-pill);background:var(--surface-3);transition:all .25s}
  .pp.done{background:var(--success)}
  .pp.you{background:var(--brand);transform:scaleY(1.4)}

  /* Info card */
  .info-card{
    background:var(--accent-soft);border:1px solid #c5dafa;
    border-radius:var(--r-lg);padding:14px 18px;margin-bottom:20px;
    display:flex;gap:12px;align-items:flex-start;
    font-size:13px;color:var(--ink-2);line-height:1.55;
  }
  .info-card .ic-icon{
    width:24px;height:24px;border-radius:50%;
    background:var(--accent);color:white;
    display:flex;align-items:center;justify-content:center;
    font-size:14px;font-weight:700;flex-shrink:0;
  }
  .info-card strong{color:var(--ink);font-weight:600}
  .info-card em{font-style:normal;color:var(--accent);font-weight:600}

  /* Toolbar */
  .toolbar{
    background:var(--surface);border-radius:var(--r-lg);
    padding:12px 16px;margin-bottom:16px;
    box-shadow:var(--shadow-1);border:1px solid var(--border);
    display:flex;gap:10px;flex-wrap:wrap;align-items:center;
  }
  .filter-chips{display:flex;gap:6px;flex-wrap:wrap}
  .chip{
    background:transparent;border:1px solid var(--border-strong);
    border-radius:var(--r-pill);padding:7px 14px;
    font-size:13px;font-weight:500;cursor:pointer;
    transition:all .15s;color:var(--ink-2);font-family:inherit;
  }
  .chip:hover{background:var(--surface-2)}
  .chip.active{background:var(--ink);color:white;border-color:var(--ink)}
  .search-input{
    flex:1;min-width:180px;
    background:var(--surface-2);border:1px solid var(--border);
    border-radius:var(--r-pill);padding:8px 16px;
    font-family:inherit;font-size:13px;color:var(--ink);transition:all .15s;
  }
  .search-input:focus{outline:none;background:var(--surface);border-color:var(--accent);box-shadow:0 0 0 3px var(--accent-soft)}

  /* Roster */
  .roster{
    background:var(--surface);border-radius:var(--r-lg);
    box-shadow:var(--shadow-1);border:1px solid var(--border);overflow:hidden;
  }
  .roster-row{
    display:grid;grid-template-columns:36px minmax(200px, 1.6fr) 130px 110px auto;
    align-items:center;gap:16px;padding:14px 20px;
    border-bottom:1px solid var(--border);transition:background .15s;
  }
  .roster-row:last-child{border-bottom:none}
  .roster-row:hover{background:var(--surface-2)}
  .roster-row.changed{background:var(--warn-soft)}
  .roster-row.changed:hover{background:#fdf0c4}
  .roster-row.locked-row{background:var(--surface-2);opacity:0.85}
  .row-num{font-size:13px;color:var(--muted-2);font-weight:500;font-variant-numeric:tabular-nums}
  .player-info .name{font-weight:600;font-size:14px;line-height:1.3;display:flex;align-items:center;gap:8px;flex-wrap:wrap}
  .player-info .style-line{
    font-size:12px;color:var(--muted);margin-top:3px;
    overflow:hidden;text-overflow:ellipsis;display:-webkit-box;
    -webkit-line-clamp:1;-webkit-box-orient:vertical;
  }
  .badge{
    display:inline-block;font-size:10px;font-weight:600;letter-spacing:0.04em;
    text-transform:uppercase;padding:2px 7px;border-radius:var(--r-pill);line-height:1.4;
  }
  .badge.cap{background:var(--brand-soft);color:var(--brand-deep)}
  .badge.team-mine{background:var(--accent-soft);color:var(--accent)}
  .team-cell{display:flex;align-items:center;gap:8px;font-size:13px;color:var(--ink-2)}
  .ppg-cell{display:flex;flex-direction:column;align-items:flex-start;line-height:1.1}
  .ppg-cell .num{font-size:18px;font-weight:700;font-family:'Plus Jakarta Sans',sans-serif}
  .ppg-cell .lbl{font-size:10px;color:var(--muted);font-weight:500;letter-spacing:0.03em;margin-top:2px}
  .tier-selector{display:flex;gap:4px;align-items:center}
  .current-label{font-size:11px;color:var(--muted);font-weight:500;margin-right:8px;white-space:nowrap}
  .tier-btn{
    width:36px;height:36px;
    background:var(--surface);border:1px solid var(--border-strong);
    border-radius:10px;
    font-family:'Plus Jakarta Sans',sans-serif;font-size:14px;font-weight:700;
    cursor:pointer;transition:all .15s;
    display:flex;align-items:center;justify-content:center;
    position:relative;color:var(--ink-2);
  }
  .tier-btn:hover:not(:disabled){background:var(--surface-2);transform:translateY(-1px)}
  .tier-btn.is-current{border-color:var(--brand);border-style:dashed}
  .tier-btn.selected{color:white;border-color:transparent;transform:scale(1.05);box-shadow:var(--shadow-2)}
  .tier-btn.selected[data-tier="1"]{background:var(--t1)}
  .tier-btn.selected[data-tier="2"]{background:var(--t2);color:var(--ink)}
  .tier-btn.selected[data-tier="3"]{background:var(--t3)}
  .tier-btn.selected[data-tier="4"]{background:var(--t4)}
  .tier-btn.selected[data-tier="5"]{background:var(--t5)}
  .lock-tag{
    display:inline-flex;align-items:center;gap:6px;
    background:var(--surface-3);color:var(--muted);
    padding:7px 14px;border-radius:var(--r-pill);
    font-size:12px;font-weight:600;
  }

  /* Submit bar */
  .submit-bar{
    position:sticky;bottom:16px;margin-top:20px;
    padding:14px 22px;background:var(--ink);color:white;
    border-radius:var(--r-pill);
    display:flex;justify-content:space-between;align-items:center;gap:16px;flex-wrap:wrap;
    box-shadow:var(--shadow-4);z-index:10;
  }
  .submit-bar .summary{font-size:13px;color:#cbd0d8}
  .submit-bar .summary strong{color:white;font-weight:600}
  .submit-bar .actions{display:flex;gap:8px}
  .submit-bar .btn{padding:9px 18px}
  .submit-bar .btn.ghost{color:white;background:transparent;border-color:transparent}
  .submit-bar .btn.ghost:hover{background:rgba(255,255,255,0.1)}
  .submit-bar .btn:not(.ghost):not(.primary){background:white;color:var(--ink);border-color:transparent}

  /* Lock banner */
  .lock-banner{
    background:linear-gradient(135deg, #e6f4ea 0%, #f0f9f3 100%);
    border:1px solid #b8dec0;border-radius:var(--r-xl);
    padding:24px 28px;margin-bottom:22px;
    display:flex;justify-content:space-between;align-items:center;gap:20px;flex-wrap:wrap;
  }
  .lock-banner .check-icon{
    width:48px;height:48px;border-radius:50%;
    background:var(--success);color:white;
    display:flex;align-items:center;justify-content:center;
    font-size:24px;font-weight:700;
    box-shadow:0 4px 14px rgba(19,115,51,0.25);flex-shrink:0;
  }
  .lock-banner .lb-content{display:flex;gap:18px;align-items:center}
  .lock-banner h3{font-size:18px;font-weight:700;line-height:1.2}
  .lock-banner p{color:var(--ink-2);font-size:13px;margin-top:4px;line-height:1.5}

  /* Section head */
  .section-head{display:flex;justify-content:space-between;align-items:baseline;margin:28px 0 14px;flex-wrap:wrap;gap:10px}
  .section-head h2{font-size:22px;font-weight:700}
  .section-head .meta{font-size:12px;color:var(--muted);font-weight:500}

  /* Change card */
  .change-grid{display:flex;flex-direction:column;gap:10px}
  .change-card{
    background:var(--surface);border:1px solid var(--border);
    border-radius:var(--r-lg);padding:16px 20px;
    display:grid;grid-template-columns:1fr auto auto auto auto auto;
    gap:18px;align-items:center;
    box-shadow:var(--shadow-1);transition:all .15s;
  }
  .change-card:hover{box-shadow:var(--shadow-2)}
  .change-card.no-change{opacity:0.7}
  .change-card.approved{border-left:4px solid var(--success);background:linear-gradient(90deg, var(--success-soft) 0%, var(--surface) 30%)}
  .change-card.rejected{border-left:4px solid var(--danger);background:linear-gradient(90deg, var(--danger-soft) 0%, var(--surface) 30%)}
  .change-card.rejected .change-name{color:var(--muted)}
  .change-name{font-size:14px;font-weight:600}
  .change-name .change-sub{display:block;font-size:12px;color:var(--muted);font-weight:400;margin-top:2px}
  .tier-pill{
    font-family:'Plus Jakarta Sans',sans-serif;font-size:14px;font-weight:700;
    min-width:44px;height:36px;padding:0 10px;
    display:flex;align-items:center;justify-content:center;
    border-radius:10px;flex-shrink:0;
  }
  .tier-pill[data-tier="1"]{background:var(--t1-soft);color:var(--t1)}
  .tier-pill[data-tier="2"]{background:var(--t2-soft);color:var(--warn)}
  .tier-pill[data-tier="3"]{background:var(--t3-soft);color:var(--t3)}
  .tier-pill[data-tier="4"]{background:var(--t4-soft);color:var(--t4)}
  .tier-pill[data-tier="5"]{background:var(--t5-soft);color:var(--t5)}
  .arrow-icon{font-size:18px;color:var(--muted)}
  .vote-breakdown{display:flex;gap:3px}
  .vote-breakdown span{
    font-size:11px;font-weight:500;padding:4px 7px;border-radius:6px;
    background:var(--surface-2);color:var(--muted);
    min-width:24px;text-align:center;font-variant-numeric:tabular-nums;
  }
  .vote-breakdown span.win{background:var(--ink);color:white;font-weight:600}
  .change-actions{display:flex;gap:6px}
  .change-actions button{
    background:var(--surface);border:1px solid var(--border-strong);
    padding:6px 12px;cursor:pointer;border-radius:var(--r-pill);
    font-family:inherit;font-size:12px;font-weight:500;
    transition:all .15s;color:var(--ink-2);
  }
  .change-actions button:hover{background:var(--surface-2)}
  .change-actions button.do-approve.on{background:var(--success);color:white;border-color:var(--success)}
  .change-actions button.do-reject.on{background:var(--danger);color:white;border-color:var(--danger)}

  /* Commish panel */
  .commish-panel{
    background:linear-gradient(135deg, #fff7ed 0%, #fef3e2 100%);
    border:1px solid #fbd9b3;border-radius:var(--r-xl);
    padding:22px 26px;margin:22px 0;
    display:flex;justify-content:space-between;align-items:center;gap:18px;flex-wrap:wrap;
  }
  .commish-panel .cp-icon{
    width:42px;height:42px;border-radius:12px;
    background:var(--brand);color:white;
    display:flex;align-items:center;justify-content:center;
    font-size:20px;flex-shrink:0;
  }
  .commish-panel .cp-content{display:flex;gap:16px;align-items:center}
  .commish-panel h3{font-size:17px;font-weight:700}
  .commish-panel p{color:var(--ink-2);font-size:13px;margin-top:3px;line-height:1.45}

  /* Final stamp */
  .final-stamp{
    background:linear-gradient(135deg, var(--success) 0%, #0d5d27 100%);
    color:white;border-radius:var(--r-xl);
    padding:32px;text-align:center;margin:24px 0;
    box-shadow:var(--shadow-3);position:relative;overflow:hidden;
  }
  .final-stamp::before{
    content:'';position:absolute;inset:0;
    background:radial-gradient(circle at 20% 20%, rgba(255,255,255,0.15), transparent 50%);
    pointer-events:none;
  }
  .final-stamp .icon-big{
    width:60px;height:60px;border-radius:50%;
    background:rgba(255,255,255,0.2);
    display:flex;align-items:center;justify-content:center;
    margin:0 auto 12px;font-size:30px;
    backdrop-filter:blur(4px);border:2px solid rgba(255,255,255,0.3);
  }
  .final-stamp h2{color:white;font-size:24px;font-weight:700;line-height:1.2}
  .final-stamp p{color:rgba(255,255,255,0.85);font-size:13px;margin-top:6px}

  /* Dashboard */
  .dash-controls{
    background:var(--surface);border-radius:var(--r-lg);
    padding:18px 20px;margin-bottom:18px;
    box-shadow:var(--shadow-1);border:1px solid var(--border);
    display:flex;gap:24px;flex-wrap:wrap;align-items:flex-end;
  }
  .ctrl-group{display:flex;flex-direction:column;gap:8px}
  .ctrl-group label{font-size:11px;font-weight:600;letter-spacing:0.04em;text-transform:uppercase;color:var(--muted