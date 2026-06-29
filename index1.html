<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SalesCRM — Pipeline Manager</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@2.44.0/tabler-icons.min.css">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg-primary: #ffffff;
    --bg-secondary: #f5f5f4;
    --bg-tertiary: #f0ede8;
    --bg-info: #e6f1fb;
    --text-primary: #1a1a18;
    --text-secondary: #6b6b67;
    --text-tertiary: #9b9b97;
    --text-info: #0c447c;
    --border-light: rgba(0,0,0,0.10);
    --border-mid: rgba(0,0,0,0.18);
    --border-strong: rgba(0,0,0,0.28);
    --accent: #185FA5;
    --accent-dark: #0C447C;
    --accent-light: #E6F1FB;
    --success: #0F6E56;
    --success-bg: #E1F5EE;
    --danger: #A32D2D;
    --danger-bg: #FCEBEB;
    --warning: #BA7517;
    --radius-sm: 6px;
    --radius-md: 8px;
    --radius-lg: 12px;
    --shadow-sm: 0 1px 3px rgba(0,0,0,0.08);
    --shadow-md: 0 4px 16px rgba(0,0,0,0.10);
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans Thai', sans-serif;
    background: var(--bg-tertiary);
    color: var(--text-primary);
    font-size: 14px;
    line-height: 1.5;
    min-height: 100vh;
  }

  /* ── Topbar ── */
  .topbar {
    position: sticky; top: 0; z-index: 50;
    background: var(--bg-primary);
    border-bottom: 0.5px solid var(--border-light);
    padding: 0 24px;
    height: 52px;
    display: flex; align-items: center; gap: 16px;
  }
  .logo { font-size: 16px; font-weight: 600; color: var(--text-primary); display: flex; align-items: center; gap: 8px; }
  .logo-dot { width: 10px; height: 10px; border-radius: 50%; background: var(--accent); }
  .nav-tabs { display: flex; gap: 2px; margin-left: auto; background: var(--bg-secondary); padding: 3px; border-radius: var(--radius-md); }
  .nav-tab {
    padding: 5px 16px; border-radius: 6px; font-size: 13px; font-weight: 500;
    cursor: pointer; border: none; background: transparent; color: var(--text-secondary);
    transition: all 0.15s; display: flex; align-items: center; gap: 6px;
  }
  .nav-tab.active { background: var(--bg-primary); color: var(--text-primary); box-shadow: var(--shadow-sm); }
  .nav-tab:hover:not(.active) { color: var(--text-primary); }
  .topbar-right { display: flex; align-items: center; gap: 8px; margin-left: 16px; }
  .topbar-btn {
    padding: 5px 12px; border-radius: var(--radius-md); font-size: 12px; font-weight: 500;
    cursor: pointer; border: 0.5px solid var(--border-mid); background: var(--bg-primary);
    color: var(--text-secondary); transition: all 0.15s; display: flex; align-items: center; gap: 5px;
  }
  .topbar-btn:hover { background: var(--bg-secondary); color: var(--text-primary); }
  .topbar-btn.primary { background: var(--accent); color: #fff; border-color: var(--accent); }
  .topbar-btn.primary:hover { background: var(--accent-dark); }

  /* ── Content ── */
  .content { padding: 20px 24px; }

  /* ── Pipeline ── */
  .pipeline-view { display: flex; gap: 14px; overflow-x: auto; padding-bottom: 16px; align-items: flex-start; }
  .stage-col { min-width: 210px; max-width: 220px; flex-shrink: 0; }
  .stage-header {
    background: var(--bg-primary); border: 0.5px solid var(--border-light);
    border-radius: var(--radius-lg) var(--radius-lg) 0 0;
    padding: 10px 12px; display: flex; align-items: flex-start; justify-content: space-between;
  }
  .stage-name { font-size: 13px; font-weight: 600; color: var(--text-primary); }
  .stage-meta { font-size: 10px; color: var(--text-tertiary); margin-top: 2px; }
  .stage-count {
    font-size: 11px; font-weight: 600; color: var(--text-secondary);
    background: var(--bg-secondary); padding: 2px 8px; border-radius: 20px; flex-shrink: 0;
  }
  .stage-header-right { display: flex; align-items: center; gap: 6px; }
  .stage-action-btn {
    width: 24px; height: 24px; border-radius: var(--radius-sm);
    border: 0.5px solid transparent; background: transparent;
    cursor: pointer; display: flex; align-items: center; justify-content: center;
    color: var(--text-tertiary); transition: all 0.15s; flex-shrink: 0;
  }
  .stage-action-btn:hover { background: var(--bg-secondary); border-color: var(--border-light); color: var(--text-secondary); }
  .stage-action-btn.danger:hover { background: var(--danger-bg); color: var(--danger); border-color: #F09595; }
  .stage-action-btn i { font-size: 13px; line-height: 1; }
  .stage-body {
    background: var(--bg-secondary); border: 0.5px solid var(--border-light);
    border-top: none; border-radius: 0 0 var(--radius-lg) var(--radius-lg);
    min-height: 130px; padding: 8px; display: flex; flex-direction: column; gap: 6px;
    transition: background 0.15s, border-color 0.15s;
  }
  .stage-body.drag-over { background: var(--accent-light); border-color: var(--accent); }

  /* ── Card ── */
  .card {
    background: var(--bg-primary); border: 0.5px solid var(--border-light);
    border-radius: var(--radius-md); padding: 10px 12px; cursor: grab;
    transition: box-shadow 0.15s, opacity 0.15s, transform 0.1s;
    user-select: none;
  }
  .card:hover { box-shadow: var(--shadow-sm); border-color: var(--border-mid); }
  .card:active { cursor: grabbing; }
  .card.dragging { opacity: 0.35; transform: scale(0.98); }
  .card-title { font-size: 13px; font-weight: 600; color: var(--text-primary); margin-bottom: 5px; }
  .card-meta { font-size: 11px; color: var(--text-secondary); display: flex; flex-direction: column; gap: 2px; }
  .card-meta span { display: flex; align-items: center; gap: 4px; }
  .card-meta i { font-size: 11px; color: var(--text-tertiary); }
  .card-value { font-size: 13px; font-weight: 700; color: var(--accent); margin-top: 6px; }
  .card-footer { display: flex; align-items: center; justify-content: space-between; margin-top: 6px; }
  .card-days { font-size: 10px; color: var(--text-tertiary); display: flex; align-items: center; gap: 3px; }
  .type-badge {
    display: inline-block; font-size: 10px; padding: 1px 7px;
    border-radius: 20px; background: var(--accent-light); color: var(--accent-dark);
    font-weight: 500;
  }
  .add-card-btn {
    width: 100%; border: 1.5px dashed var(--border-light); border-radius: var(--radius-md);
    padding: 7px; font-size: 12px; color: var(--text-tertiary); cursor: pointer;
    background: transparent; transition: all 0.15s; display: flex; align-items: center;
    justify-content: center; gap: 5px; margin-top: 2px;
  }
  .add-card-btn:hover { border-color: var(--border-mid); color: var(--text-secondary); background: var(--bg-primary); }
  .add-stage-col {
    min-width: 180px; flex-shrink: 0; border: 1.5px dashed var(--border-light);
    border-radius: var(--radius-lg); padding: 20px 16px; display: flex; align-items: center;
    justify-content: center; gap: 6px; cursor: pointer; color: var(--text-tertiary);
    font-size: 13px; background: transparent; transition: all 0.15s; height: 76px;
    align-self: flex-start;
  }
  .add-stage-col:hover { background: var(--bg-secondary); color: var(--text-secondary); border-color: var(--border-mid); }

  /* ── Dashboard ── */
  .dash-metrics { display: grid; grid-template-columns: repeat(4, 1fr); gap: 12px; margin-bottom: 18px; }
  .metric-card { background: var(--bg-primary); border: 0.5px solid var(--border-light); border-radius: var(--radius-lg); padding: 16px 18px; }
  .metric-label { font-size: 11px; color: var(--text-secondary); font-weight: 500; text-transform: uppercase; letter-spacing: 0.04em; margin-bottom: 6px; }
  .metric-value { font-size: 26px; font-weight: 700; color: var(--text-primary); line-height: 1.1; }
  .metric-sub { font-size: 11px; color: var(--text-tertiary); margin-top: 4px; }
  .metric-card.accent { border-top: 3px solid var(--accent); }
  .metric-card.success { border-top: 3px solid var(--success); }
  .metric-card.warning { border-top: 3px solid var(--warning); }
  .metric-card.danger { border-top: 3px solid var(--danger); }

  .dash-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; margin-bottom: 14px; }
  .dash-card { background: var(--bg-primary); border: 0.5px solid var(--border-light); border-radius: var(--radius-lg); padding: 18px 20px; }
  .dash-card-title { font-size: 13px; font-weight: 600; color: var(--text-primary); margin-bottom: 14px; }
  .bar-row { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; }
  .bar-label { font-size: 12px; color: var(--text-secondary); width: 100px; flex-shrink: 0; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; display: flex; align-items: center; gap: 5px; }
  .bar-track { flex: 1; height: 7px; background: var(--bg-secondary); border-radius: 20px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 20px; transition: width 0.5s; }
  .bar-val { width: 60px; text-align: right; font-size: 12px; font-weight: 600; color: var(--text-primary); }
  .stage-dot { width: 7px; height: 7px; border-radius: 50%; display: inline-block; flex-shrink: 0; }

  .recent-item { display: flex; align-items: center; gap: 12px; padding: 9px 0; border-bottom: 0.5px solid var(--border-light); }
  .recent-item:last-child { border: none; padding-bottom: 0; }
  .avatar {
    width: 32px; height: 32px; border-radius: 50%; background: var(--accent-light); color: var(--accent-dark);
    display: flex; align-items: center; justify-content: center; font-size: 11px; font-weight: 700; flex-shrink: 0;
  }
  .recent-info { flex: 1; min-width: 0; }
  .recent-name { font-size: 12px; font-weight: 600; color: var(--text-primary); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
  .recent-sub { font-size: 11px; color: var(--text-secondary); display: flex; align-items: center; gap: 4px; }
  .recent-val { font-size: 12px; font-weight: 700; color: var(--accent); white-space: nowrap; }

  /* ── Modal ── */
  .modal-bg {
    position: fixed; inset: 0; background: rgba(0,0,0,0.32); display: none;
    align-items: center; justify-content: center; z-index: 200; padding: 20px;
  }
  .modal-bg.open { display: flex; }
  .modal {
    background: var(--bg-primary); border-radius: var(--radius-lg);
    border: 0.5px solid var(--border-light); box-shadow: var(--shadow-md);
    width: 100%; max-width: 560px; max-height: 92vh; overflow-y: auto;
    animation: slideUp 0.18s ease;
  }
  @keyframes slideUp { from { transform: translateY(12px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
  .modal-header {
    padding: 16px 20px; border-bottom: 0.5px solid var(--border-light);
    display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0;
    background: var(--bg-primary); z-index: 1;
  }
  .modal-title { font-size: 15px; font-weight: 600; }
  .modal-body { padding: 20px; display: flex; flex-direction: column; gap: 14px; }
  .modal-footer {
    padding: 14px 20px; border-top: 0.5px solid var(--border-light);
    display: flex; gap: 8px; justify-content: flex-end; position: sticky; bottom: 0;
    background: var(--bg-primary);
  }
  .close-btn { background: none; border: none; cursor: pointer; color: var(--text-secondary); font-size: 22px; line-height: 1; padding: 0 2px; }
  .close-btn:hover { color: var(--text-primary); }

  /* ── Form Elements ── */
  .field-label { font-size: 11px; font-weight: 600; color: var(--text-secondary); margin-bottom: 5px; text-transform: uppercase; letter-spacing: 0.04em; }
  .field-row { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .field-row-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 12px; }
  input[type=text], input[type=number], input[type=date], select, textarea {
    width: 100%; padding: 8px 10px; border: 0.5px solid var(--border-mid);
    border-radius: var(--radius-md); font-size: 13px;
    background: var(--bg-primary); color: var(--text-primary);
    font-family: inherit; transition: border-color 0.15s;
  }
  input:focus, select:focus, textarea:focus { outline: none; border-color: var(--accent); box-shadow: 0 0 0 2px rgba(24,95,165,0.12); }
  textarea { resize: vertical; min-height: 70px; }

  .btn {
    padding: 7px 16px; border-radius: var(--radius-md); font-size: 13px; font-weight: 500;
    cursor: pointer; border: 0.5px solid var(--border-mid); background: var(--bg-primary);
    color: var(--text-primary); transition: all 0.15s; display: inline-flex; align-items: center; gap: 6px;
  }
  .btn:hover { background: var(--bg-secondary); }
  .btn-primary { background: var(--accent); color: #fff; border-color: var(--accent); }
  .btn-primary:hover { background: var(--accent-dark); border-color: var(--accent-dark); }
  .btn-danger { color: var(--danger); border-color: #F09595; }
  .btn-danger:hover { background: var(--danger-bg); }
  .btn-sm { padding: 4px 10px; font-size: 12px; }
  .btn-ghost { border-color: transparent; background: transparent; }
  .btn-ghost:hover { background: var(--bg-secondary); border-color: transparent; }

  /* ── File Area ── */
  .file-drop {
    border: 1.5px dashed var(--border-mid); border-radius: var(--radius-md);
    padding: 18px; text-align: center; color: var(--text-tertiary); cursor: pointer;
    transition: all 0.15s;
  }
  .file-drop:hover { background: var(--bg-secondary); color: var(--text-secondary); border-color: var(--accent); }
  .file-drop i { font-size: 24px; display: block; margin-bottom: 4px; }
  .file-list { display: flex; flex-direction: column; gap: 5px; margin-top: 8px; }
  .file-item {
    display: flex; align-items: center; gap: 8px; padding: 7px 10px;
    background: var(--bg-secondary); border-radius: var(--radius-md); border: 0.5px solid var(--border-light);
  }
  .file-item i { font-size: 14px; color: var(--text-tertiary); }
  .file-name { flex: 1; font-size: 12px; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
  .file-size { font-size: 10px; color: var(--text-tertiary); white-space: nowrap; }

  /* ── Type combo row ── */
  .type-row { display: flex; gap: 6px; align-items: center; }
  .type-row select { flex: 1; }

  /* ── Stage color picker ── */
  .color-swatches { display: flex; gap: 8px; flex-wrap: wrap; }
  .color-swatch {
    width: 26px; height: 26px; border-radius: 50%; cursor: pointer;
    border: 2px solid transparent; transition: transform 0.12s, border-color 0.12s;
  }
  .color-swatch:hover { transform: scale(1.15); }
  .color-swatch.selected { border-color: var(--text-primary); }

  /* ── Stage history timeline ── */
  .stage-timeline { display: flex; flex-direction: column; gap: 6px; }
  .timeline-item { display: flex; align-items: center; gap: 10px; font-size: 12px; }
  .timeline-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .timeline-label { color: var(--text-secondary); flex: 1; }
  .timeline-days { color: var(--text-tertiary); font-size: 11px; }

  /* ── Detail stats row ── */
  .detail-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .detail-stat { background: var(--bg-secondary); border-radius: var(--radius-md); padding: 10px 12px; }
  .detail-stat-label { font-size: 10px; color: var(--text-tertiary); margin-bottom: 3px; text-transform: uppercase; letter-spacing: 0.04em; }
  .detail-stat-value { font-size: 20px; font-weight: 700; color: var(--text-primary); }

  /* ── Empty state ── */
  .empty { padding: 32px 16px; text-align: center; color: var(--text-tertiary); font-size: 13px; }

  /* ── Scrollbar ── */
  ::-webkit-scrollbar { width: 6px; height: 6px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: var(--border-mid); border-radius: 20px; }

  /* ── Section title ── */
  .section-divider { border: none; border-top: 0.5px solid var(--border-light); margin: 2px 0; }

  /* ── Calendar View ── */
  .cal-wrap { display: flex; gap: 0; height: calc(100vh - 52px); overflow: hidden; }

  /* LEFT — Appointment List */
  .cal-list-pane {
    flex: 1; display: flex; flex-direction: column; overflow: hidden;
    border-right: 0.5px solid var(--border-light);
  }
  .cal-list-header {
    padding: 14px 20px 10px; background: var(--bg-primary);
    border-bottom: 0.5px solid var(--border-light); flex-shrink: 0;
    display: flex; align-items: center; justify-content: space-between; gap: 10px;
  }
  .cal-list-date-title { font-size: 16px; font-weight: 700; color: var(--text-primary); }
  .cal-list-body { flex: 1; overflow-y: auto; padding: 16px 20px; }
  .appt-item {
    background: var(--bg-primary); border: 0.5px solid var(--border-light);
    border-left: 3px solid var(--accent); border-radius: var(--radius-md);
    padding: 11px 14px; margin-bottom: 10px; cursor: pointer;
    transition: box-shadow 0.15s, border-color 0.15s;
  }
  .appt-item:hover { box-shadow: var(--shadow-sm); border-left-color: var(--accent-dark); }
  .appt-time-badge {
    font-size: 11px; font-weight: 700; color: var(--accent);
    background: var(--accent-light); padding: 2px 8px; border-radius: 20px;
    display: inline-flex; align-items: center; gap: 4px; margin-bottom: 6px;
  }
  .appt-subject { font-size: 13px; font-weight: 600; color: var(--text-primary); margin-bottom: 3px; }
  .appt-client { font-size: 11px; color: var(--text-secondary); display: flex; align-items: center; gap: 4px; }
  .appt-detail-text { font-size: 11px; color: var(--text-tertiary); margin-top: 4px; white-space: pre-wrap; }

  /* RIGHT — Mini Calendar */
  .cal-right-pane {
    width: 300px; flex-shrink: 0; background: var(--bg-primary);
    display: flex; flex-direction: column; padding: 16px;
  }
  .mini-cal { user-select: none; }
  .mini-cal-header {
    display: flex; align-items: center; justify-content: space-between;
    margin-bottom: 12px;
  }
  .mini-cal-title { font-size: 14px; font-weight: 700; color: var(--text-primary); }
  .mini-cal-nav {
    width: 28px; height: 28px; border-radius: var(--radius-sm); border: 0.5px solid var(--border-light);
    background: var(--bg-primary); cursor: pointer; display: flex; align-items: center;
    justify-content: center; color: var(--text-secondary); font-size: 14px; transition: all 0.15s;
  }
  .mini-cal-nav:hover { background: var(--bg-secondary); color: var(--text-primary); }
  .mini-cal-grid { display: grid; grid-template-columns: repeat(7,1fr); gap: 2px; }
  .mini-cal-dow {
    text-align: center; font-size: 10px; font-weight: 600; color: var(--text-tertiary);
    padding: 4px 0; text-transform: uppercase;
  }
  .mini-cal-day {
    text-align: center; padding: 5px 2px; font-size: 12px; border-radius: 50%;
    cursor: pointer; color: var(--text-primary); transition: all 0.12s; line-height: 1.6;
    width: 30px; height: 30px; display: flex; align-items: center; justify-content: center;
    margin: auto;
  }
  .mini-cal-day:hover:not(.empty-day) { background: var(--bg-secondary); }
  .mini-cal-day.other-month { color: var(--text-tertiary); }
  .mini-cal-day.today { background: var(--accent); color: #fff; font-weight: 700; }
  .mini-cal-day.selected:not(.today) { background: var(--accent-light); color: var(--accent-dark); font-weight: 600; border: 1.5px solid var(--accent); }
  .mini-cal-day.has-appt:not(.today) { color: var(--danger); font-weight: 700; }
  .mini-cal-day.has-appt.today { background: var(--accent); color: #fff; box-shadow: 0 0 0 2px var(--danger); }
  .empty-day { cursor: default; }

  /* Card appointment list inside card modal */
  .card-appt-list { display: flex; flex-direction: column; gap: 6px; }
  .card-appt-row {
    display: flex; align-items: center; gap: 10px; padding: 8px 10px;
    background: var(--bg-secondary); border-radius: var(--radius-md);
    border: 0.5px solid var(--border-light); cursor: pointer; transition: box-shadow 0.15s;
  }
  .card-appt-row:hover { box-shadow: var(--shadow-sm); }
  .card-appt-date { font-size: 11px; font-weight: 700; color: var(--accent); white-space: nowrap; }
  .card-appt-subject { flex: 1; font-size: 12px; font-weight: 500; color: var(--text-primary); overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
</style>
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2/dist/umd/supabase.min.js"></script>
<script>
// ════════════════════════════════════════════════════════════════
//  ⚙️  SUPABASE CONFIG — แก้ไขค่านี้ก่อนใช้งาน
//  คัดลอกจาก Supabase Dashboard → Project Settings → API
// ════════════════════════════════════════════════════════════════
window.__CRM_CONFIG__ = {
  supabaseUrl: "https://iemrnckfixeajpyabinj.supabase.co",   // ← แก้ตรงนี้
  supabaseKey: "sb_publishable_3ejtp8-FSNgPWYdDNZ58pg_pP-RFP_e",                  // ← แก้ตรงนี้
};
</script>
</head>
<body>

<div id="app">
  <div class="topbar">
    <div class="logo"><div class="logo-dot"></div> SalesCRM</div>
    <div class="nav-tabs">
      <button class="nav-tab" id="tab-calendar" onclick="switchView('calendar')" title="ปฏิทินนัดหมาย">
        <i class="ti ti-calendar-event"></i> Calendar
      </button>
      <button class="nav-tab active" id="tab-pipeline" onclick="switchView('pipeline')">
        <i class="ti ti-layout-kanban"></i> Pipeline
      </button>
      <button class="nav-tab" id="tab-dashboard" onclick="switchView('dashboard')">
        <i class="ti ti-chart-bar"></i> Dashboard
      </button>
    </div>
    <div class="topbar-right">
      <button class="topbar-btn" onclick="openAddStage()"><i class="ti ti-layout-columns"></i> เพิ่ม Stage</button>
      <button class="topbar-btn primary" onclick="openNewCard(state.stages[0].id)"><i class="ti ti-plus"></i> เพิ่มงาน</button>
    </div>
  </div>
  <div class="content" id="main-content"></div>
</div>

<!-- Modal -->
<div class="modal-bg" id="modal-bg" onclick="handleModalBgClick(event)">
  <div class="modal" id="modal-box"></div>
</div>

<!-- Hidden file input -->
<input type="file" id="file-input" multiple style="display:none">

<script>
// ════════════════════════════════════════════════════════════════
//  SUPABASE DB LAYER
//  เชื่อมต่อ Supabase (PostgREST) โดยตรงจาก frontend
//  ไม่ผ่าน backend /db/ endpoints อีกต่อไป
// ════════════════════════════════════════════════════════════════
let _sb = null;
function getSB() {
  if (!_sb) {
    const cfg = window.__CRM_CONFIG__ || {};
    const url = cfg.supabaseUrl || '';
    const key = cfg.supabaseKey || '';
    if (!url || url.includes('your-project-id') || !key || key.includes('your-anon'))
      throw new Error('กรุณาแก้ไข supabaseUrl และ supabaseKey ใน &lt;script&gt; CONFIG ด้านบนของไฟล์ HTML ก่อน');
    _sb = supabase.createClient(url, key);
  }
  return _sb;
}

const DB = {
  // ── Cards ──────────────────────────────────────────────────────
  async insertCard(c) {
    const sb = getSB();
    const { error: e1 } = await sb.from('cards').insert({
      id: c.id, stage_id: c.stageId, title: c.title,
      salesperson: c.salesperson || null, job_title: c.jobTitle || null,
      value: c.value || 0, cost: c.cost || 0,
      job_type: c.jobType || null,
      start_date: c.startDate || null, end_date: c.endDate || null,
      remark: c.remark || null,
    });
    if (e1) throw new Error(e1.message);
    if (c.stageHistory?.length) {
      const { error: e2 } = await sb.from('stage_history').insert(
        c.stageHistory.map(h => ({ card_id: c.id, stage_id: h.stageId, entered_at: h.enteredAt }))
      );
      if (e2) throw new Error(e2.message);
    }
    if (c.files?.length) {
      const { error: e3 } = await sb.from('card_files').insert(
        c.files.map(f => ({ card_id: c.id, file_name: f.name, file_type: f.type, file_size: f.size, file_data: f.data }))
      );
      if (e3) throw new Error(e3.message);
    }
  },

  async updateCard(c) {
    const sb = getSB();
    const { error: e1 } = await sb.from('cards').update({
      stage_id: c.stageId, title: c.title,
      salesperson: c.salesperson || null, job_title: c.jobTitle || null,
      value: c.value || 0, cost: c.cost || 0,
      job_type: c.jobType || null,
      start_date: c.startDate || null, end_date: c.endDate || null,
      remark: c.remark || null,
      updated_at: new Date().toISOString(),
    }).eq('id', c.id);
    if (e1) throw new Error(e1.message);
    // replace history
    await sb.from('stage_history').delete().eq('card_id', c.id);
    if (c.stageHistory?.length) {
      const { error: e2 } = await sb.from('stage_history').insert(
        c.stageHistory.map(h => ({ card_id: c.id, stage_id: h.stageId, entered_at: h.enteredAt }))
      );
      if (e2) throw new Error(e2.message);
    }
    // replace files
    await sb.from('card_files').delete().eq('card_id', c.id);
    if (c.files?.length) {
      const { error: e3 } = await sb.from('card_files').insert(
        c.files.map(f => ({ card_id: c.id, file_name: f.name, file_type: f.type, file_size: f.size, file_data: f.data }))
      );
      if (e3) throw new Error(e3.message);
    }
  },

  async deleteCard(id) {
    const { error } = await getSB().from('cards').delete().eq('id', id);
    if (error) throw new Error(error.message);
  },

  // ── Stages ─────────────────────────────────────────────────────
  async insertStage(s) {
    const sb = getSB();
    const { data: mx } = await sb.from('stages').select('sort_order').order('sort_order', { ascending: false }).limit(1);
    const nextOrder = mx?.length ? mx[0].sort_order + 1 : 1;
    const { error } = await sb.from('stages').insert({ id: s.id, name: s.name, color: s.color, sort_order: nextOrder });
    if (error) throw new Error(error.message);
  },

  async updateStage(id, name, color) {
    const { error } = await getSB().from('stages').update({ name, color }).eq('id', id);
    if (error) throw new Error(error.message);
  },

  async deleteStage(id) {
    const { error } = await getSB().from('stages').delete().eq('id', id);
    if (error) throw new Error(error.message);
  },

  // ── Job Types ──────────────────────────────────────────────────
  async insertJobType(name) {
    const { error } = await getSB().from('job_types').upsert({ name }, { onConflict: 'name', ignoreDuplicates: true });
    if (error) throw new Error(error.message);
  },

  // ── Appointments ───────────────────────────────────────────────
  async loadAppointments() {
    const { data, error } = await getSB()
      .from('appointments').select('*').order('appt_date').order('appt_time');
    if (error) throw new Error(error.message);
    return data || [];
  },
  async insertAppointment(a) {
    const { data, error } = await getSB().from('appointments').insert({
      card_id: a.cardId || null, card_title: a.cardTitle || null,
      appt_date: a.apptDate, appt_time: a.apptTime,
      subject: a.subject, detail: a.detail || null,
    }).select().single();
    if (error) throw new Error(error.message);
    return data;
  },
  async updateAppointment(id, a) {
    const { error } = await getSB().from('appointments').update({
      card_id: a.cardId || null, card_title: a.cardTitle || null,
      appt_date: a.apptDate, appt_time: a.apptTime,
      subject: a.subject, detail: a.detail || null,
      updated_at: new Date().toISOString(),
    }).eq('id', id);
    if (error) throw new Error(error.message);
  },
  async deleteAppointment(id) {
    const { error } = await getSB().from('appointments').delete().eq('id', id);
    if (error) throw new Error(error.message);
  },
};

// ── UI helpers ────────────────────────────────────────────────────────────────
function showToast(msg, isErr) {
  let t = document.getElementById('_toast');
  if (!t) {
    t = document.createElement('div');
    t.id = '_toast';
    t.style.cssText = [
      'position:fixed;bottom:24px;right:24px;z-index:9999',
      'padding:9px 18px;border-radius:8px;font-size:13px;font-weight:500',
      'box-shadow:0 4px 16px rgba(0,0,0,.15);transition:opacity .35s',
    ].join(';');
    document.body.appendChild(t);
  }
  t.textContent = msg;
  t.style.background = isErr ? '#A32D2D' : '#0F6E56';
  t.style.color = '#fff'; t.style.opacity = '1';
  clearTimeout(t._to);
  t._to = setTimeout(() => { t.style.opacity = '0'; }, 3200);
}

function setBusy(on) {
  let el = document.getElementById('_busy');
  if (!el) {
    el = document.createElement('div');
    el.id = '_busy';
    el.innerHTML = '<i class="ti ti-loader-2"></i> กำลังบันทึก...';
    el.style.cssText = [
      'position:fixed;top:56px;right:20px;z-index:999',
      'background:#185FA5;color:#fff;padding:5px 14px',
      'border-radius:8px;font-size:12px;display:none;align-items:center;gap:6px',
    ].join(';');
    const sty = document.createElement('style');
    sty.textContent = '#_busy i{animation:_spin .8s linear infinite}@keyframes _spin{to{transform:rotate(360deg)}}';
    document.head.appendChild(sty);
    document.body.appendChild(el);
  }
  el.style.display = on ? 'flex' : 'none';
}

// ════════════════════════════════════════════════════════════════
//  STATE  (โหลดจาก BOONKONG/CRM69 ตอน init)
// ════════════════════════════════════════════════════════════════
const STAGE_COLORS = ['#185FA5','#0F6E56','#BA7517','#993C1D','#533AB7','#993556','#639922','#888780','#E24B4A','#1D9E75'];

let state = {
  view: 'pipeline',
  stages:       [],
  cards:        [],
  jobTypes:     [],
  appointments: [],
  dragCardId:   null,
  nextId:       100,
  selectedColor: STAGE_COLORS[0],
  searchQuery:  '',
  calDate:      new Date(),          // วันที่ที่เลือกใน calendar
  calViewMonth: new Date(),          // เดือนที่แสดงใน mini-calendar
};

let _editingCard = null;

// ── Helpers ──────────────────────────────────────────────────────────────────

function cardsInStage(stageId) { return state.cards.filter(c => c.stageId === stageId); }

function getDaysInStage(card) {
  const h = card.stageHistory;
  if (!h || !h.length) return 0;
  return Math.floor((Date.now() - h[h.length-1].enteredAt) / 86400000);
}

function getTotalDays(card) {
  const h = card.stageHistory;
  if (!h || !h.length) return 0;
  return Math.floor((Date.now() - h[0].enteredAt) / 86400000);
}

function avgDaysInStage(stageId) {
  const cs = cardsInStage(stageId);
  if (!cs.length) return 0;
  return Math.round(cs.reduce((a, c) => a + getDaysInStage(c), 0) / cs.length);
}

function fmt(n) { return Number(n).toLocaleString('th-TH'); }
function fmtM(n) { return (n / 1000).toFixed(0) + 'K'; }

function genId() { return 'x' + (state.nextId++); }

function stageName(id) {
  const s = state.stages.find(s => s.id === id);
  return s ? s.name : id;
}

function stageColor(id) {
  const s = state.stages.find(s => s.id === id);
  return s ? s.color : '#888';
}

// ── Render ────────────────────────────────────────────────────────────────────

function render() {
  const el = document.getElementById('main-content');
  if (state.view === 'calendar') {
    el.style.padding = '0';
    el.innerHTML = renderCalendar();
  } else {
    el.style.padding = '';
    el.innerHTML = state.view === 'pipeline' ? renderPipeline() : renderDashboard();
    if (state.view === 'pipeline') bindDragEvents();
  }
}

function switchView(v) {
  state.view = v;
  document.getElementById('tab-calendar').classList.toggle('active',  v === 'calendar');
  document.getElementById('tab-pipeline').classList.toggle('active',  v === 'pipeline');
  document.getElementById('tab-dashboard').classList.toggle('active', v === 'dashboard');
  render();
}

// ══════════════════════════════════════════════════════════════════
// CALENDAR VIEW
// ══════════════════════════════════════════════════════════════════

function toDateStr(d) {
  return d.getFullYear() + '-' +
    String(d.getMonth()+1).padStart(2,'0') + '-' +
    String(d.getDate()).padStart(2,'0');
}

function fmtDateThai(dateStr) {
  if (!dateStr) return '';
  const d = new Date(dateStr + 'T00:00:00');
  return d.toLocaleDateString('th-TH', { weekday:'short', day:'numeric', month:'long', year:'numeric' });
}

function fmtTimeThai(timeStr) {
  if (!timeStr) return '';
  return timeStr.substring(0,5);
}

function apptDates() {
  const s = new Set();
  state.appointments.forEach(a => s.add(a.appt_date));
  return s;
}

function apptsForDate(dateStr) {
  return state.appointments
    .filter(a => a.appt_date === dateStr)
    .sort((a,b) => a.appt_time.localeCompare(b.appt_time));
}

function renderCalendar() {
  const selStr = toDateStr(state.calDate);
  const appts  = apptsForDate(selStr);
  const datesWithAppt = apptDates();

  // mini calendar
  const vm   = state.calViewMonth;
  const year = vm.getFullYear();
  const mon  = vm.getMonth();
  const firstDay = new Date(year, mon, 1).getDay();
  const daysInMonth = new Date(year, mon+1, 0).getDate();
  const todayStr = toDateStr(new Date());
  const DOWS = ['อา','จ','อ','พ','พฤ','ศ','ส'];
  const MONTHS_TH = ['มกราคม','กุมภาพันธ์','มีนาคม','เมษายน','พฤษภาคม','มิถุนายน',
                     'กรกฎาคม','สิงหาคม','กันยายน','ตุลาคม','พฤศจิกายน','ธันวาคม'];

  let calCells = '';
  // blank cells
  for (let i = 0; i < firstDay; i++) calCells += `<div class="mini-cal-day empty-day other-month"></div>`;
  for (let d = 1; d <= daysInMonth; d++) {
    const dStr = year + '-' + String(mon+1).padStart(2,'0') + '-' + String(d).padStart(2,'0');
    const isToday    = dStr === todayStr;
    const isSelected = dStr === selStr;
    const hasAppt    = datesWithAppt.has(dStr);
    let cls = 'mini-cal-day';
    if (isToday)    cls += ' today';
    else if (isSelected) cls += ' selected';
    if (hasAppt)    cls += ' has-appt';
    calCells += `<div class="${cls}" onclick="calSelectDate('${dStr}')">${d}</div>`;
  }

  return `<div class="cal-wrap">
    <!-- LEFT: Appointment list -->
    <div class="cal-list-pane">
      <div class="cal-list-header">
        <div>
          <div class="cal-list-date-title">${fmtDateThai(selStr)}</div>
          <div style="font-size:11px;color:var(--text-tertiary);margin-top:2px">${appts.length} นัดหมาย</div>
        </div>
        <button class="btn btn-primary btn-sm" onclick="openApptForm(null,'${selStr}')">
          <i class="ti ti-plus"></i> เพิ่มนัดหมาย
        </button>
      </div>
      <div class="cal-list-body">
        ${appts.length ? appts.map(a => `
          <div class="appt-item" onclick="openApptForm(${a.id})">
            <div class="appt-time-badge"><i class="ti ti-clock" style="font-size:10px"></i>${fmtTimeThai(a.appt_time)} น.</div>
            <div class="appt-subject">${escHtml(a.subject)}</div>
            ${a.card_title ? `<div class="appt-client"><i class="ti ti-building" style="font-size:10px"></i>${escHtml(a.card_title)}</div>` : ''}
            ${a.detail ? `<div class="appt-detail-text">${escHtml(a.detail.substring(0,80))}${a.detail.length>80?'…':''}</div>` : ''}
          </div>`).join('') :
          `<div class="empty" style="margin-top:40px">
            <i class="ti ti-calendar-off" style="font-size:36px;display:block;margin-bottom:10px"></i>
            ไม่มีนัดหมายในวันนี้
          </div>`}
      </div>
    </div>

    <!-- RIGHT: Mini calendar -->
    <div class="cal-right-pane">
      <div class="mini-cal">
        <div class="mini-cal-header">
          <button class="mini-cal-nav" onclick="calPrevMonth()"><i class="ti ti-chevron-left"></i></button>
          <div class="mini-cal-title">${MONTHS_TH[mon]} ${year + 543}</div>
          <button class="mini-cal-nav" onclick="calNextMonth()"><i class="ti ti-chevron-right"></i></button>
        </div>
        <div class="mini-cal-grid">
          ${DOWS.map(d => `<div class="mini-cal-dow">${d}</div>`).join('')}
          ${calCells}
        </div>
      </div>
      <div style="margin-top:20px;padding-top:14px;border-top:0.5px solid var(--border-light)">
        <div style="font-size:11px;font-weight:600;color:var(--text-secondary);margin-bottom:8px">สัญลักษณ์</div>
        <div style="display:flex;flex-direction:column;gap:6px;font-size:11px;color:var(--text-secondary)">
          <div style="display:flex;align-items:center;gap:8px">
            <div style="width:22px;height:22px;border-radius:50%;background:var(--accent);display:flex;align-items:center;justify-content:center;color:#fff;font-size:10px;font-weight:700">8</div>
            <span>วันนี้</span>
          </div>
          <div style="display:flex;align-items:center;gap:8px">
            <div style="width:22px;height:22px;border-radius:50%;background:var(--accent-light);border:1.5px solid var(--accent);display:flex;align-items:center;justify-content:center;color:var(--accent-dark);font-size:10px;font-weight:700">8</div>
            <span>วันที่เลือก</span>
          </div>
          <div style="display:flex;align-items:center;gap:8px">
            <div style="width:22px;height:22px;border-radius:50%;display:flex;align-items:center;justify-content:center;color:var(--danger);font-size:10px;font-weight:700">8</div>
            <span>มีนัดหมาย</span>
          </div>
        </div>
      </div>
    </div>
  </div>`;
}

function calSelectDate(dateStr) {
  state.calDate = new Date(dateStr + 'T00:00:00');
  // ถ้าเดือนต่างกัน ให้ sync calViewMonth ด้วย
  if (state.calDate.getMonth() !== state.calViewMonth.getMonth() ||
      state.calDate.getFullYear() !== state.calViewMonth.getFullYear()) {
    state.calViewMonth = new Date(state.calDate.getFullYear(), state.calDate.getMonth(), 1);
  }
  render();
}

function calPrevMonth() {
  const d = state.calViewMonth;
  state.calViewMonth = new Date(d.getFullYear(), d.getMonth()-1, 1);
  render();
}
function calNextMonth() {
  const d = state.calViewMonth;
  state.calViewMonth = new Date(d.getFullYear(), d.getMonth()+1, 1);
  render();
}

// ── Appointment Form Modal ─────────────────────────────────────────────────────
function openApptForm(apptId, defaultDate, fromCardId) {
  const a = apptId ? state.appointments.find(x => x.id === apptId) : null;
  const dateVal = a ? a.appt_date : (defaultDate || toDateStr(state.calDate));
  const timeVal = a ? a.appt_time.substring(0,5) : '09:00';

  // unique client list from cards
  const clientOpts = [...new Map(state.cards.map(c => [c.title, c])).values()]
    .sort((a,b) => a.title.localeCompare(b.title, 'th'))
    .map(c => `<option value="${escHtml(c.id)}" data-title="${escHtml(c.title)}" ${a && a.card_id===c.id?'selected':''}>${escHtml(c.title)}</option>`)
    .join('');

  const backBtn = fromCardId
    ? '<button class="btn btn-sm" onclick="closeModal();setTimeout(function(){openCardDetail(\'' + fromCardId + '\')},60)" style="padding:4px 10px;font-size:11px;flex-shrink:0"><i class=\"ti ti-arrow-left\"></i> กลับ Card</button>'
    : '';
  showModal(`
    <div class="modal-header">
      <div style="display:flex;align-items:center;gap:8px;flex:1;min-width:0">
        ${backBtn}
        <span class="modal-title" style="flex:1">${a ? 'แก้ไขนัดหมาย' : 'เพิ่มนัดหมาย'}</span>
      </div>
      <button class="close-btn" onclick="closeModal()">×</button>
    </div>
    <div class="modal-body">
      <div>
        <div class="field-label">ลูกค้า / บริษัท</div>
        <input type="text" id="appt-client-search" placeholder="ค้นหาชื่อลูกค้า..."
          oninput="filterApptClients(this.value)"
          value="${a ? escHtml(a.card_title||'') : ''}"
          style="margin-bottom:6px">
        <select id="appt-card-id" size="4"
          style="width:100%;border-radius:var(--radius-md);font-size:12px;padding:4px"
          onchange="syncApptClientSearch(this)">
          <option value="">— ไม่ระบุ —</option>
          ${clientOpts}
        </select>
      </div>
      <div class="field-row">
        <div>
          <div class="field-label">วันที่นัดหมาย</div>
          <input type="date" id="appt-date" value="${dateVal}">
        </div>
        <div>
          <div class="field-label">เวลานัดหมาย</div>
          <input type="time" id="appt-time" value="${timeVal}">
        </div>
      </div>
      <div>
        <div class="field-label">หัวข้อนัดหมาย *</div>
        <input type="text" id="appt-subject" value="${a ? escHtml(a.subject) : ''}" placeholder="เช่น นำเสนอโครงการ, ประชุมติดตามงาน...">
      </div>
      <div>
        <div class="field-label">รายละเอียด</div>
        <textarea id="appt-detail" rows="4" placeholder="รายละเอียดเพิ่มเติม...">${a ? escHtml(a.detail||'') : ''}</textarea>
      </div>
    </div>
    <div class="modal-footer">
      ${a ? `<button class="btn btn-danger" onclick="deleteAppt(${a.id})"><i class="ti ti-trash"></i> ลบ</button>` : ''}
      <button class="btn" onclick="closeModal()">ยกเลิก</button>
      <button class="btn btn-primary" onclick="saveAppt(${a ? a.id : 'null'})"><i class="ti ti-check"></i> บันทึก</button>
    </div>`);
}

function filterApptClients(q) {
  const sel = document.getElementById('appt-card-id');
  if (!sel) return;
  Array.from(sel.options).forEach(opt => {
    opt.style.display = (!q || opt.text.toLowerCase().includes(q.toLowerCase())) ? '' : 'none';
  });
}

function syncApptClientSearch(sel) {
  const opt = sel.options[sel.selectedIndex];
  const inp = document.getElementById('appt-client-search');
  if (inp && opt && opt.value) inp.value = opt.getAttribute('data-title') || '';
}

async function saveAppt(apptId) {
  const subject = document.getElementById('appt-subject').value.trim();
  if (!subject) { alert('กรุณาระบุหัวข้อนัดหมาย'); return; }
  const sel = document.getElementById('appt-card-id');
  const selectedOpt = sel.options[sel.selectedIndex];
  const cardId    = sel.value || null;
  const cardTitle = cardId ? (selectedOpt.getAttribute('data-title') || selectedOpt.text) : null;
  const payload = {
    cardId, cardTitle,
    apptDate: document.getElementById('appt-date').value,
    apptTime: document.getElementById('appt-time').value + ':00',
    subject,
    detail: document.getElementById('appt-detail').value.trim() || null,
  };
  setBusy(true);
  try {
    if (apptId) {
      await DB.updateAppointment(apptId, payload);
      const idx = state.appointments.findIndex(a => a.id === apptId);
      if (idx >= 0) state.appointments[idx] = { ...state.appointments[idx],
        card_id: payload.cardId, card_title: payload.cardTitle,
        appt_date: payload.apptDate, appt_time: payload.apptTime,
        subject: payload.subject, detail: payload.detail };
      showToast('✅ บันทึกนัดหมายสำเร็จ');
    } else {
      const saved = await DB.insertAppointment(payload);
      state.appointments.push(saved);
      state.calDate = new Date(payload.apptDate + 'T00:00:00');
      showToast('✅ เพิ่มนัดหมายสำเร็จ');
    }
    closeModal();
    if (state.view === 'calendar') render();
  } catch(e) { showToast('❌ ' + e.message, true); }
  finally { setBusy(false); }
}

async function deleteAppt(apptId) {
  if (!confirm('ลบนัดหมายนี้?')) return;
  setBusy(true);
  try {
    await DB.deleteAppointment(apptId);
    state.appointments = state.appointments.filter(a => a.id !== apptId);
    closeModal();
    showToast('✅ ลบนัดหมายสำเร็จ');
    if (state.view === 'calendar') render();
  } catch(e) { showToast('❌ ' + e.message, true); }
  finally { setBusy(false); }
}

// ── Pipeline ─────────────────────────────────────────────────────────────────

function renderPipeline() {
  return `<div style="display:flex;flex-direction:column;height:100%">
    <div style="display:flex;justify-content:center;padding:10px 20px 6px;background:var(--bg-primary);border-bottom:1px solid var(--border-light);flex-shrink:0">
      <div style="position:relative;width:320px">
        <i class="ti ti-search" style="position:absolute;left:10px;top:50%;transform:translateY(-50%);color:var(--text-tertiary);font-size:14px;pointer-events:none"></i>
        <input
          type="text"
          id="pipeline-search"
          placeholder="ค้นหาชื่อลูกค้า..."
          value="${state.searchQuery}"
          oninput="state.searchQuery=this.value;renderPipelineCards()"
          style="width:100%;padding:7px 10px 7px 32px;border:1px solid var(--border);border-radius:8px;font-size:13px;background:var(--bg-secondary);color:var(--text-primary);box-sizing:border-box;outline:none"
        >
        ${state.searchQuery ? `<button onclick="state.searchQuery='';render()" style="position:absolute;right:8px;top:50%;transform:translateY(-50%);background:none;border:none;cursor:pointer;color:var(--text-tertiary);font-size:16px;line-height:1;padding:0">×</button>` : ''}
      </div>
    </div>
    <div class="pipeline-view" id="pipeline-view">
      ${state.stages.map(s => renderStageCol(s)).join('')}
      <button class="add-stage-col" onclick="openAddStage()">
        <i class="ti ti-plus"></i> เพิ่ม Stage
      </button>
    </div>
  </div>`;
}

function renderPipelineCards() {
  // re-render เฉพาะ card ในแต่ละ stage โดยไม่ rebuild ทั้งหน้า
  state.stages.forEach(s => {
    const body = document.getElementById('body-' + s.id);
    if (!body) return;
    const cards = cardsInStageFiltered(s.id);
    body.innerHTML = cards.map(c => renderCard(c, s)).join('') +
      `<button class="add-card-btn" onclick="openNewCard('${s.id}')"><i class="ti ti-plus"></i> เพิ่มงาน</button>`;
  });
  bindDragEvents();
}

function cardsInStageFiltered(stageId) {
  const q = state.searchQuery.trim().toLowerCase();
  return state.cards.filter(c => c.stageId === stageId &&
    (!q || c.title.toLowerCase().includes(q) || (c.salesperson||'').toLowerCase().includes(q)));
}

function renderStageCol(s) {
  const cards = cardsInStageFiltered(s.id);
  const allCards = cardsInStage(s.id);
  const avg = avgDaysInStage(s.id);
  const canDelete = allCards.length === 0;
  return `<div class="stage-col" data-stage="${s.id}">
    <div class="stage-header" style="border-top:3px solid ${s.color}">
      <div style="flex:1;min-width:0">
        <div class="stage-name">${s.name}</div>
        <div class="stage-meta"><i class="ti ti-clock" style="font-size:10px"></i> เฉลี่ย ${avg} วัน</div>
      </div>
      <div class="stage-header-right">
        <span class="stage-count">${state.searchQuery ? cards.length + '/' + allCards.length : allCards.length}</span>
        <button class="stage-action-btn" onclick="event.stopPropagation();openEditStage('${s.id}')" title="แก้ไขชื่อ Stage">
          <i class="ti ti-pencil"></i>
        </button>
        <button class="stage-action-btn danger" onclick="event.stopPropagation();deleteStage('${s.id}')"
          title="${canDelete ? 'ลบ Stage' : 'ไม่สามารถลบได้ (มีงานอยู่)'}"
          ${canDelete ? '' : 'style="opacity:0.35;cursor:not-allowed"'}
          ${canDelete ? '' : 'disabled'}>
          <i class="ti ti-trash"></i>
        </button>
      </div>
    </div>
    <div class="stage-body" id="body-${s.id}">
      ${cards.map(c => renderCard(c, s)).join('')}
      <button class="add-card-btn" onclick="openNewCard('${s.id}')">
        <i class="ti ti-plus"></i> เพิ่มงาน
      </button>
    </div>
  </div>`;
}

function renderCard(c, s) {
  const days = getDaysInStage(c);
  const total = getTotalDays(c);
  return `<div class="card" draggable="true" data-card="${c.id}" onclick="openCardDetail('${c.id}')">
    <div class="card-title">${c.title}</div>
    <div class="card-meta">
      ${c.salesperson ? `<span><i class="ti ti-user"></i>${c.salesperson}</span>` : ''}
      ${c.jobTitle ? `<span><i class="ti ti-briefcase"></i>${c.jobTitle}</span>` : ''}
    </div>
    ${c.value ? `<div class="card-value">฿${fmt(c.value)}</div>` : ''}
    <div class="card-footer">
      ${c.jobType ? `<span class="type-badge">${c.jobType}</span>` : '<span></span>'}
      <span class="card-days"><i class="ti ti-clock" style="font-size:10px"></i> ${days} วัน · รวม ${total} วัน</span>
    </div>
  </div>`;
}

// ── Drag & Drop ───────────────────────────────────────────────────────────────

function bindDragEvents() {
  document.querySelectorAll('.card').forEach(el => {
    el.addEventListener('dragstart', e => {
      state.dragCardId = el.dataset.card;
      setTimeout(() => el.classList.add('dragging'), 0);
      e.dataTransfer.effectAllowed = 'move';
    });
    el.addEventListener('dragend', () => {
      el.classList.remove('dragging');
      state.dragCardId = null;
    });
  });
  document.querySelectorAll('.stage-body').forEach(el => {
    el.addEventListener('dragover', e => { e.preventDefault(); el.classList.add('drag-over'); });
    el.addEventListener('dragleave', () => el.classList.remove('drag-over'));
    el.addEventListener('drop', e => {
      e.preventDefault();
      el.classList.remove('drag-over');
      const stageId = el.id.replace('body-', '');
      if (!state.dragCardId) return;
      const card = state.cards.find(c => c.id === state.dragCardId);
      if (card && card.stageId !== stageId) {
        card.stageId = stageId;
        if (!card.stageHistory) card.stageHistory = [];
        card.stageHistory.push({ stageId, enteredAt: Date.now() });
        DB.updateCard(card).then(()=>showToast('✅ ย้าย Stage สำเร็จ')).catch(e=>showToast('❌ '+e.message,true));
      }
      state.dragCardId = null;
      render();
    });
  });
}

// ── Dashboard ─────────────────────────────────────────────────────────────────

function renderDashboard() {
  const total = state.cards.reduce((a, c) => a + (Number(c.value) || 0), 0);

  // คำนวณ "มูลค่าปิดแล้ว" และ "อัตราปิด" จาก Stage ที่ชื่อ "End job"
  const endJobStage = state.stages.find(s => s.name.trim().toLowerCase() === 'end job');
  const endJobId    = endJobStage ? endJobStage.id : null;
  const endJobCards = endJobId ? state.cards.filter(c => c.stageId === endJobId) : [];
  const won         = endJobCards.reduce((a, c) => a + (Number(c.value) || 0), 0);
  const winRate     = state.cards.length ? Math.round(endJobCards.length / state.cards.length * 100) : 0;
  const closedCost  = endJobCards.reduce((a, c) => a + (Number(c.cost) || 0), 0);
  const netProfit   = won - closedCost;
  const costRate    = won > 0 ? (closedCost * 100 / won).toFixed(1) : '0.0';

  const avgTotal = state.cards.length ? Math.round(state.cards.reduce((a, c) => a + getTotalDays(c), 0) / state.cards.length) : 0;

  const byStage = state.stages.map(s => ({ ...s, count: cardsInStage(s.id).length, val: cardsInStage(s.id).reduce((a, c) => a + (Number(c.value) || 0), 0), avg: avgDaysInStage(s.id) }));
  const maxVal = Math.max(...byStage.map(s => s.val), 1);
  const maxAvg = Math.max(...byStage.map(s => s.avg), 1);

  const bySales = {};
  state.cards.forEach(c => {
    const n = c.salesperson || 'ไม่ระบุ';
    bySales[n] = (bySales[n] || 0) + (Number(c.value) || 0);
  });
  const maxSales = Math.max(...Object.values(bySales), 1);

  // มูลค่างานตามพนักงานขายที่ปิดแล้ว (เฉพาะ Stage End job)
  const bySalesClosed = {};
  endJobCards.forEach(c => {
    const n = c.salesperson || 'ไม่ระบุ';
    bySalesClosed[n] = (bySalesClosed[n] || 0) + (Number(c.value) || 0);
  });
  const bySalesClosedSorted = Object.entries(bySalesClosed).sort((a, b) => b[1] - a[1]);
  const maxSalesClosed = Math.max(...Object.values(bySalesClosed), 1);

  const byType = {};
  state.cards.forEach(c => {
    if (c.jobType) byType[c.jobType] = (byType[c.jobType] || 0) + 1;
  });

  const recentCards = [...state.cards].sort((a, b) => {
    const ah = a.stageHistory; const bh = b.stageHistory;
    return (bh && bh.length ? bh[bh.length-1].enteredAt : 0) - (ah && ah.length ? ah[ah.length-1].enteredAt : 0);
  }).slice(0, 5);

  return `<div>
    <div class="dash-metrics">
      <div class="metric-card accent">
        <div class="metric-label">งานทั้งหมด</div>
        <div class="metric-value">${state.cards.length}</div>
        <div class="metric-sub">โครงการ</div>
      </div>
      <div class="metric-card success">
        <div class="metric-label">มูลค่ารวม</div>
        <div class="metric-value">฿${fmtM(total)}</div>
        <div class="metric-sub">บาท</div>
      </div>
      <div class="metric-card warning">
        <div class="metric-label">มูลค่าปิดแล้ว</div>
        <div class="metric-value">฿${fmtM(won)}</div>
        <div class="metric-sub">บาท</div>
      </div>
      <div class="metric-card danger">
        <div class="metric-label">อัตราปิด</div>
        <div class="metric-value">${winRate}%</div>
        <div class="metric-sub">เฉลี่ย ${avgTotal} วัน/งาน</div>
      </div>
      <div class="metric-card" style="border-top:3px solid #993C1D">
        <div class="metric-label">ค่าใช้จ่ายที่ปิดแล้ว</div>
        <div class="metric-value">฿${fmtM(closedCost)}</div>
        <div class="metric-sub">เฉพาะ End job</div>
      </div>
      <div class="metric-card" style="border-top:3px solid ${netProfit >= 0 ? '#639922' : '#E24B4A'}">
        <div class="metric-label">กำไรสุทธิ</div>
        <div class="metric-value" style="color:${netProfit >= 0 ? 'var(--success)' : 'var(--danger)'}">฿${fmtM(Math.abs(netProfit))}${netProfit < 0 ? ' 📉' : ''}</div>
        <div class="metric-sub">มูลค่าปิด − ค่าใช้จ่าย</div>
      </div>
      <div class="metric-card" style="border-top:3px solid #BA7517">
        <div class="metric-label">อัตราค่าใช้จ่าย</div>
        <div class="metric-value">${costRate}%</div>
        <div class="metric-sub">ค่าใช้จ่าย / มูลค่าปิด</div>
      </div>
    </div>
    <div class="dash-row">
      <div class="dash-card">
        <div class="dash-card-title">มูลค่างานตาม Stage</div>
        ${byStage.map(s => `<div class="bar-row">
          <span class="bar-label"><span class="stage-dot" style="background:${s.color}"></span>${s.name}</span>
          <div class="bar-track"><div class="bar-fill" style="width:${Math.round(s.val/maxVal*100)}%;background:${s.color}"></div></div>
          <span class="bar-val">฿${(s.val/1000).toFixed(0)}K</span>
        </div>`).join('')}
      </div>
      <div class="dash-card">
        <div class="dash-card-title">งานล่าสุด</div>
        ${recentCards.length ? recentCards.map(c => {
          const initials = c.title.replace(/[^\u0E00-\u0E7FA-Za-z\s]/g,'').split(' ').filter(Boolean).slice(0,2).map(w => w[0]).join('').toUpperCase().slice(0,2) || '?';
          return `<div class="recent-item">
            <div class="avatar">${initials}</div>
            <div class="recent-info">
              <div class="recent-name">${c.title}</div>
              <div class="recent-sub"><span class="stage-dot" style="background:${stageColor(c.stageId)}"></span>${stageName(c.stageId)} · ${c.salesperson || '-'}</div>
            </div>
            <span class="recent-val">${c.value ? '฿'+fmt(c.value) : '-'}</span>
          </div>`;
        }).join('') : '<div class="empty">ยังไม่มีงาน</div>'}
      </div>
    </div>
    <div class="dash-row">
      <div class="dash-card">
        <div class="dash-card-title">มูลค่าตามพนักงานขาย</div>
        ${Object.entries(bySales).map(([n, v]) => `<div class="bar-row">
          <span class="bar-label">${n}</span>
          <div class="bar-track"><div class="bar-fill" style="width:${Math.round(v/maxSales*100)}%"></div></div>
          <span class="bar-val">฿${(v/1000).toFixed(0)}K</span>
        </div>`).join('') || '<div class="empty">ไม่มีข้อมูล</div>'}
      </div>
      <div class="dash-card">
        <div class="dash-card-title">วันเฉลี่ยต่อ Stage</div>
        ${byStage.map(s => `<div class="bar-row">
          <span class="bar-label"><span class="stage-dot" style="background:${s.color}"></span>${s.name}</span>
          <div class="bar-track"><div class="bar-fill" style="width:${maxAvg ? Math.round(s.avg/maxAvg*100) : 0}%;background:${s.color}"></div></div>
          <span class="bar-val">${s.avg} วัน</span>
        </div>`).join('')}
      </div>
    </div>
    <div class="dash-row">
      <div class="dash-card" style="grid-column: 1 / -1">
        <div class="dash-card-title" style="display:flex;align-items:center;gap:8px">
          มูลค่างานตามพนักงานขายที่ปิดแล้ว
          <span style="font-size:11px;font-weight:400;color:var(--text-tertiary);background:var(--bg-secondary);padding:2px 8px;border-radius:20px">เฉพาะ Stage End job</span>
        </div>
        ${bySalesClosedSorted.length ? bySalesClosedSorted.map(([n, v]) => {
          const closedCount = endJobCards.filter(c => (c.salesperson || 'ไม่ระบุ') === n).length;
          return `<div class="bar-row">
            <span class="bar-label" style="width:130px">${n}</span>
            <div class="bar-track"><div class="bar-fill" style="width:${Math.round(v/maxSalesClosed*100)}%;background:var(--success)"></div></div>
            <span style="font-size:11px;color:var(--text-tertiary);white-space:nowrap;margin-right:8px">${closedCount} งาน</span>
            <span class="bar-val">฿${(v/1000).toFixed(0)}K</span>
          </div>`;
        }).join('') : '<div class="empty">ยังไม่มีงานใน Stage End job</div>'}
      </div>
    </div>
  </div>`;
}

// ── Modal helpers ─────────────────────────────────────────────────────────────

function showModal(html) {
  document.getElementById('modal-box').innerHTML = html;
  document.getElementById('modal-bg').classList.add('open');
}

function closeModal() {
  document.getElementById('modal-bg').classList.remove('open');
  document.getElementById('modal-box').innerHTML = '';
  _editingCard = null;
}

function handleModalBgClick(e) {
  if (e.target === document.getElementById('modal-bg')) closeModal();
}

// ── Add Stage ─────────────────────────────────────────────────────────────────

function openAddStage() {
  state.selectedColor = STAGE_COLORS[0];
  showModal(`
    <div class="modal-header">
      <span class="modal-title">เพิ่ม Stage ใหม่</span>
      <button class="close-btn" onclick="closeModal()">×</button>
    </div>
    <div class="modal-body">
      <div>
        <div class="field-label">ชื่อ Stage</div>
        <input type="text" id="new-stage-name" placeholder="เช่น ตรวจสอบ, อนุมัติ, ส่งมอบ...">
      </div>
      <div>
        <div class="field-label">สี</div>
        <div class="color-swatches" id="color-swatches">
          ${STAGE_COLORS.map((c, i) => `<div class="color-swatch${i===0?' selected':''}" style="background:${c}" data-color="${c}" onclick="selectColor(this,'${c}')"></div>`).join('')}
        </div>
        <input type="text" id="sel-color" value="${STAGE_COLORS[0]}" style="margin-top:8px" placeholder="#185FA5" oninput="state.selectedColor=this.value">
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn" onclick="closeModal()">ยกเลิก</button>
      <button class="btn btn-primary" onclick="addStage()"><i class="ti ti-check"></i> เพิ่ม Stage</button>
    </div>`);
}

function selectColor(el, color) {
  state.selectedColor = color;
  document.getElementById('sel-color').value = color;
  document.querySelectorAll('.color-swatch').forEach(s => s.classList.remove('selected'));
  el.classList.add('selected');
}

async function addStage() {
  const name = document.getElementById('new-stage-name').value.trim();
  if (!name) { alert('กรุณาระบุชื่อ Stage'); return; }
  const color = document.getElementById('sel-color').value.trim() || state.selectedColor || '#888780';
  const s = { id: genId(), name, color };
  setBusy(true);
  try {
    await DB.insertStage(s);          // Direct INSERT → BOONKONG/CRM69
    state.stages.push(s);
    closeModal(); render();
    showToast('✅ เพิ่ม Stage สำเร็จ');
  } catch(e) { showToast('❌ ' + e.message, true); }
  finally { setBusy(false); }
}

// ── Edit Stage ────────────────────────────────────────────────────────────────

function openEditStage(stageId) {
  const s = state.stages.find(x => x.id === stageId);
  if (!s) return;
  state.selectedColor = s.color;
  showModal(`
    <div class="modal-header">
      <span class="modal-title">แก้ไข Stage</span>
      <button class="close-btn" onclick="closeModal()">×</button>
    </div>
    <div class="modal-body">
      <div>
        <div class="field-label">ชื่อ Stage</div>
        <input type="text" id="edit-stage-name" value="${escHtml(s.name)}" placeholder="ชื่อ Stage">
      </div>
      <div>
        <div class="field-label">สี</div>
        <div class="color-swatches" id="color-swatches">
          ${STAGE_COLORS.map(c => `<div class="color-swatch${c===s.color?' selected':''}" style="background:${c}" data-color="${c}" onclick="selectColor(this,'${c}')"></div>`).join('')}
        </div>
        <input type="text" id="sel-color" value="${s.color}" style="margin-top:8px" placeholder="#185FA5" oninput="state.selectedColor=this.value">
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn" onclick="closeModal()">ยกเลิก</button>
      <button class="btn btn-primary" onclick="saveEditStage('${stageId}')"><i class="ti ti-check"></i> บันทึก</button>
    </div>`);
}

async function saveEditStage(stageId) {
  const s = state.stages.find(x => x.id === stageId);
  if (!s) return;
  const name = document.getElementById('edit-stage-name').value.trim();
  if (!name) { alert('กรุณาระบุชื่อ Stage'); return; }
  const color = document.getElementById('sel-color').value.trim() || state.selectedColor || s.color;
  setBusy(true);
  try {
    await DB.updateStage(stageId, name, color);   // Direct UPDATE → BOONKONG
    s.name = name; s.color = color;
    closeModal(); render();
    showToast('✅ บันทึก Stage สำเร็จ');
  } catch(e) { showToast('❌ ' + e.message, true); }
  finally { setBusy(false); }
}

// ── Delete Stage ──────────────────────────────────────────────────────────────

async function deleteStage(stageId) {
  const cards = cardsInStage(stageId);
  if (cards.length > 0) {
    alert(`ไม่สามารถลบ Stage นี้ได้\nเนื่องจากมีงานอยู่ ${cards.length} รายการ\nกรุณาย้ายงานออกก่อน`);
    return;
  }
  const s = state.stages.find(x => x.id === stageId);
  if (!s) return;
  if (!confirm(`ลบ Stage "${s.name}" ออกจากระบบ?`)) return;
  setBusy(true);
  try {
    await DB.deleteStage(stageId);    // Direct DELETE → BOONKONG
    state.stages = state.stages.filter(x => x.id !== stageId);
    render();
    showToast('✅ ลบ Stage สำเร็จ');
  } catch(e) { showToast('❌ ' + e.message, true); }
  finally { setBusy(false); }
}

// ── Card Form ─────────────────────────────────────────────────────────────────

function openNewCard(stageId) {
  _editingCard = { id: genId(), stageId, title:'', salesperson:'', jobTitle:'', value:'', cost:'', startDate:'', endDate:'', remark:'', jobType: state.jobTypes[0]||'', files:[], stageHistory:[{ stageId, enteredAt: Date.now() }] };
  renderCardModal(true);
}

function openCardDetail(id) {
  _editingCard = JSON.parse(JSON.stringify(state.cards.find(c => c.id === id)));
  renderCardModal(false);
}

function renderCardApptList(cardId) {
  if (!cardId) return '<div style="font-size:12px;color:var(--text-tertiary);padding:4px 0">บันทึกงานก่อนเพื่อดูนัดหมาย</div>';
  const appts = state.appointments
    .filter(a => a.card_id === cardId)
    .sort((a, b) => (a.appt_date + a.appt_time).localeCompare(b.appt_date + b.appt_time));
  if (!appts.length) return '<div style="font-size:12px;color:var(--text-tertiary);padding:4px 0">ยังไม่มีนัดหมาย</div>';
  return '<div class="card-appt-list">' + appts.map(function(a) {
    return '<div class="card-appt-row" onclick="goToApptFromCard(' + a.id + ',\'' + cardId + '\')">'
      + '<div class="card-appt-date"><i class="ti ti-calendar" style="font-size:10px"></i>&nbsp;' + a.appt_date
      + '<br><span style="font-size:11px">' + fmtTimeThai(a.appt_time) + ' น.</span></div>'
      + '<div class="card-appt-subject">' + escHtml(a.subject) + '</div>'
      + '<i class="ti ti-chevron-right" style="font-size:12px;color:var(--text-tertiary)"></i>'
      + '</div>';
  }).join('') + '</div>';
}

function goToApptFromCard(apptId, cardId) {
  event.stopPropagation();
  closeModal();
  setTimeout(function() {
    switchView('calendar');
    openApptForm(apptId, null, cardId);
  }, 80);
}

function renderCardModal(isNew) {
  const c = _editingCard;
  const days = isNew ? 0 : getDaysInStage(c);
  const total = isNew ? 0 : getTotalDays(c);
  const stageOpts = state.stages.map(s => `<option value="${s.id}" ${s.id===c.stageId?'selected':''}>${s.name}</option>`).join('');
  const typeOpts = state.jobTypes.map(t => `<option value="${t}" ${t===c.jobType?'selected':''}>${t}</option>`).join('');
  const fileHtml = renderFileList(c);
  const timelineHtml = !isNew ? renderTimeline(c) : '';

  showModal(`
    <div class="modal-header">
      <span class="modal-title">${isNew ? 'เพิ่มงานใหม่' : (c.title||'รายละเอียดงาน')}</span>
      <button class="close-btn" onclick="closeModal()">×</button>
    </div>
    <div class="modal-body">
      ${!isNew ? `<div class="detail-stats">
        <div class="detail-stat"><div class="detail-stat-label">วันใน Stage นี้</div><div class="detail-stat-value">${days}</div></div>
        <div class="detail-stat"><div class="detail-stat-label">วันรวมทั้งหมด</div><div class="detail-stat-value">${total}</div></div>
      </div>` : ''}

      <div>
        <div class="field-label">ชื่อลูกค้า / บริษัท *</div>
        <input type="text" id="f-title" value="${escHtml(c.title)}" placeholder="ชื่อบริษัทหรือลูกค้า">
      </div>
      <div class="field-row">
        <div>
          <div class="field-label">ชื่อพนักงานขาย</div>
          <input type="text" id="f-sales" value="${escHtml(c.salesperson)}" placeholder="ชื่อ-นามสกุล">
        </div>
        <div>
          <div class="field-label">Stage</div>
          <select id="f-stage">${stageOpts}</select>
        </div>
      </div>
      <div>
        <div class="field-label">ชื่อหัวข้องาน</div>
        <input type="text" id="f-jobtitle" value="${escHtml(c.jobTitle)}" placeholder="เช่น ระบบ ERP, ปรับปรุงเว็บไซต์...">
      </div>
      <div class="field-row">
        <div>
          <div class="field-label">มูลค่างาน (บาท)</div>
          <input type="number" id="f-value" value="${c.value||''}" placeholder="0" min="0">
        </div>
        <div>
          <div class="field-label">ประเภทงาน</div>
          <div class="type-row">
            <select id="f-type">${typeOpts}</select>
            <button class="btn btn-sm" onclick="addJobTypePrompt()" title="เพิ่มประเภทงาน"><i class="ti ti-plus"></i></button>
          </div>
        </div>
      </div>
      <div class="field-row">
        <div>
          <div class="field-label">ค่าใช้จ่ายโครงการ (บาท)</div>
          <input type="number" id="f-cost" value="${c.cost||''}" placeholder="0" min="0">
        </div>
        <div></div>
      </div>
      <div class="field-row">
        <div>
          <div class="field-label">วันเริ่มโครงการ</div>
          <input type="date" id="f-start" value="${c.startDate||''}">
        </div>
        <div>
          <div class="field-label">วันสิ้นสุดโครงการ</div>
          <input type="date" id="f-end" value="${c.endDate||''}">
        </div>
      </div>
      <div>
        <div class="field-label" style="margin-bottom:8px">ข้อมูลการนัดหมายงาน</div>
        ${renderCardApptList(c.id)}
      </div>

      <hr class="section-divider">

      <div>
        <div class="field-label">หมายเหตุ</div>
        <textarea id="f-remark" rows="3" placeholder="บันทึกหมายเหตุเพิ่มเติม..." style="width:100%;resize:vertical;font-family:inherit;font-size:13px;padding:8px 10px;border:1px solid var(--border);border-radius:6px;background:var(--bg-input,var(--bg-secondary));color:var(--text-primary);box-sizing:border-box">${escHtml(c.remark||'')}</textarea>
      </div>

      <hr class="section-divider">

      <div>
        <div class="field-label" style="margin-bottom:8px">ไฟล์งาน</div>
        <div class="file-drop" onclick="triggerFileInput()">
          <i class="ti ti-cloud-upload"></i>
          <span style="font-size:12px">คลิกหรือลากไฟล์มาวางที่นี่</span>
        </div>
        <div class="file-list" id="file-list"></div>
      </div>

      ${timelineHtml ? `<hr class="section-divider"><div><div class="field-label" style="margin-bottom:8px">ประวัติ Stage</div><div class="stage-timeline">${timelineHtml}</div></div>` : ''}
    </div>
    <div class="modal-footer">
      ${!isNew ? `<button class="btn btn-danger" onclick="deleteCard('${c.id}')"><i class="ti ti-trash"></i> ลบงาน</button>` : ''}
      <button class="btn" onclick="closeModal()">ยกเลิก</button>
      <button class="btn btn-primary" onclick="saveCard(${isNew})"><i class="ti ti-check"></i> บันทึก</button>
    </div>`);

  document.getElementById('file-list').innerHTML = fileHtml;

  document.getElementById('file-input').onchange = function(e) {
    Array.from(e.target.files).forEach(f => {
      const reader = new FileReader();
      reader.onload = ev => {
        _editingCard.files.push({ name: f.name, data: ev.target.result, type: f.type, size: f.size });
        document.getElementById('file-list').innerHTML = renderFileList(_editingCard);
        bindFileEvents();
      };
      reader.readAsDataURL(f);
    });
    e.target.value = '';
  };

  bindFileEvents();
}

function renderTimeline(c) {
  const h = c.stageHistory || [];
  return h.map((item, i) => {
    const next = h[i+1];
    const daysSpent = next ? Math.floor((next.enteredAt - item.enteredAt) / 86400000) : Math.floor((Date.now() - item.enteredAt) / 86400000);
    const color = stageColor(item.stageId);
    return `<div class="timeline-item">
      <div class="timeline-dot" style="background:${color}"></div>
      <span class="timeline-label">${stageName(item.stageId)}</span>
      <span class="timeline-days">${daysSpent} วัน${i===h.length-1?' (ปัจจุบัน)':''}</span>
    </div>`;
  }).join('');
}

function renderFileList(c) {
  if (!c.files || !c.files.length) return '';
  return c.files.map((f, i) => `<div class="file-item" data-fi="${i}">
    <i class="ti ti-file-text"></i>
    <span class="file-name">${escHtml(f.name)}</span>
    <span class="file-size">${f.size ? (f.size/1024 < 1024 ? (f.size/1024).toFixed(1)+'KB' : (f.size/1024/1024).toFixed(1)+'MB') : ''}</span>
    <button class="btn btn-ghost btn-sm" onclick="downloadFile(${i})" title="ดาวน์โหลด"><i class="ti ti-download"></i></button>
    <button class="btn btn-ghost btn-sm" onclick="removeFile(${i})" title="ลบ" style="color:var(--danger)"><i class="ti ti-trash"></i></button>
  </div>`).join('');
}

function bindFileEvents() {}

function triggerFileInput() { document.getElementById('file-input').click(); }

function downloadFile(i) {
  const f = _editingCard && _editingCard.files[i];
  if (!f) return;
  const a = document.createElement('a');
  a.href = f.data; a.download = f.name; a.click();
}

function removeFile(i) {
  if (!_editingCard) return;
  _editingCard.files.splice(i, 1);
  document.getElementById('file-list').innerHTML = renderFileList(_editingCard);
}

async function addJobTypePrompt() {
  const name = prompt('ชื่อประเภทงานใหม่:', '');
  if (!name || !name.trim()) return;
  const trimmed = name.trim();
  if (!state.jobTypes.includes(trimmed)) {
    try {
      await DB.insertJobType(trimmed);   // Direct INSERT → BOONKONG
      state.jobTypes.push(trimmed);
    } catch(e) { showToast('❌ ' + e.message, true); return; }
  }
  const sel = document.getElementById('f-type');
  if (sel) {
    const opt = document.createElement('option');
    opt.value = trimmed; opt.textContent = trimmed; opt.selected = true;
    sel.appendChild(opt);
  }
}

async function saveCard(isNew) {
  const title = document.getElementById('f-title').value.trim();
  if (!title) { alert('กรุณาระบุชื่อลูกค้า / บริษัท'); return; }
  const newStageId = document.getElementById('f-stage').value;

  Object.assign(_editingCard, {
    title,
    salesperson: document.getElementById('f-sales').value.trim(),
    jobTitle:    document.getElementById('f-jobtitle').value.trim(),
    value:       Number(document.getElementById('f-value').value) || 0,
    cost:        Number(document.getElementById('f-cost').value)  || 0,
    jobType:     document.getElementById('f-type').value,
    startDate:   document.getElementById('f-start').value,
    endDate:     document.getElementById('f-end').value,
    remark:      document.getElementById('f-remark').value.trim(),
  });

  setBusy(true);
  try {
    if (isNew) {
      _editingCard.stageId = newStageId;
      _editingCard.stageHistory = [{ stageId: newStageId, enteredAt: Date.now() }];
      await DB.insertCard(_editingCard);        // Direct INSERT → BOONKONG/CRM69
      state.cards.push({ ..._editingCard });
      showToast('✅ เพิ่มงานสำเร็จ');
    } else {
      const existing = state.cards.find(c => c.id === _editingCard.id);
      if (existing) {
        const prevStage = existing.stageId;
        Object.assign(existing, _editingCard);
        existing.stageId = newStageId;
        if (prevStage !== newStageId) {
          if (!existing.stageHistory) existing.stageHistory = [];
          existing.stageHistory.push({ stageId: newStageId, enteredAt: Date.now() });
        }
        await DB.updateCard(existing);          // Direct UPDATE → BOONKONG/CRM69
      }
      showToast('✅ บันทึกงานสำเร็จ');
    }
    closeModal(); render();
  } catch(e) { showToast('❌ บันทึกล้มเหลว: ' + e.message, true); }
  finally { setBusy(false); }
}

async function deleteCard(id) {
  if (!confirm('ลบงานนี้ออกจากระบบ?')) return;
  setBusy(true);
  try {
    await DB.deleteCard(id);           // Direct DELETE → BOONKONG/CRM69
    state.cards = state.cards.filter(c => c.id !== id);
    closeModal(); render();
    showToast('✅ ลบงานสำเร็จ');
  } catch(e) { showToast('❌ ' + e.message, true); }
  finally { setBusy(false); }
}

function escHtml(s) {
  return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');
}


// ── INIT — โหลดข้อมูลจาก Supabase ───────────────────────────────────────────
async function initApp() {
  const main = document.getElementById('main-content');
  main.innerHTML = `
    <div style="display:flex;flex-direction:column;align-items:center;justify-content:center;height:60vh;gap:14px;color:var(--text-secondary)">
      <i class="ti ti-database" style="font-size:42px;color:var(--accent)"></i>
      <div style="font-size:14px;font-weight:500">กำลังเชื่อมต่อ Supabase ...</div>
      <div style="font-size:12px;color:var(--text-tertiary)">Supabase PostgreSQL</div>
    </div>`;
  try {
    const sb = getSB();

    // โหลดข้อมูลพร้อมกัน
    const [stagesRes, cardsRes, histRes, filesRes, jtRes, apptRes] = await Promise.all([
      sb.from('stages').select('*').order('sort_order'),
      sb.from('cards').select('*').order('created_at'),
      sb.from('stage_history').select('*').order('entered_at'),
      sb.from('card_files').select('*').order('id'),
      sb.from('job_types').select('name').order('id'),
      sb.from('appointments').select('*').order('appt_date').order('appt_time'),
    ]);

    for (const r of [stagesRes, cardsRes, histRes, filesRes, jtRes, apptRes]) {
      if (r.error) throw new Error(r.error.message);
    }

    state.stages       = stagesRes.data;
    state.jobTypes     = jtRes.data.map(r => r.name);
    state.appointments = apptRes.data || [];
    state.calDate      = new Date();
    state.calViewMonth = new Date();

    // รวม history + files เข้า cards
    state.cards = cardsRes.data.map(c => ({
      id:          c.id,
      stageId:     c.stage_id,
      title:       c.title,
      salesperson: c.salesperson  || '',
      jobTitle:    c.job_title    || '',
      value:       Number(c.value) || 0,
      cost:        Number(c.cost)  || 0,
      jobType:     c.job_type     || '',
      startDate:   c.start_date   || '',
      endDate:     c.end_date     || '',
      remark:      c.remark       || '',
      stageHistory: histRes.data
        .filter(h => h.card_id === c.id)
        .map(h => ({ stageId: h.stage_id, enteredAt: Number(h.entered_at) })),
      files: filesRes.data
        .filter(f => f.card_id === c.id)
        .map(f => ({ name: f.file_name, type: f.file_type, size: f.file_size, data: f.file_data })),
    }));

    const nums = state.cards.map(c => parseInt(c.id.replace(/\D/g,''),10)).filter(n=>!isNaN(n));
    if (nums.length) state.nextId = Math.max(...nums) + 1;

    render();
    showToast(`✅ เชื่อมต่อ Supabase สำเร็จ (${state.cards.length} งาน)`);
  } catch (e) {
    main.innerHTML = `
      <div style="display:flex;flex-direction:column;align-items:center;justify-content:center;height:60vh;gap:12px">
        <i class="ti ti-database-off" style="font-size:48px;color:var(--danger)"></i>
        <div style="font-size:15px;font-weight:600;color:var(--text-primary)">เชื่อมต่อ Supabase ไม่ได้</div>
        <div style="font-size:12px;color:var(--text-secondary);max-width:380px;text-align:center">${e.message}</div>
        <button onclick="initApp()" style="margin-top:8px;padding:8px 22px;background:var(--accent);color:#fff;border:none;border-radius:8px;cursor:pointer;font-size:13px;display:flex;align-items:center;gap:6px">
          <i class="ti ti-refresh"></i> ลองใหม่
        </button>
      </div>`;
  }
}

initApp();

</script>
</body>
</html>
