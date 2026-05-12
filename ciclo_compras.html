<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8" isELIgnored="false"%>
<!DOCTYPE html>
<%@ page import="java.util.*" %>
<%@ taglib uri="http://java.sun.com/jstl/core_rt" prefix="c" %>
<%@ taglib prefix="snk" uri="/WEB-INF/tld/sankhyaUtil.tld" %>
<%@ taglib uri="http://java.sun.com/jsp/jstl/fmt" prefix="fmt" %>

<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ciclo de Compras - Tempo por Compradora</title>
<snk:load/>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<style>
  :root {
    --bg: #f4f3f0; --surface: #ffffff; --surface2: #f9f8f5;
    --border: rgba(0,0,0,0.10); --border2: rgba(0,0,0,0.18);
    --text: #1a1a18; --text2: #5f5e5a; --text3: #888780;
    --teal: #1D9E75; --teal-light: #E1F5EE; --teal-dark: #0F6E56;
    --amber: #BA7517; --amber-light: #FAEEDA;
    --red: #A32D2D; --red-light: #FCEBEB;
    --blue: #185FA5; --blue-light: #E6F1FB;
    --purple: #6B3FA0; --purple-light: #F0EAFA;
    --orange: #C46C1A; --orange-light: #FDF0E3;
    --radius: 10px; --radius-sm: 6px;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Segoe UI', system-ui, sans-serif; background: var(--bg); color: var(--text); font-size: 14px; line-height: 1.5; }

  /* HEADER */
  header { background: var(--surface); border-bottom: 1px solid var(--border2); padding: 14px 24px; display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0; z-index: 100; }
  .logo { display: flex; align-items: center; gap: 10px; }
  .logo-box { width: 32px; height: 32px; background: var(--blue); border-radius: var(--radius-sm); display: flex; align-items: center; justify-content: center; font-size: 16px; }
  .logo-text { font-size: 15px; font-weight: 600; letter-spacing: -0.3px; }
  .logo-sub { font-size: 12px; color: var(--text2); }

  /* LAYOUT */
  .layout { display: grid; grid-template-columns: 260px 1fr; min-height: calc(100vh - 57px); }
  aside { background: var(--surface); border-right: 1px solid var(--border); padding: 20px 16px; display: flex; flex-direction: column; gap: 20px; }
  .filter-title { font-size: 11px; font-weight: 600; color: var(--text3); text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 6px; }
  .filter-group { display: flex; flex-direction: column; gap: 8px; }
  label { font-size: 12px; color: var(--text2); display: block; margin-bottom: 3px; }
  input[type=text], input[type=date], select {
    width: 100%; padding: 7px 10px; border: 1px solid var(--border2);
    border-radius: var(--radius-sm); background: var(--surface2);
    color: var(--text); font-size: 13px; outline: none;
  }
  input:focus, select:focus { border-color: var(--blue); }
  .btn { padding: 8px 16px; border-radius: var(--radius-sm); font-size: 13px; font-weight: 500; cursor: pointer; border: none; width: 100%; transition: opacity 0.15s; }
  .btn-primary { background: var(--blue); color: #fff; }
  .btn-ghost { background: transparent; color: var(--text2); border: 1px solid var(--border2); margin-top: 4px; }
  .btn-ghost:hover { background: var(--surface2); }

  /* MAIN */
  main { padding: 20px 24px; display: flex; flex-direction: column; gap: 20px; overflow: auto; }

  /* METRICS */
  .metrics { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 12px; }
  .metric-card { background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius); padding: 14px 16px; }
  .metric-card.accent-teal  { border-left: 3px solid var(--teal); }
  .metric-card.accent-blue  { border-left: 3px solid var(--blue); }
  .metric-card.accent-amber { border-left: 3px solid var(--amber); }
  .metric-card.accent-red   { border-left: 3px solid var(--red); }
  .metric-card.accent-purple{ border-left: 3px solid var(--purple); }
  .metric-card.accent-orange{ border-left: 3px solid var(--orange); }
  .metric-label { font-size: 11px; color: var(--text3); text-transform: uppercase; letter-spacing: 0.6px; margin-bottom: 6px; }
  .metric-value { font-size: 24px; font-weight: 700; letter-spacing: -0.5px; }
  .metric-sub { font-size: 11px; color: var(--text2); margin-top: 3px; }

  /* CHARTS */
  .charts { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .chart-card { background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius); padding: 16px 18px; }
  .chart-card.full { grid-column: 1 / -1; }
  .card-title { font-size: 13px; font-weight: 600; margin-bottom: 14px; color: var(--text); }

  /* STATUS BADGES */
  .badge { display: inline-block; padding: 2px 8px; border-radius: 20px; font-size: 10px; font-weight: 600; }
  .b-aberta    { background: var(--blue-light);   color: var(--blue); }
  .b-fechada   { background: var(--teal-light);   color: var(--teal-dark); }
  .b-aprovada  { background: #E8F5E9;              color: #2E7D32; }
  .b-cancelada { background: var(--red-light);    color: var(--red); }
  .b-precif    { background: var(--amber-light);  color: var(--amber); }
  .b-enviada   { background: var(--purple-light); color: var(--purple); }
  .b-sem       { background: var(--surface2);     color: var(--text3); border: 1px solid var(--border2); }

  /* DETALHE COMPRA */
  .b-vcasada  { background: #E3F2FD; color: #1565C0; }
  .b-export   { background: #E8EAF6; color: #3949AB; }
  .b-estrateg { background: #E0F2F1; color: #00695C; }
  .b-balcao   { background: #FFF8E1; color: #F57F17; }
  .b-estoque  { background: #F3E5F5; color: #7B1FA2; }

  /* TABLE */
  .table-card { background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius); overflow: hidden; }
  .table-header { padding: 14px 18px; border-bottom: 1px solid var(--border); display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 8px; }
  .search-wrap { position: relative; }
  .search-wrap input { padding: 6px 10px 6px 28px; width: 300px; font-size: 12px; }
  .search-icon { position: absolute; left: 8px; top: 50%; transform: translateY(-50%); color: var(--text3); font-size: 13px; pointer-events: none; }
  .table-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; font-size: 12px; }
  thead th { padding: 9px 12px; text-align: left; font-size: 10px; font-weight: 600; color: var(--text3); text-transform: uppercase; letter-spacing: 0.5px; background: var(--surface2); border-bottom: 1px solid var(--border); white-space: nowrap; cursor: pointer; user-select: none; }
  thead th:hover { color: var(--text); }
  tbody tr { border-bottom: 1px solid var(--border); cursor: pointer; }
  tbody tr:hover { background: var(--surface2); }
  tbody tr:last-child { border-bottom: none; }
  tbody td { padding: 9px 12px; white-space: nowrap; }
  tbody tr.row-selected { background: var(--blue-light) !important; }
  tbody tr.row-selected td { color: var(--blue); font-weight: 500; }

  /* PAGINATION */
  .pagination { padding: 12px 18px; border-top: 1px solid var(--border); display: flex; align-items: center; justify-content: space-between; font-size: 12px; color: var(--text2); }
  .pag-btns { display: flex; gap: 4px; flex-wrap: wrap; }
  .pb { padding: 4px 10px; border: 1px solid var(--border2); background: var(--surface); border-radius: var(--radius-sm); cursor: pointer; font-size: 12px; }
  .pb.act { background: var(--blue); color: #fff; border-color: var(--blue); }

  /* TABS */
  .tabs { display: flex; border-bottom: 1px solid var(--border); }
  .tab { padding: 10px 18px; font-size: 13px; cursor: pointer; color: var(--text2); border-bottom: 2px solid transparent; margin-bottom: -1px; }
  .tab.act { color: var(--blue); border-bottom-color: var(--blue); font-weight: 500; }
  .tc { display: none; }
  .tc.act { display: block; }

  /* MISC */
  .no-data, .loading { text-align: center; padding: 36px; color: var(--text3); font-style: italic; }
  .val-pos { color: var(--teal-dark); font-weight: 600; }
  .val-neg { color: var(--red); font-weight: 600; }
  .val-warn { color: var(--amber); font-weight: 600; }

  /* AUTOCOMPLETE */
  .ac-wrap { position: relative; }
  .ac-list { position: absolute; top: 100%; left: 0; right: 0; background: var(--surface); border: 1px solid var(--border2); border-radius: 0 0 var(--radius-sm) var(--radius-sm); max-height: 220px; overflow-y: auto; z-index: 999; box-shadow: 0 4px 12px rgba(0,0,0,0.12); }
  .ac-item { padding: 8px 10px; cursor: pointer; font-size: 12px; border-bottom: 1px solid var(--border); display: flex; gap: 8px; }
  .ac-item:hover { background: var(--blue-light); }
  .ac-cod { font-weight: 600; color: var(--blue); min-width: 36px; }
  .ac-nome { color: var(--text2); }
  .ac-selected { background: var(--blue-light); border: 1px solid var(--blue); border-radius: var(--radius-sm); padding: 6px 10px; font-size: 12px; color: var(--blue); font-weight: 500; display: flex; align-items: center; justify-content: space-between; margin-top: 4px; }
  .ac-selected button { background: none; border: none; cursor: pointer; color: var(--blue); font-size: 14px; padding: 0; }

  /* FULLSCREEN */
  .table-card.fullscreen {
    position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
    z-index: 999; margin: 0; border-radius: 0;
    box-shadow: 0 0 0 9999px rgba(0,0,0,0.4);
    display: flex; flex-direction: column; background: var(--surface);
  }
  .table-card.fullscreen .table-wrap { flex: 1; overflow: auto; }
  .layout.fullscreen aside { display: none; }
  .layout.fullscreen main { grid-column: 1 / -1; width: 100%; }

  /* RANKING TABLE */
  .rank-table { width: 100%; border-collapse: collapse; font-size: 12px; }
  .rank-table td { padding: 7px 10px; border-bottom: 1px solid var(--border); }
  .rank-table tr:last-child td { border-bottom: none; }
  .rank-bar-wrap { background: var(--surface2); border-radius: 4px; height: 6px; flex: 1; overflow: hidden; }
  .rank-bar { height: 100%; border-radius: 4px; background: var(--blue); }

  /* TEMPO COLOR */
  .t-fast   { color: var(--teal-dark); font-weight: 600; }
  .t-medium { color: var(--amber);     font-weight: 600; }
  .t-slow   { color: var(--red);       font-weight: 600; }
</style>
</head>
<body>

<header>
  <div class="logo">
    <div class="logo-box">&#x1F6D2;</div>
    <div>
      <div class="logo-text">Ciclo de Compras</div>
      <div class="logo-sub">Suprimentos &middot; Tempo por Compradora</div>
    </div>
  </div>
  <span style="font-size:12px;color:var(--text3);" id="upd"></span>
</header>

<div class="layout">
  <aside>
    <div>
      <div class="filter-title">Periodo</div>
      <div class="filter-group">
        <div><label>Data inicial</label><input type="date" id="fini"></div>
        <div><label>Data final</label><input type="date" id="ffin"></div>
      </div>
    </div>
    <div>
      <div class="filter-title">Filtros</div>
      <div class="filter-group">
        <div>
          <label>Nro Único Pedido</label>
          <input type="text" id="fnropedido" placeholder="Ex: 123456">
        </div>
        <div>
          <label>Num. Cotação</label>
          <input type="text" id="fnumcotacao" placeholder="Ex: 1234">
        </div>
        <div>
          <label>Compradora</label>
          <div class="ac-wrap">
            <input type="text" id="fcomp_nome" placeholder="Digite nome ou codigo..." autocomplete="off" oninput="buscarComprador(this.value)">
            <input type="hidden" id="fcomp" value="0">
            <div id="acListComp" class="ac-list" style="display:none;"></div>
          </div>
          <div id="acSelecionadoComp" style="display:none;"></div>
        </div>
        <div>
          <label>Status</label>
          <select id="fstatus">
            <option value="">Todos</option>
            <option value="O">Aberta</option>
            <option value="F">Fechada</option>
            <option value="A">Aprovada</option>
            <option value="C">Cancelada</option>
            <option value="P">Precificada</option>
            <option value="E">Enviada</option>
          </select>
        </div>
        <div>
          <label>Detalhe da Compra</label>
          <select id="fdetalhe">
            <option value="">Todos</option>
            <option value="1">Venda Casada</option>
            <option value="2">Exportacao</option>
            <option value="3">Compra Estrategica</option>
            <option value="4">Balcao</option>
            <option value="5">Estoque</option>
          </select>
        </div>
      </div>
    </div>
    <button class="btn btn-primary" onclick="aplicar()">&#x1F50D; Aplicar Filtros</button>
    <button class="btn btn-ghost" onclick="limpar()">Limpar Filtros</button>
    <div style="margin-top:auto;padding-top:16px;border-top:1px solid var(--border);">
      <div class="filter-title">Exportar</div>
      <button class="btn btn-ghost" style="margin-top:6px;" onclick="exportCSV()">&#x2B07; Exportar CSV</button>
    </div>
  </aside>

  <main>
    <!-- METRICS -->
    <div class="metrics">
      <div class="metric-card accent-blue">
        <div class="metric-label">Total de Cotacoes</div>
        <div class="metric-value" id="mTotal">-</div>
        <div class="metric-sub">no periodo</div>
      </div>
      <div class="metric-card accent-teal">
        <div class="metric-label">Fechadas</div>
        <div class="metric-value" id="mFechadas">-</div>
        <div class="metric-sub">concluidas</div>
      </div>
      <div class="metric-card accent-amber">
        <div class="metric-label">Abertas</div>
        <div class="metric-value" id="mAbertas">-</div>
        <div class="metric-sub">em andamento</div>
      </div>
      <div class="metric-card accent-red">
        <div class="metric-label">Canceladas</div>
        <div class="metric-value" id="mCanceladas">-</div>
        <div class="metric-sub">no periodo</div>
      </div>
      <div class="metric-card accent-purple">
        <div class="metric-label">Tempo Medio</div>
        <div class="metric-value" id="mTempMed">-</div>
        <div class="metric-sub">dias (com data final)</div>
      </div>
      <div class="metric-card accent-purple">
        <div class="metric-label">Tempo Medio em Horas</div>
        <div class="metric-value" id="mTempMedHoras">-</div>
        <div class="metric-sub">horas (com data final)</div>
      </div>
      <div class="metric-card accent-orange">
        <div class="metric-label">Compradoras</div>
        <div class="metric-value" id="mCompradoras">-</div>
        <div class="metric-sub">ativas no periodo</div>
      </div>
    </div>

    <!-- CHARTS -->
    <div class="charts">
      <div class="chart-card">
        <div class="card-title">Status das Cotacoes por Compradora</div>
        <div style="position:relative;height:240px;"><canvas id="cStatus"></canvas></div>
      </div>
      <div class="chart-card">
        <div class="card-title">Tempo Medio de Ciclo (dias) por Compradora</div>
        <div style="position:relative;height:240px;"><canvas id="cTempo"></canvas></div>
      </div>
      <div class="chart-card full">
        <div class="card-title">Cotacoes Abertas por Dia</div>
        <div style="position:relative;height:180px;"><canvas id="cLine"></canvas></div>
      </div>
    </div>

    <!-- TABLE -->
    <div class="table-card">
      <div class="table-header">
        <div style="display:flex;align-items:center;gap:12px;">
          <span style="font-size:13px;font-weight:600;">Detalhamento das Cotacoes</span>
          <span id="tcnt" style="font-size:11px;color:var(--text3);"></span>
        </div>
        <div style="display:flex;align-items:center;gap:8px;">
          <div class="search-wrap">
            <span class="search-icon">&#x1F50D;</span>
            <input type="text" id="tsrch" placeholder="Buscar num. cotacao, compradora, vendedor..." oninput="renderTabela()">
          </div>
          <button class="pb" id="btnFullscreen" style="padding:6px 10px;" onclick="toggleTableFullscreen()">&#x26F6;</button>
        </div>
      </div>

      <div class="tabs">
        <div class="tab act" onclick="swtab(this,'t1')">Cotacoes</div>
        <div class="tab"     onclick="swtab(this,'t2')">Resumo por Compradora</div>
      </div>

      <div class="table-wrap">
        <!-- Tab 1: Detail -->
        <div id="t1" class="tc act">
          <table>
            <thead><tr>
              <th onclick="srt('numcot')">Num. Cotacao</th>
              <th onclick="srt('nropedido')">Num. Pedido</th>
              <th onclick="srt('comprador')">Compradora</th>
              <th onclick="srt('vendedor')">Vendedor</th>
              <th onclick="srt('dhinic')">Data Inicio</th>
              <th onclick="srt('dhfinal')">Data Fim</th>
              <th onclick="srt('tempoDias')" style="text-align:right">Tempo (Dias)</th>
              <th onclick="srt('tempoHoras')" style="text-align:right">Tempo (Hrs)</th>
              <th onclick="srt('status')">Status</th>
              <th onclick="srt('detalhe')">Detalhe Compra</th>
            </tr></thead>
            <tbody id="b1"><tr><td colspan="9" class="loading">Aplique os filtros para carregar os dados.</td></tr></tbody>
          </table>
        </div>

        <!-- Tab 2: Summary -->
        <div id="t2" class="tc">
          <table>
            <thead><tr>
              <th>Compradora</th>
              <th style="text-align:right">Total Cotacoes</th>
              <th style="text-align:right">Abertas</th>
              <th style="text-align:right">Fechadas</th>
              <th style="text-align:right">Aprovadas</th>
              <th style="text-align:right">Canceladas</th>
              <th style="text-align:right">Precificadas</th>
              <th style="text-align:right">Enviadas</th>
              <th style="text-align:right">Tempo Med. (dias)</th>
            </tr></thead>
            <tbody id="b2"><tr><td colspan="9" class="loading">Aplique os filtros para carregar os dados.</td></tr></tbody>
          </table>
        </div>
      </div>

      <div class="pagination">
        <span id="pinfo"></span>
        <div class="pag-btns" id="pbts"></div>
      </div>
    </div>
  </main>
</div>

<script>

var ALL = [], FIL = [];
var sortC = 'dhinic', sortD = 1;
var pg = 1, PP = 15;
var chartStatus = null, chartTempo = null, chartLine = null;
var acTimer = null;
var selectedRow = null;

// ===== DATAS PADRAO =====
(function(){
    var hoje = new Date();
    var prim = new Date(hoje.getFullYear(), hoje.getMonth(), 1);
    function fmt(d){ return d.toISOString().split('T')[0]; }
    document.getElementById('fini').value = fmt(prim);
    document.getElementById('ffin').value = fmt(hoje);
})();

// ===== AUTOCOMPLETE COMPRADOR =====
function buscarComprador(termo){
    clearTimeout(acTimer);
    var list = document.getElementById('acListComp');
    if(!termo || termo.length < 2){ list.style.display='none'; list.innerHTML=''; return; }
    acTimer = setTimeout(function(){
        var like = '%' + termo.toUpperCase() + '%';
        var q = "SELECT CODUSU, NOMEUSU FROM TSIUSU " +
                "WHERE (UPPER(NOMEUSU) LIKE ? OR TO_CHAR(CODUSU) LIKE ?) " +
                "AND DTLIMACESSO IS NULL AND CODGRUPO IN (5,1) AND ROWNUM <= 15 ORDER BY NOMEUSU";
        var params = [{value:like,type:"S"},{value:like,type:"S"}];
        executeQuery(q, params, function(res){
            var dados = JSON.parse(res);
            if(!dados || dados.length===0){
                list.innerHTML='<div class="ac-item"><span class="ac-nome">Nenhum encontrado</span></div>';
                list.style.display='block'; return;
            }
            list.innerHTML = dados.map(function(p){
                var nome = (p.NOMEUSU||'').replace(/"/g,'&quot;');
                return '<div class="ac-item" onclick="selecionarComprador('+p.CODUSU+',\''+nome.replace(/'/g,"\\'")+'\')">'+
                       '<span class="ac-cod">'+p.CODUSU+'</span>'+
                       '<span class="ac-nome">'+p.NOMEUSU+'</span></div>';
            }).join('');
            list.style.display='block';
        }, function(err){
            list.innerHTML='<div class="ac-item"><span class="ac-nome">Erro: '+err+'</span></div>';
            list.style.display='block';
        });
    }, 300);
}

function selecionarComprador(cod, nome){
    document.getElementById('fcomp').value = cod;
    document.getElementById('fcomp_nome').value = '';
    document.getElementById('acListComp').style.display='none';
    document.getElementById('acListComp').innerHTML='';
    var sel = document.getElementById('acSelecionadoComp');
    sel.style.display='block';
    sel.innerHTML='<div class="ac-selected"><span>'+cod+' - '+nome+'</span>'+
                  '<button onclick="limparComprador()">x</button></div>';
}

function limparComprador(){
    document.getElementById('fcomp').value='0';
    document.getElementById('fcomp_nome').value='';
    document.getElementById('acSelecionadoComp').style.display='none';
    document.getElementById('acSelecionadoComp').innerHTML='';
}

document.addEventListener('click', function(e){
    if(!e.target.closest('.ac-wrap')){
        var list = document.getElementById('acListComp');
        if(list) list.style.display='none';
    }
});

// ===== FORMATOS =====
function fmtDate(d){
    if(!d) return '-';
    var dt = (d instanceof Date)?d:new Date(d);
    if(isNaN(dt)) return '-';
    return dt.toLocaleDateString('pt-BR');
}

function fmtTempo(dias){
    if(dias === null || dias === undefined || isNaN(dias)) return '-';
    if(dias < 1) return (dias * 24).toFixed(1) + 'h';
    return dias.toFixed(1) + 'd';
}

function tempoCls(dias){
    if(dias === null || dias === undefined || isNaN(dias)) return '';
    if(dias <= 3)  return 't-fast';
    if(dias <= 7)  return 't-medium';
    return 't-slow';
}

function badgeStatus(s){
    var mapa = {
        'Aberta':'b-aberta','Fechada':'b-fechada','Aprovada':'b-aprovada',
        'Cancelada':'b-cancelada','Precificada':'b-precif','Enviada':'b-enviada'
    };
    return '<span class="badge '+(mapa[s]||'b-sem')+'">'+(s||'-')+'</span>';
}

function badgeDetalhe(d){
    var mapa = {
        'Venda Casada':'b-vcasada','Exportacao':'b-export','Exportação':'b-export',
        'Compra Estrategica':'b-estrateg','Compra Estratégica':'b-estrateg',
        'Balcao':'b-balcao','Balcão':'b-balcao','Estoque':'b-estoque'
    };
    return '<span class="badge '+(mapa[d]||'b-sem')+'">'+(d||'-')+'</span>';
}

// ===== APLICAR FILTROS =====
function aplicar(){
    var nroPedido   = (document.getElementById('fnropedido').value || '').trim();
    var numCotacao  = (document.getElementById('fnumcotacao').value || '').trim();
    var dataIni     = document.getElementById('fini').value;
    var dataFim     = document.getElementById('ffin').value;
    var usarData    = !nroPedido && !numCotacao;

    if(usarData && (!dataIni || !dataFim)){ alert("Informe as datas de inicio e fim ou use um filtro de Nro Pedido/Cotacao."); return; }

    var codComp  = parseInt(document.getElementById('fcomp').value) || 0;
    var status   = document.getElementById('fstatus').value || " ";
    var detalhe  = document.getElementById('fdetalhe').value || "0";

    document.getElementById('upd').textContent = "Carregando...";
    document.getElementById('b1').innerHTML = '<tr><td colspan="9" class="loading">Buscando dados...</td></tr>';

    // =============================================
    // QUERY PRINCIPAL: cotacoes com tempo de ciclo
    // Parametros variam conforme os filtros usados
    // =============================================
    var query =
    "SELECT DISTINCT " +
    "    COT.NUMCOTACAO, " +
    "    GRU.AD_CODUSU || ' - ' || USUC.NOMEUSU AS COMPRADOR, " +
    "    GRU.AD_CODUSU AS COD_COMPRADOR, " +
    "    COT.CODUSUREQ || ' - ' || USU.NOMEUSU AS VENDEDOR, " +
    "    COT.DHINIC, " +
    "    ITC.AD_DATAFINAL, " +
    "    (ITC.AD_DATAFINAL - COT.DHINIC) - (8/24) AS TEMPO_DIAS, " +
    "    ((ITC.AD_DATAFINAL - COT.DHINIC) * 24) - 8 AS TEMPO_HORAS, " +
    "    CAB.NUNOTA AS NRO_UNICO_PEDIDO, " +
    "    CASE " +
    "        WHEN ITC.STATUSPRODCOT = 'A' THEN 'Aprovada' " +
    "        WHEN ITC.STATUSPRODCOT = 'C' THEN 'Cancelada' " +
    "        WHEN ITC.STATUSPRODCOT = 'P' THEN 'Precificada' " +
    "        WHEN ITC.STATUSPRODCOT = 'F' THEN 'Fechada' " +
    "        WHEN ITC.STATUSPRODCOT = 'O' THEN 'Aberta' " +
    "        WHEN ITC.STATUSPRODCOT = 'E' THEN 'Enviada' " +
    "        ELSE 'Sem status' " +
    "    END AS STATUS, " +
    "    CASE " +
    "        WHEN ITC.AD_DETCOMP = 1 THEN 'Venda Casada' " +
    "        WHEN ITC.AD_DETCOMP = 2 THEN 'Exportacao' " +
    "        WHEN ITC.AD_DETCOMP = 3 THEN 'Compra Estrategica' " +
    "        WHEN ITC.AD_DETCOMP = 4 THEN 'Balcao' " +
    "        WHEN ITC.AD_DETCOMP = 5 THEN 'Estoque' " +
    "        ELSE 'Sem status' " +
    "    END AS DETALHE_COMPRA " +
    "FROM TGFCOT COT " +
    "INNER JOIN TGFITC ITC ON ITC.NUMCOTACAO = COT.NUMCOTACAO " +
    "INNER JOIN TGFPRO PRO ON PRO.CODPROD = ITC.CODPROD " +
    "INNER JOIN TGFGRU GRU ON GRU.CODGRUPOPROD = PRO.CODGRUPOPROD " +
    "INNER JOIN TSIUSU USUC ON USUC.CODUSU = GRU.AD_CODUSU " +
    "INNER JOIN TSIUSU USU  ON USU.CODUSU  = COT.CODUSUREQ " +
    "LEFT JOIN AD_NUMCOTACAO ANC ON ANC.NUMCOTACAO = COT.NUMCOTACAO " +
    "LEFT JOIN TGFCAB CAB ON CAB.NUNOTA = ANC.NUNOTA " +
    "WHERE COT.DHINIC IS NOT NULL ";

    var params = [];
    var paramIdx = 0;

    // Se tem filtro por pedido ou cotação, ignora data
    if(nroPedido){
        query += "AND CAB.NUNOTA = ? ";
        params.push({value: nroPedido, type: "S"});
    } else if(numCotacao){
        query += "AND COT.NUMCOTACAO = ? ";
        params.push({value: numCotacao, type: "S"});
    } else {
        // Filtro de data só se não for pedido/cotação
        query += "AND COT.DHINIC BETWEEN ? AND ? ";
        params.push({value: dataIni + " 00:00:00", type: "D"});
        params.push({value: dataFim + " 23:59:59", type: "D"});
    }

    // Demais filtros
    query += "AND (GRU.AD_CODUSU = ? OR ? = 0) " +
             "AND (ITC.STATUSPRODCOT = ? OR ? = ' ') " +
             "AND (TO_CHAR(ITC.AD_DETCOMP) = ? OR ? = '0') " +
             "ORDER BY COT.DHINIC ASC";

    params.push({value: codComp, type: "I"});
    params.push({value: codComp, type: "I"});
    params.push({value: status,  type: "S"});
    params.push({value: status,  type: "S"});
    params.push({value: detalhe, type: "S"});
    params.push({value: detalhe, type: "S"});

    executeQuery(query, params, function(res){
        var dados = JSON.parse(res);
        document.getElementById('upd').textContent = "Atualizado: " + new Date().toLocaleTimeString('pt-BR');

        if(!dados || dados.length === 0){
            ALL = []; FIL = [];
            document.getElementById('b1').innerHTML = '<tr><td colspan="9" class="no-data">Nenhuma cotacao encontrada.</td></tr>';
            document.getElementById('b2').innerHTML = '<tr><td colspan="9" class="no-data">Nenhum dado encontrado.</td></tr>';
            atualizarMetricas();
            return;
        }

        ALL = dados.map(function(r){
            var td = parseFloat(r.TEMPO_DIAS);
            var th = parseFloat(r.TEMPO_HORAS);
            return {
                numcot:      r.NUMCOTACAO,
                nropedido:   r.NRO_UNICO_PEDIDO || '-',
                comprador:   r.COMPRADOR   || '-',
                codcomp:     r.COD_COMPRADOR || '',
                vendedor:    r.VENDEDOR    || '-',
                dhinic:      r.DHINIC ? new Date(r.DHINIC) : null,
                dhfinal:     r.AD_DATAFINAL ? new Date(r.AD_DATAFINAL) : null,
                dhinicFmt:   fmtDate(r.DHINIC),
                dhfinalFmt:  fmtDate(r.AD_DATAFINAL),
                tempoDias:   isNaN(td) ? null : td,
                tempoHoras:  isNaN(th) ? null : th,
                status:      r.STATUS      || 'Sem status',
                detalhe:     r.DETALHE_COMPRA || 'Sem status'
            };
        });

        FIL = ALL; pg = 1;
        atualizarMetricas();
        renderTabela();
        renderResumo();
        renderGraficos();

    }, function(err){
        document.getElementById('upd').textContent = "Erro ao carregar.";
        alert("Erro ao carregar dados:\n" + err);
    });
}

// ===== LIMPAR =====
function limpar(){
    document.getElementById('fnropedido').value = '';
    document.getElementById('fnumcotacao').value = '';
    limparComprador();
    document.getElementById('fstatus').value  = '';
    document.getElementById('fdetalhe').value = '';
}

// ===== METRICAS =====
function atualizarMetricas(){
    var fechadas   = FIL.filter(function(r){ return r.status === 'Fechada'; });
    var abertas    = FIL.filter(function(r){ return r.status === 'Aberta'; });
    var canceladas = FIL.filter(function(r){ return r.status === 'Cancelada'; });
    var tempos     = FIL.filter(function(r){ return r.tempoDias !== null; }).map(function(r){ return r.tempoDias; });
    var medTempo   = tempos.length ? (tempos.reduce(function(a,b){return a+b;},0) / tempos.length) : null;
    var temposHoras = FIL.filter(function(r){ return r.tempoHoras !== null; }).map(function(r){ return r.tempoHoras; });
    var medTempoHoras = temposHoras.length ? (temposHoras.reduce(function(a,b){return a+b;},0) / temposHoras.length) : null;
    var compradoras = new Set(FIL.map(function(r){ return r.comprador; })).size;

    document.getElementById('mTotal').textContent      = FIL.length;
    document.getElementById('mFechadas').textContent   = fechadas.length;
    document.getElementById('mAbertas').textContent    = abertas.length;
    document.getElementById('mCanceladas').textContent = canceladas.length;
    document.getElementById('mTempMed').textContent    = medTempo !== null ? medTempo.toFixed(1) : '-';
    document.getElementById('mTempMedHoras').textContent = medTempoHoras !== null ? medTempoHoras.toFixed(1) + 'h' : '-';
    document.getElementById('mCompradoras').textContent= compradoras;
}

// ===== SELECIONAR LINHA =====
function selecionarLinha(el){
    if(selectedRow) selectedRow.classList.remove('row-selected');
    el.classList.add('row-selected');
    selectedRow = el;
}

// ===== TABELA =====
function renderTabela(){
    var busca = (document.getElementById('tsrch').value || '').toLowerCase();
    var d = FIL.filter(function(r){
        if(!busca) return true;
        return String(r.numcot).toLowerCase().indexOf(busca) >= 0 ||
               String(r.nropedido).toLowerCase().indexOf(busca) >= 0 ||
               r.comprador.toLowerCase().indexOf(busca) >= 0 ||
               r.vendedor.toLowerCase().indexOf(busca) >= 0;
    });

    d.sort(function(a,b){
        var va=a[sortC], vb=b[sortC];
        if(sortC==='dhinic'||sortC==='dhfinal'){
            var ta = va ? va.getTime() : 0;
            var tb = vb ? vb.getTime() : 0;
            return sortD*(ta-tb);
        }
        if(va===null&&vb===null) return 0;
        if(va===null) return 1; if(vb===null) return -1;
        if(typeof va==='number') return sortD*(va-vb);
        return sortD*String(va).localeCompare(String(vb),'pt-BR');
    });

    var total=d.length, totalP=Math.ceil(total/PP)||1;
    if(pg>totalP) pg=totalP;
    var pag=d.slice((pg-1)*PP, pg*PP);

    document.getElementById('tcnt').textContent = total+' registro(s)';
    document.getElementById('pinfo').textContent = 'Pagina '+pg+' de '+totalP+' ('+total+' registros)';

    var b1 = document.getElementById('b1');
    b1.innerHTML = pag.length===0
        ? '<tr><td colspan="9" class="no-data">Nenhum registro encontrado.</td></tr>'
        : pag.map(function(r){
            var tCls = tempoCls(r.tempoDias);
            return '<tr onclick="selecionarLinha(this)">'+
                '<td><strong style="color:#185FA5;cursor:pointer" onclick="abrirCotacao('+r.numcot+')">'+r.numcot+'</strong></td>'+
                '<td><strong style="color:#185FA5;cursor:pointer" onclick="abrirPedido('+r.nropedido+')">'+r.nropedido+'</strong></td>'+
                '<td>'+r.comprador+'</td>'+
                '<td>'+r.vendedor+'</td>'+
                '<td>'+r.dhinicFmt+'</td>'+
                '<td>'+r.dhfinalFmt+'</td>'+
                '<td style="text-align:right" class="'+tCls+'">'+fmtTempo(r.tempoDias)+'</td>'+
                '<td style="text-align:right">'+( r.tempoHoras !== null ? r.tempoHoras.toFixed(1)+'h' : '-' )+'</td>'+
                '<td>'+badgeStatus(r.status)+'</td>'+
                '<td>'+badgeDetalhe(r.detalhe)+'</td>'+
            '</tr>';
          }).join('');

    renderPagina(totalP);
}

// ===== RESUMO POR COMPRADORA =====
function renderResumo(){
    var map = {};
    FIL.forEach(function(r){
        var k = r.comprador;
        if(!map[k]) map[k] = {comprador:k, total:0, abertas:0, fechadas:0, aprovadas:0, canceladas:0, precificadas:0, enviadas:0, tempos:[]};
        map[k].total++;
        if(r.status==='Aberta')      map[k].abertas++;
        if(r.status==='Fechada')     map[k].fechadas++;
        if(r.status==='Aprovada')    map[k].aprovadas++;
        if(r.status==='Cancelada')   map[k].canceladas++;
        if(r.status==='Precificada') map[k].precificadas++;
        if(r.status==='Enviada')     map[k].enviadas++;
        if(r.tempoDias!==null) map[k].tempos.push(r.tempoDias);
    });

    var rows = Object.values(map).sort(function(a,b){ return b.total - a.total; });
    var b2 = document.getElementById('b2');
    b2.innerHTML = rows.length===0
        ? '<tr><td colspan="9" class="no-data">Nenhum dado.</td></tr>'
        : rows.map(function(row){
            var med = row.tempos.length ? (row.tempos.reduce(function(a,b){return a+b;},0)/row.tempos.length) : null;
            var mCls = tempoCls(med);
            return '<tr onclick="selecionarLinha(this)">'+
                '<td><strong>'+row.comprador+'</strong></td>'+
                '<td style="text-align:right"><strong>'+row.total+'</strong></td>'+
                '<td style="text-align:right;color:var(--blue)">'+row.abertas+'</td>'+
                '<td style="text-align:right;color:var(--teal-dark)">'+row.fechadas+'</td>'+
                '<td style="text-align:right;color:#2E7D32">'+row.aprovadas+'</td>'+
                '<td style="text-align:right;color:var(--red)">'+row.canceladas+'</td>'+
                '<td style="text-align:right;color:var(--amber)">'+row.precificadas+'</td>'+
                '<td style="text-align:right;color:var(--purple)">'+row.enviadas+'</td>'+
                '<td style="text-align:right" class="'+mCls+'">'+(med!==null?med.toFixed(1)+'d':'-')+'</td>'+
            '</tr>';
        }).join('');
}

function renderPagina(totalP){
    var el=document.getElementById('pbts');
    el.innerHTML='';
    for(var i=1;i<=totalP;i++){
        el.innerHTML+='<button class="pb'+(i===pg?' act':'')+'" onclick="irPag('+i+')">'+i+'</button>';
    }
}

// abrir pedido
function abrirPedido(nunota){
  openApp('br.com.sankhya.com.mov.CentralNotas',{
      NUNOTA: nunota
  });
}

// abrir cotacao
function abrirCotacao(numcot){
  openApp('br.com.sankhya.swb.cotacao.rotinas.cotacao',{
      NUMCOTACAO: numcot
  });
}
function irPag(n){ pg=n; renderTabela(); }

// ===== ORDENACAO =====
function srt(col){
    if(sortC===col) sortD*=-1; else { sortC=col; sortD=1; }
    renderTabela();
}

// ===== GRAFICOS =====
var CORES_STATUS = {
    'Aberta':    '#185FA5',
    'Fechada':   '#1D9E75',
    'Aprovada':  '#2E7D32',
    'Cancelada': '#A32D2D',
    'Precificada':'#BA7517',
    'Enviada':   '#6B3FA0',
    'Sem status':'#888780'
};
var CORES_BARRA = ['#185FA5','#1D9E75','#BA7517','#A32D2D','#6B3FA0','#C46C1A','#2A7A9B','#3D7A3D'];

function renderGraficos(){
    // ---- CHART 1: Status por compradora (stacked bar) ----
    var comps = Array.from(new Set(FIL.map(function(r){ return r.comprador; }))).sort();
    var statusList = ['Aberta','Fechada','Aprovada','Cancelada','Precificada','Enviada'];

    var datasets = statusList.map(function(st){
        return {
            label: st,
            data: comps.map(function(c){
                return FIL.filter(function(r){ return r.comprador===c && r.status===st; }).length;
            }),
            backgroundColor: CORES_STATUS[st],
            borderRadius: 3
        };
    });

    // Shorten labels
    var shortLabels = comps.map(function(c){
        var parts = c.split(' - ');
        return parts.length > 1 ? parts[1].split(' ')[0] : c.substring(0,12);
    });

    if(chartStatus) chartStatus.destroy();
    chartStatus = new Chart(document.getElementById('cStatus'), {
        type: 'bar',
        data: { labels: shortLabels, datasets: datasets },
        options: {
            responsive: true, maintainAspectRatio: false,
            plugins: {
                legend: { position: 'bottom', labels: { boxWidth: 10, font: { size: 10 } } }
            },
            scales: {
                x: { stacked: true },
                y: { stacked: true, beginAtZero: true }
            }
        }
    });

    // ---- CHART 2: Tempo medio por compradora ----
    var tempoData = comps.map(function(c){
        var ts = FIL.filter(function(r){ return r.comprador===c && r.tempoDias!==null; }).map(function(r){ return r.tempoDias; });
        return ts.length ? (ts.reduce(function(a,b){return a+b;},0)/ts.length) : 0;
    });

    if(chartTempo) chartTempo.destroy();
    chartTempo = new Chart(document.getElementById('cTempo'), {
        type: 'bar',
        data: {
            labels: shortLabels,
            datasets: [{
                data: tempoData,
                backgroundColor: tempoData.map(function(v){
                    if(v<=3) return '#1D9E75';
                    if(v<=7) return '#BA7517';
                    return '#A32D2D';
                }),
                borderRadius: 4
            }]
        },
        options: {
            responsive: true, maintainAspectRatio: false,
            plugins: { legend: { display: false } },
            scales: { y: { beginAtZero: true, title: { display: true, text: 'Dias', font: { size: 10 } } } }
        }
    });

    // ---- CHART 3: Cotacoes por dia (line) ----
    var porDia = {};
    FIL.forEach(function(r){
        if(r.dhinicFmt && r.dhinicFmt !== '-'){
            porDia[r.dhinicFmt] = (porDia[r.dhinicFmt]||0) + 1;
        }
    });
    var dias = Object.keys(porDia).sort(function(a,b){
        return new Date(a.split('/').reverse().join('-')) - new Date(b.split('/').reverse().join('-'));
    });

    if(chartLine) chartLine.destroy();
    chartLine = new Chart(document.getElementById('cLine'), {
        type: 'line',
        data: {
            labels: dias,
            datasets: [{
                label: 'Cotacoes abertas',
                data: dias.map(function(k){ return porDia[k]; }),
                borderColor: '#185FA5',
                backgroundColor: 'rgba(24,95,165,0.12)',
                borderWidth: 2, pointRadius: 3, tension: 0.3, fill: true
            }]
        },
        options: {
            responsive: true, maintainAspectRatio: false,
            plugins: { legend: { display: false } },
            scales: { y: { beginAtZero: true } }
        }
    });
}

// ===== ABAS =====
function swtab(el, id){
    document.querySelectorAll('.tab').forEach(function(t){ t.classList.remove('act'); });
    document.querySelectorAll('.tc').forEach(function(t){ t.classList.remove('act'); });
    el.classList.add('act');
    document.getElementById(id).classList.add('act');
}

// ===== FULLSCREEN =====
function toggleTableFullscreen(){
    var layout = document.querySelector('.layout');
    var card = document.querySelector('.table-card');
    var btn = document.getElementById('btnFullscreen');
    var inFull = card.classList.toggle('fullscreen');
    layout.classList.toggle('fullscreen', inFull);
    btn.innerHTML = inFull ? '&#x2715;' : '&#x26F6;';
}

// ===== EXPORTAR CSV =====
function exportCSV(){
    if(FIL.length===0){ alert("Sem dados para exportar."); return; }
    function esc(v){ return '"'+String(v==null?'':v).replace(/"/g,'""')+'"'; }
    var SEP = ";";
    var header = ["Num.Cotacao", "Num. Pedido", "Compradora", "Vendedor", "Data Inicio", "Data Fim", "Tempo (dias)", "Tempo (horas)", "Status", "Detalhe Compra"];
    var linhas = FIL.map(function(r){
        return [
            esc(r.numcot), esc(r.nropedido), esc(r.comprador), esc(r.vendedor),
            esc(r.dhinicFmt), esc(r.dhfinalFmt),
            esc(r.tempoDias !== null ? r.tempoDias.toFixed(2).replace('.',',') : ''),
            esc(r.tempoHoras !== null ? r.tempoHoras.toFixed(2).replace('.',',') : ''),
            esc(r.status), esc(r.detalhe)
        ].join(SEP);
    });
    var csv = "sep=;\r\n" + header.map(esc).join(SEP) + "\r\n" + linhas.join("\r\n");
    var blob = new Blob(["\uFEFF"+csv], {type:'text/csv;charset=utf-8;'});
    var url = URL.createObjectURL(blob);
    var a = document.createElement('a');
    a.href=url; a.download='ciclo_compras.csv';
    a.style.display='none';
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
}

</script>
</body>
</html>
