import { useState } from "react";

const HISTORIAL_INICIAL = [
  // ── 10 DE MAYO ──────────────────────────────────────────────────────
  { id:1,  fecha:"2026-05-10", campaña:"Chamarra 10 mayo",  producto:"Chamarra de Gamuza NORA",  inversion:51,  cpc:0.26, atc:8,  pur:1, uds:2, price:63.85, descPct:0, cog:23 },
  { id:2,  fecha:"2026-05-10", campaña:"Colección 10 mayo", producto:"Chamarra de Gamuza NORA",  inversion:50,  cpc:1.21, atc:6,  pur:1, uds:1, price:63.80, descPct:0, cog:23 },
  { id:3,  fecha:"2026-05-10", campaña:"Camisa 10 mayo",    producto:"ORION Sobrecamisa Urbana", inversion:30,  cpc:1.72, atc:2,  pur:1, uds:2, price:44.67, descPct:0, cog:16 },
  { id:4,  fecha:"2026-05-10", campaña:"Botas 10 mayo",     producto:"Botas Chelsea Rignora",    inversion:30,  cpc:1.80, atc:0,  pur:1, uds:1, price:58.02, descPct:0, cog:25 },
  { id:5,  fecha:"2026-05-10", campaña:"Zapatos 10 mayo",   producto:"Zapatos",                  inversion:30,  cpc:1.28, atc:0,  pur:0, uds:0, price:50,    descPct:0, cog:20 },
  // ── 11 DE MAYO ──────────────────────────────────────────────────────
  { id:6,  fecha:"2026-05-11", campaña:"Chamarra 10 mayo",  producto:"Chamarra de Gamuza NORA",  inversion:51,  cpc:0.27, atc:10, pur:2, uds:3, price:71.15, descPct:0, cog:23 },
  { id:7,  fecha:"2026-05-11", campaña:"Colección 10 mayo", producto:"Chamarra de Gamuza NORA",  inversion:50,  cpc:0.87, atc:9,  pur:2, uds:2, price:71.15, descPct:0, cog:23 },
  { id:8,  fecha:"2026-05-11", campaña:"Camisa 10 mayo",    producto:"ORION Sobrecamisa Urbana", inversion:30,  cpc:1.58, atc:2,  pur:0, uds:0, price:44.67, descPct:0, cog:16 },
  // ── 12 DE MAYO ──────────────────────────────────────────────────────
  { id:9,  fecha:"2026-05-12", campaña:"Chamarra 10 mayo",  producto:"Chamarra de Gamuza NORA",  inversion:51,  cpc:0.33, atc:13, pur:2, uds:2, price:65.70, descPct:0, cog:23 },
  { id:10, fecha:"2026-05-12", campaña:"Colección 10 mayo", producto:"Reloj Legacy de cuero",    inversion:50,  cpc:0.56, atc:5,  pur:1, uds:1, price:39.41, descPct:0, cog:13 },
  { id:11, fecha:"2026-05-12", campaña:"Camisa 10 mayo",    producto:"ORION Sobrecamisa Urbana", inversion:30,  cpc:0.90, atc:0,  pur:0, uds:0, price:44.67, descPct:0, cog:16 },
  // ── 17 DE MAYO ──────────────────────────────────────────────────────
  { id:15, fecha:"2026-05-17", campaña:"Trio NORA 17 de mayo", producto:"Chamarra de Gamuza NORA", inversion:61, cpc:0.32, atc:8, pur:2, uds:2, price:74.77, descPct:0, cog:23 },
  { id:12, fecha:"2026-05-13", campaña:"Chamarra 10 mayo",  producto:"Chamarra de Gamuza NORA",  inversion:51,  cpc:0.24, atc:5,  pur:1, uds:1, price:44.74, descPct:0, cog:16 },
  { id:13, fecha:"2026-05-13", campaña:"Colección 10 mayo", producto:"Chamarra de Gamuza NORA",  inversion:50,  cpc:0.47, atc:4,  pur:0, uds:0, price:63.85, descPct:0, cog:23 },
  { id:14, fecha:"2026-05-13", campaña:"Camisa 10 mayo",    producto:"ORION Sobrecamisa Urbana", inversion:30,  cpc:0,    atc:0,  pur:0, uds:0, price:44.74, descPct:0, cog:16 },
];

const NUM = v => parseFloat(v) || 0;

function calcRow(r) {
  const uds        = NUM(r.uds);
  const descMult   = 1 - (r.descPct||0) / 100;
  const precioReal = r.price * descMult;
  const descTotal  = r.price * (r.descPct||0) / 100 * uds;
  const valTienda  = uds * precioReal;
  const cogT       = uds * r.cog;
  const comision   = valTienda * ((r.comisionPct||5.4) / 100);
  const margenUnit = r.price - r.cog;
  const ber        = margenUnit > 0 ? r.price / margenUnit : 0;
  const roas       = r.inversion > 0 ? valTienda / r.inversion : 0;
  const cpa        = r.pur > 0 ? r.inversion / r.pur : 0;
  const margenEur  = valTienda - cogT - r.inversion - comision;
  const margenPct  = valTienda > 0 ? (margenEur / valTienda) * 100 : (r.inversion > 0 ? -100 : 0);
  return { valTienda, cogT, comision, margenUnit, ber, roas, cpa, margenEur, margenPct, precioReal, descTotal };
}

function calcGroup(rows) {
  const inv       = rows.reduce((a,r)=>a+r.inversion,0);
  const pur       = rows.reduce((a,r)=>a+r.pur,0);
  const uds       = rows.reduce((a,r)=>a+(r.uds||0),0);
  const atc       = rows.reduce((a,r)=>a+r.atc,0);
  const valTienda = rows.reduce((a,r)=>a+calcRow(r).valTienda,0);
  const cogT      = rows.reduce((a,r)=>a+calcRow(r).cogT,0);
  const com       = rows.reduce((a,r)=>a+calcRow(r).comision,0);
  const margenEur = rows.reduce((a,r)=>a+calcRow(r).margenEur,0);
  const margenPct = valTienda>0?(margenEur/valTienda)*100:(inv>0?-100:0);
  const roas      = inv>0?valTienda/inv:0;
  const cpa       = pur>0?inv/pur:0;
  const dias      = [...new Set(rows.map(r=>r.fecha))].length;
  return {inv,pur,uds,atc,valTienda,cogT,com,margenEur,margenPct,roas,cpa,dias};
}

function getVerdict(g) {
  const {inv,pur,margenPct,roas,atc,dias} = g;
  if (!inv) return null;
  if (pur===0&&inv>=30&&atc===0) return {label:"Apagar",color:"#A32D2D",bg:"#FCEBEB",icon:"✕",action:"Sin ATC con +$30 gastado. Problema de landing o producto."};
  if (pur===0&&inv>=30) return {label:"Apagar",color:"#A32D2D",bg:"#FCEBEB",icon:"✕",action:"Sin ventas con +$30 USD gastado. Para según regla PDF."};
  if (margenPct>=30&&dias>=2) return {label:"Escalar agresivo",color:"#1a7a1a",bg:"#EAF3DE",icon:"↑↑",action:"+30% margen por 2+ días. Sube al siguiente paso de presupuesto."};
  if (margenPct>=15&&dias>=2) return {label:"Escalar",color:"#2d8f2d",bg:"#EAF3DE",icon:"↑",action:"+15% margen por 2+ días. Condición de escalado cumplida."};
  if (margenPct>=0) return {label:"Break-even",color:"#854F0B",bg:"#FAEEDA",icon:"≈",action:"Dale 1 día más antes de decidir."};
  if (pur>=1&&margenPct<0) return {label:"Pérdidas",color:"#A32D2D",bg:"#FCEBEB",icon:"↓",action:"Tiene ventas pero en pérdidas. Revisa precio o reduce inversión."};
  return {label:"Evaluar",color:"#854F0B",bg:"#FAEEDA",icon:"?",action:"Señales mixtas. Analiza métricas antes de decidir."};
}

const rcol = r=>r>=2.5?{bg:"#1a7a1a",t:"#fff"}:r>=2?{bg:"#2d8f2d",t:"#fff"}:r>=1.5?{bg:"#e6a817",t:"#fff"}:{bg:"#c0392b",t:"#fff"};
const mcol = m=>m>=20?{bg:"#EAF3DE",t:"#3B6D11"}:m>=0?{bg:"#FAEEDA",t:"#854F0B"}:{bg:"#FCEBEB",t:"#A32D2D"};
const fD   = v=>"$"+Math.abs(NUM(v)).toFixed(2);
const fX   = v=>NUM(v).toFixed(2)+"x";
const fP   = v=>(NUM(v)>=0?"+":"")+NUM(v).toFixed(1)+"%";
const sgn  = v=>v>=0?"+":"-";

const EMPTY = {fecha:"2026-05-13",campaña:"",producto:"",inversion:"",cpc:"",atc:"",pur:"",uds:"",price:"",descPct:"0",cog:""};

export default function App() {
  const [hist,setHist]           = useState(HISTORIAL_INICIAL);
  const [form,setForm]           = useState(EMPTY);
  const [showForm,setShowForm]   = useState(false);
  const [view,setView]           = useState("dia");
  const [fechaSel,setFechaSel]   = useState("2026-05-10");
  const [prodSel,setProdSel]     = useState("Chamarra de Gamuza NORA");
  const [campSel,setCampSel]     = useState("Chamarra 10 mayo");

  const fechas    = [...new Set(hist.map(r=>r.fecha))].sort();
  const productos = [...new Set(hist.map(r=>r.producto))].sort();
  const campañas  = [...new Set(hist.map(r=>r.campaña))].sort();

  const updRow = (id,f,v) => setHist(h=>h.map(x=>x.id===id?{...x,[f]:v}:x));
  const addRow = () => {
    if(!form.inversion||!form.price||!form.cog||!form.producto||!form.campaña) return;
    setHist(h=>[...h,{...form,id:Date.now(),inversion:NUM(form.inversion),cpc:NUM(form.cpc),atc:NUM(form.atc),pur:NUM(form.pur),uds:NUM(form.uds)||NUM(form.pur),price:NUM(form.price),descPct:NUM(form.descPct),cog:NUM(form.cog)}]);
    setShowForm(false); setForm(EMPTY);
  };
  const delRow = id=>setHist(h=>h.filter(r=>r.id!==id));

  const th    = {background:"#1a1a2e",color:"#c8d6e5",padding:"7px 6px",fontSize:11,fontWeight:600,textAlign:"center",borderRight:"1px solid #2d3561",whiteSpace:"nowrap"};
  const thy   = {background:"#2d3561",color:"#fff9d6",padding:"7px 6px",fontSize:11,fontWeight:600,textAlign:"center",borderRight:"1px solid #3d4571",whiteSpace:"nowrap"};
  const td    = {background:"#f8f9fa",padding:"6px 6px",fontSize:12,textAlign:"center",borderRight:"1px solid #dee2e6",borderBottom:"1px solid #dee2e6",whiteSpace:"nowrap"};
  const tdy   = {background:"#fff9d6",padding:"6px 6px",fontSize:12,textAlign:"center",borderRight:"1px solid #dee2e6",borderBottom:"1px solid #dee2e6",whiteSpace:"nowrap"};
  const tf    = {background:"#1a1a2e",color:"#fff",padding:"7px 6px",fontSize:12,fontWeight:700,textAlign:"center",borderRight:"1px solid #2d3561",whiteSpace:"nowrap"};
  const inp   = {width:"100%",padding:"7px 10px",border:"0.5px solid #ccc",borderRadius:6,fontSize:13,background:"#fff",color:"#222",boxSizing:"border-box"};
  const lbl   = {fontSize:12,color:"#666",display:"block",marginBottom:3};
  const iCell = {width:"100%",border:"none",background:"transparent",fontSize:12,textAlign:"center",outline:"none",color:"inherit",padding:0,fontFamily:"inherit"};
  const tab   = a=>({padding:"7px 14px",fontSize:13,fontWeight:a?600:400,borderRadius:7,border:"none",background:a?"#1a1a2e":"#e2e8f0",color:a?"#fff":"#555",cursor:"pointer"});

  const Cards = ({g}) => (
    <div style={{display:"grid",gridTemplateColumns:"repeat(auto-fit,minmax(120px,1fr))",gap:8,marginBottom:12}}>
      {[
        {l:"Inversión ads",       v:fD(g.inv),   s:"gasto en Meta"},
        {l:"Pedidos · Unidades",  v:g.pur+" ped · "+g.uds+" uds", s:fD(g.valTienda)+" ingresos"},
        {l:"ROAS",                v:fX(g.roas),  s:"retorno ads", col:rcol(g.roas)},
        {l:"COG — Proveedor",     v:fD(g.cogT),  s:"deuda proveedor"},
        {l:"Margen $",            v:sgn(g.margenEur)+fD(g.margenEur), s:fP(g.margenPct)+" sobre ventas", col:mcol(g.margenPct), m:g.margenEur},
      ].map((c,i)=>(
        <div key={i} style={{background:c.col?c.col.bg:"#fff",borderRadius:8,padding:"0.7rem 0.875rem",boxShadow:"0 1px 4px rgba(0,0,0,0.08)"}}>
          <div style={{fontSize:11,color:c.col?c.col.t:"#888",marginBottom:2}}>{c.l}</div>
          <div style={{fontSize:17,fontWeight:700,color:c.col?c.col.t:c.m!==undefined?(c.m>=0?"#1a7a1a":"#c0392b"):"#1a1a2e"}}>{c.v}</div>
          <div style={{fontSize:11,color:c.col?c.col.t:"#aaa",marginTop:2,opacity:.85}}>{c.s}</div>
        </div>
      ))}
    </div>
  );

  const Tabla = ({rows,showFecha=true,showProducto=true,showCampaña=true}) => {
    if(!rows.length) return <div style={{textAlign:"center",padding:"2rem",color:"#888",fontSize:13,background:"#fff",borderRadius:10}}>Sin datos.</div>;
    const g=calcGroup(rows);
    return (
      <div style={{overflowX:"auto",borderRadius:10,boxShadow:"0 2px 8px rgba(0,0,0,0.08)"}}>
        <table style={{borderCollapse:"collapse",width:"100%",minWidth:900}}>
          <thead>
            <tr>
              <th style={th}>Nº</th>
              {showFecha    && <th style={thy}>Fecha</th>}
              {showCampaña  && <th style={thy}>Campaña</th>}
              {showProducto && <th style={thy}>Producto</th>}
              <th style={thy}>Inversión ($)</th>
              <th style={thy}>CPC ($)</th>
              <th style={thy}>ATC</th>
              <th style={thy}>PUR</th>
              <th style={th}>BER</th>
              <th style={th}>ROAS</th>
              <th style={th}>CPA ($)</th>
              <th style={thy}>PRICE ($)</th>
              <th style={thy}>COG ($)</th>
              <th style={th}>Mg unit ($)</th>
              <th style={thy}>Unid.</th>
              <th style={th}>Total COG ($)</th>
              <th style={th}>Valor Tienda ($)</th>
              <th style={thy}>Desc (%)</th>
              <th style={thy}>Comisión (%)</th>
              <th style={th}>Margen $</th>
              <th style={th}>Margen (%)</th>
              <th style={th}></th>
            </tr>
          </thead>
          <tbody>
            {rows.map((r,i)=>{
              const c=calcRow(r);const rc=rcol(c.roas);const mc=mcol(c.margenPct);
              return (
                <tr key={r.id} style={{background:i%2===0?"#fff":"#f5f7fa"}}>
                  <td style={{...td,color:"#aaa"}}>{i+1}</td>
                  {showFecha   && <td style={tdy}><input style={{...iCell}} value={r.fecha} onChange={e=>updRow(r.id,"fecha",e.target.value)}/></td>}
                  {showCampaña && <td style={{...tdy,textAlign:"left"}}><input style={{...iCell,color:"#7B3FB5",fontWeight:500}} value={r.campaña} onChange={e=>updRow(r.id,"campaña",e.target.value)}/></td>}
                  {showProducto&& <td style={{...tdy,textAlign:"left"}}><input style={{...iCell,color:"#185FA5",fontWeight:500}} value={r.producto} onChange={e=>updRow(r.id,"producto",e.target.value)}/></td>}
                  <td style={tdy}><input style={iCell} type="number" value={r.inversion} onChange={e=>updRow(r.id,"inversion",NUM(e.target.value))}/></td>
                  <td style={tdy}><input style={{...iCell,color:r.cpc<=0.4?"#1a7a1a":r.cpc<=0.74?"#854F0B":"#c0392b",fontWeight:500}} type="number" value={r.cpc} onChange={e=>updRow(r.id,"cpc",NUM(e.target.value))}/></td>
                  <td style={tdy}><input style={{...iCell,color:r.atc>=5?"#1a7a1a":"#854F0B"}} type="number" value={r.atc} onChange={e=>updRow(r.id,"atc",NUM(e.target.value))}/></td>
                  <td style={tdy}><input style={iCell} type="number" value={r.pur} onChange={e=>updRow(r.id,"pur",NUM(e.target.value))}/></td>
                  <td style={td}>{r.uds>0?fX(c.ber):"—"}</td>
                  <td style={{...td,background:r.uds>0?rc.bg:"#FCEBEB",color:r.uds>0?rc.t:"#A32D2D",fontWeight:700}}>{fX(c.roas)}</td>
                  <td style={td}>{c.cpa>0?fD(c.cpa):"—"}</td>
                  <td style={tdy}><input style={iCell} type="number" value={r.price} onChange={e=>updRow(r.id,"price",NUM(e.target.value))}/></td>
                  <td style={tdy}><input style={iCell} type="number" value={r.cog} onChange={e=>updRow(r.id,"cog",NUM(e.target.value))}/></td>
                  <td style={td}>{r.uds>0?fD(c.margenUnit):"—"}</td>
                  <td style={tdy}><input style={iCell} type="number" value={r.uds} onChange={e=>updRow(r.id,"uds",NUM(e.target.value))}/></td>
                  <td style={{...td,color:"#c0392b",fontWeight:500}}>{fD(c.cogT)}</td>
                  <td style={td}>{fD(c.valTienda)}</td>
                  <td style={tdy}><input style={{...iCell,color:(r.descPct||0)>0?"#854F0B":"#aaa"}} type="number" value={r.descPct||0} onChange={e=>updRow(r.id,"descPct",NUM(e.target.value))}/></td>
                  <td style={tdy}><input style={{...iCell,color:"#854F0B"}} type="number" step="0.1" value={r.comisionPct||5.4} onChange={e=>updRow(r.id,"comisionPct",NUM(e.target.value))}/></td>
                  <td style={{...td,color:c.margenEur>=0?"#1a7a1a":"#c0392b",fontWeight:700}}>{sgn(c.margenEur)}{fD(c.margenEur)}</td>
                  <td style={{...td,background:mc.bg,color:mc.t,fontWeight:700}}>{fP(c.margenPct)}</td>
                  <td style={{...td,cursor:"pointer",color:"#c0392b",fontWeight:700}} onClick={()=>delRow(r.id)}>✕</td>
                </tr>
              );
            })}
          </tbody>
          <tfoot>
            <tr>
              <td style={tf}>∑</td>
              {showFecha   &&<td style={tf}>TOTALES</td>}
              {showCampaña &&<td style={tf}>{!showFecha?"TOTALES":""}</td>}
              {showProducto&&<td style={tf}>{!showFecha&&!showCampaña?"TOTALES":""}</td>}
              <td style={tf}>{fD(g.inv)}</td>
              <td style={tf}>—</td>
              <td style={tf}>{g.atc}</td>
              <td style={tf}>{g.pur}</td>
              <td style={tf}>—</td>
              <td style={{...tf,background:rcol(g.roas).bg}}>{fX(g.roas)}</td>
              <td style={tf}>{g.cpa>0?fD(g.cpa):"—"}</td>
              <td style={tf}>—</td>
              <td style={tf}>—</td>
              <td style={tf}>—</td>
              <td style={tf}>{g.uds}</td>
              <td style={{...tf,color:"#ff9999"}}>{fD(g.cogT)}</td>
              <td style={tf}>{fD(g.valTienda)}</td>
              <td style={tf}>—</td>
              <td style={{...tf,color:"#ffcc88"}}>{fD(g.com)}</td>
              <td style={{...tf,color:g.margenEur>=0?"#7ddb7d":"#ff8080"}}>{sgn(g.margenEur)}{fD(g.margenEur)}</td>
              <td style={{...tf,background:mcol(g.margenPct).bg,color:mcol(g.margenPct).t}}>{fP(g.margenPct)}</td>
              <td style={tf}></td>
            </tr>
          </tfoot>
        </table>
      </div>
    );
  };

  // Vista por fecha
  const ViewDia = () => {
    const rows=hist.filter(r=>r.fecha===fechaSel).sort((a,b)=>a.campaña.localeCompare(b.campaña));
    return (
      <div>
        <div style={{display:"flex",alignItems:"center",gap:10,marginBottom:12,flexWrap:"wrap"}}>
          <span style={{fontSize:13,color:"#555",fontWeight:500}}>Fecha:</span>
          <select value={fechaSel} onChange={e=>setFechaSel(e.target.value)} style={{...inp,width:"auto"}}>
            {fechas.map(f=><option key={f} value={f}>{f}</option>)}
          </select>
          <span style={{fontSize:12,color:"#888"}}>{rows.length} campañas ese día</span>
        </div>
        <Cards g={calcGroup(rows)}/>
        <Tabla rows={rows} showFecha={false}/>
      </div>
    );
  };

  // Vista por campaña
  const ViewCampaña = () => {
    const rows=hist.filter(r=>r.campaña===campSel).sort((a,b)=>a.fecha.localeCompare(b.fecha));
    const g=calcGroup(rows);
    const v=getVerdict(g);
    return (
      <div>
        <div style={{display:"flex",alignItems:"center",gap:10,marginBottom:12,flexWrap:"wrap"}}>
          <span style={{fontSize:13,color:"#555",fontWeight:500}}>Campaña:</span>
          <select value={campSel} onChange={e=>setCampSel(e.target.value)} style={{...inp,width:"auto"}}>
            {campañas.map(c=><option key={c} value={c}>{c}</option>)}
          </select>
          <span style={{fontSize:12,color:"#888"}}>{g.dias} días activa</span>
        </div>
        <Cards g={g}/>
        {v&&<div style={{borderRadius:8,padding:"0.7rem 1rem",background:v.bg,marginBottom:12}}>
          <span style={{fontWeight:700,color:v.color,fontSize:14}}>{v.icon} {v.label}: </span>
          <span style={{fontSize:13,color:v.color}}>{v.action}</span>
        </div>}
        <Tabla rows={rows} showCampaña={false}/>
      </div>
    );
  };

  // Vista por producto
  const ViewProducto = () => {
    const rows=hist.filter(r=>r.producto===prodSel).sort((a,b)=>a.fecha.localeCompare(b.fecha));
    return (
      <div>
        <div style={{display:"flex",alignItems:"center",gap:10,marginBottom:12,flexWrap:"wrap"}}>
          <span style={{fontSize:13,color:"#555",fontWeight:500}}>Producto:</span>
          <select value={prodSel} onChange={e=>setProdSel(e.target.value)} style={{...inp,width:"auto"}}>
            {productos.map(p=><option key={p} value={p}>{p}</option>)}
          </select>
          <span style={{fontSize:12,color:"#888"}}>{[...new Set(rows.map(r=>r.fecha))].length} días</span>
        </div>
        <Cards g={calcGroup(rows)}/>
        <Tabla rows={rows} showProducto={false}/>
      </div>
    );
  };

  // Vista global
  const ViewGlobal = () => {
    const g=calcGroup(hist);
    // Ranking campañas
    const rankCamp=campañas.map(c=>{
      const rows=hist.filter(r=>r.campaña===c);
      const pg=calcGroup(rows);
      const v=getVerdict(pg);
      return {...pg,nombre:c,veredicto:v};
    }).sort((a,b)=>b.margenEur-a.margenEur);
    // Ranking productos
    const rankProd=productos.map(p=>{
      const rows=hist.filter(r=>r.producto===p);
      const pg=calcGroup(rows);
      return {...pg,nombre:p};
    }).sort((a,b)=>b.margenEur-a.margenEur);

    return (
      <div>
        <div style={{fontSize:12,color:"#888",marginBottom:8}}>Acumulado total desde inicio</div>
        <Cards g={g}/>

        <div style={{fontSize:12,fontWeight:600,color:"#555",textTransform:"uppercase",letterSpacing:".06em",margin:"1rem 0 .5rem"}}>🎯 Ranking por campaña</div>
        <div style={{overflowX:"auto",borderRadius:10,boxShadow:"0 2px 8px rgba(0,0,0,0.08)",marginBottom:16}}>
          <table style={{borderCollapse:"collapse",width:"100%",minWidth:600}}>
            <thead><tr>{["Campaña","Días","Inversión","Pedidos","Uds","Ingresos","COG","Comisión","ROAS","CPA","Margen $","Margen (%)","Veredicto"].map((h,i)=><th key={i} style={th}>{h}</th>)}</tr></thead>
            <tbody>
              {rankCamp.map((r,i)=>{
                const rc=rcol(r.roas),mc=mcol(r.margenPct);
                return (
                  <tr key={i} style={{background:i%2===0?"#fff":"#f5f7fa"}}>
                    <td style={{...td,textAlign:"left",fontWeight:600,color:"#7B3FB5"}}>{r.nombre}</td>
                    <td style={td}>{r.dias}</td>
                    <td style={td}>{fD(r.inv)}</td>
                    <td style={td}>{r.pur}</td>
                    <td style={td}>{r.uds}</td>
                    <td style={td}>{fD(r.valTienda)}</td>
                    <td style={{...td,color:"#c0392b",fontWeight:500}}>{fD(r.cogT)}</td>
                    <td style={{...td,color:"#854F0B"}}>{fD(r.com)}</td>
                    <td style={{...td,background:rc.bg,color:rc.t,fontWeight:700}}>{fX(r.roas)}</td>
                    <td style={td}>{r.cpa>0?fD(r.cpa):"—"}</td>
                    <td style={{...td,color:r.margenEur>=0?"#1a7a1a":"#c0392b",fontWeight:700}}>{sgn(r.margenEur)}{fD(r.margenEur)}</td>
                    <td style={{...td,background:mc.bg,color:mc.t,fontWeight:700}}>{fP(r.margenPct)}</td>
                    <td style={{...td,background:r.veredicto?.bg,color:r.veredicto?.color,fontWeight:600}}>{r.veredicto?`${r.veredicto.icon} ${r.veredicto.label}`:"—"}</td>
                  </tr>
                );
              })}
            </tbody>
            <tfoot><tr>
              <td style={tf}>∑ TOTAL</td><td style={tf}>—</td>
              <td style={tf}>{fD(g.inv)}</td><td style={tf}>{g.pur}</td><td style={tf}>{g.uds}</td>
              <td style={tf}>{fD(g.valTienda)}</td>
              <td style={{...tf,color:"#ff9999"}}>{fD(g.cogT)}</td>
              <td style={{...tf,color:"#ffcc88"}}>{fD(g.com)}</td>
              <td style={{...tf,background:rcol(g.roas).bg}}>{fX(g.roas)}</td>
              <td style={tf}>{g.cpa>0?fD(g.cpa):"—"}</td>
              <td style={{...tf,color:g.margenEur>=0?"#7ddb7d":"#ff8080"}}>{sgn(g.margenEur)}{fD(g.margenEur)}</td>
              <td style={{...tf,background:mcol(g.margenPct).bg,color:mcol(g.margenPct).t}}>{fP(g.margenPct)}</td>
              <td style={tf}></td>
            </tr></tfoot>
          </table>
        </div>

        <div style={{fontSize:12,fontWeight:600,color:"#555",textTransform:"uppercase",letterSpacing:".06em",margin:"1rem 0 .5rem"}}>📦 Ranking por producto</div>
        <div style={{overflowX:"auto",borderRadius:10,boxShadow:"0 2px 8px rgba(0,0,0,0.08)"}}>
          <table style={{borderCollapse:"collapse",width:"100%",minWidth:600}}>
            <thead><tr>{["Producto","Días","Inversión","Pedidos","Uds","Ingresos","COG","Comisión","ROAS","CPA","Margen $","Margen (%)"].map((h,i)=><th key={i} style={th}>{h}</th>)}</tr></thead>
            <tbody>
              {rankProd.map((r,i)=>{
                const rc=rcol(r.roas),mc=mcol(r.margenPct);
                return (
                  <tr key={i} style={{background:i%2===0?"#fff":"#f5f7fa"}}>
                    <td style={{...td,textAlign:"left",fontWeight:600,color:"#185FA5"}}>{r.nombre}</td>
                    <td style={td}>{r.dias}</td>
                    <td style={td}>{fD(r.inv)}</td>
                    <td style={td}>{r.pur}</td>
                    <td style={td}>{r.uds}</td>
                    <td style={td}>{fD(r.valTienda)}</td>
                    <td style={{...td,color:"#c0392b",fontWeight:500}}>{fD(r.cogT)}</td>
                    <td style={{...td,color:"#854F0B"}}>{fD(r.com)}</td>
                    <td style={{...td,background:rc.bg,color:rc.t,fontWeight:700}}>{fX(r.roas)}</td>
                    <td style={td}>{r.cpa>0?fD(r.cpa):"—"}</td>
                    <td style={{...td,color:r.margenEur>=0?"#1a7a1a":"#c0392b",fontWeight:700}}>{sgn(r.margenEur)}{fD(r.margenEur)}</td>
                    <td style={{...td,background:mc.bg,color:mc.t,fontWeight:700}}>{fP(r.margenPct)}</td>
                  </tr>
                );
              })}
            </tbody>
            <tfoot><tr>
              <td style={tf}>∑ TOTAL</td><td style={tf}>—</td>
              <td style={tf}>{fD(g.inv)}</td><td style={tf}>{g.pur}</td><td style={tf}>{g.uds}</td>
              <td style={tf}>{fD(g.valTienda)}</td>
              <td style={{...tf,color:"#ff9999"}}>{fD(g.cogT)}</td>
              <td style={{...tf,color:"#ffcc88"}}>{fD(g.com)}</td>
              <td style={{...tf,background:rcol(g.roas).bg}}>{fX(g.roas)}</td>
              <td style={tf}>{g.cpa>0?fD(g.cpa):"—"}</td>
              <td style={{...tf,color:g.margenEur>=0?"#7ddb7d":"#ff8080"}}>{sgn(g.margenEur)}{fD(g.margenEur)}</td>
              <td style={{...tf,background:mcol(g.margenPct).bg,color:mcol(g.margenPct).t}}>{fP(g.margenPct)}</td>
            </tr></tfoot>
          </table>
        </div>
      </div>
    );
  };

  return (
    <div style={{fontFamily:"'Segoe UI',sans-serif",background:"#f0f2f5",minHeight:"100vh",padding:"1rem"}}>
      <div style={{background:"#1a1a2e",borderRadius:10,padding:"1rem 1.25rem",marginBottom:12,display:"flex",justifyContent:"space-between",alignItems:"center",flexWrap:"wrap",gap:8}}>
        <div>
          <div style={{color:"#fff",fontSize:16,fontWeight:700}}>CALCULADORA DE ROAS — NORAVEL</div>
          <div style={{color:"#8899aa",fontSize:11,marginTop:2}}>{hist.length} registros · {campañas.length} campañas · {productos.length} productos · {fechas.length} días</div>
        </div>
        <button onClick={()=>setShowForm(s=>!s)} style={{background:"#2563eb",border:"none",borderRadius:7,color:"#fff",padding:"8px 18px",fontSize:13,cursor:"pointer",fontWeight:600}}>
          {showForm?"Cancelar":"+ Registrar día"}
        </button>
      </div>

      {showForm&&(
        <div style={{background:"#fff",borderRadius:10,padding:"1rem 1.25rem",marginBottom:12,border:"1px solid #85B7EB"}}>
          <div style={{fontWeight:600,color:"#185FA5",marginBottom:12}}>Nuevo registro</div>
          <div style={{display:"grid",gridTemplateColumns:"repeat(auto-fit,minmax(120px,1fr))",gap:10,marginBottom:10}}>
            <div><label style={lbl}>Fecha</label><input style={inp} type="date" value={form.fecha} onChange={e=>setForm({...form,fecha:e.target.value})}/></div>
            <div><label style={lbl}>Campaña</label><input style={inp} value={form.campaña} onChange={e=>setForm({...form,campaña:e.target.value})} placeholder="Ej: Chamarra 10 mayo"/></div>
            <div><label style={lbl}>Producto vendido</label><input style={inp} value={form.producto} onChange={e=>setForm({...form,producto:e.target.value})}/></div>
            <div><label style={lbl}>Inversión ($)</label><input style={inp} type="number" step="0.01" value={form.inversion} onChange={e=>setForm({...form,inversion:e.target.value})} placeholder="0"/></div>
            <div><label style={lbl}>CPC ($)</label><input style={inp} type="number" step="0.01" value={form.cpc} onChange={e=>setForm({...form,cpc:e.target.value})} placeholder="0"/></div>
            <div><label style={lbl}>ATC</label><input style={inp} type="number" value={form.atc} onChange={e=>setForm({...form,atc:e.target.value})} placeholder="0"/></div>
            <div><label style={lbl}>PUR</label><input style={inp} type="number" value={form.pur} onChange={e=>setForm({...form,pur:e.target.value})} placeholder="0"/></div>
            <div><label style={lbl}>Unid. Vendidas</label><input style={inp} type="number" value={form.uds} onChange={e=>setForm({...form,uds:e.target.value})} placeholder="0"/></div>
            <div><label style={lbl}>Precio ($)</label><input style={inp} type="number" step="0.01" value={form.price} onChange={e=>setForm({...form,price:e.target.value})}/></div>
            <div><label style={lbl}>Descuento (%)</label><input style={inp} type="number" step="0.1" value={form.descPct} onChange={e=>setForm({...form,descPct:e.target.value})} placeholder="0"/></div>
            <div><label style={lbl}>Costo prod. ($)</label><input style={inp} type="number" step="0.01" value={form.cog} onChange={e=>setForm({...form,cog:e.target.value})}/></div>
          </div>
          <button onClick={addRow} style={{background:"#1a7a1a",border:"none",borderRadius:7,color:"#fff",padding:"8px 20px",fontSize:13,cursor:"pointer",fontWeight:600}}>Guardar</button>
        </div>
      )}

      <div style={{display:"flex",gap:6,marginBottom:12,flexWrap:"wrap"}}>
        <button style={tab(view==="dia")}      onClick={()=>setView("dia")}>📅 Por fecha</button>
        <button style={tab(view==="campaña")}  onClick={()=>setView("campaña")}>📣 Por campaña</button>
        <button style={tab(view==="producto")} onClick={()=>setView("producto")}>📦 Por producto</button>
        <button style={tab(view==="global")}   onClick={()=>setView("global")}>🌐 Global</button>
      </div>

      {view==="dia"      && <ViewDia/>}
      {view==="campaña"  && <ViewCampaña/>}
      {view==="producto" && <ViewProducto/>}
      {view==="global"   && <ViewGlobal/>}

      <div style={{marginTop:10,background:"#1a1a2e",borderRadius:10,padding:"0.75rem 1rem",display:"flex",gap:12,flexWrap:"wrap",alignItems:"center"}}>
        <div style={{color:"#8899aa",fontSize:11,fontWeight:600}}>SEMÁFORO</div>
        {[
          {c:"#fff9d6",t:"#333",b:"1px solid #ccc",l:"Amarillo = entrada"},
          {c:"#f8f9fa",t:"#333",b:"1px solid #ccc",l:"Gris = calculado"},
          {c:"#1a7a1a",l:"ROAS 2.5+"},{c:"#2d8f2d",l:"ROAS 2–2.5"},{c:"#e6a817",l:"ROAS 1.5–2"},{c:"#c0392b",l:"ROAS <1.5"},
          {c:"#1a7a1a",l:"Margen 20%+"},{c:"#e6a817",l:"Margen 0–20%"},{c:"#c0392b",l:"Margen 0%-"}
        ].map((s,i)=>(
          <div key={i} style={{display:"flex",alignItems:"center",gap:5}}>
            <div style={{width:10,height:10,borderRadius:3,background:s.c,border:s.b||"none"}}></div>
            <span style={{color:"#c8d6e5",fontSize:11}}>{s.l}</span>
          </div>
        ))}
      </div>
    </div>
  );
}
