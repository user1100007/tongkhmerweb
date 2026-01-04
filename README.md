# tongkhmerweb
<!DOCTYPE html>

<html lang="km">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>តារាងពិនិត្យតាមដានសម្ភារពេញលេញ</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Khmer:wght@400;600;700&display=swap');

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Noto Sans Khmer', sans-serif;
  background: #f5f5f5;
  padding: 15px;
}

.tabs {
  max-width: 1400px;
  margin: 0 auto 20px;
  display: flex;
  gap: 10px;
  justify-content: center;
  flex-wrap: wrap;
}

.tab-btn {
  padding: 12px 24px;
  font-family: 'Noto Sans Khmer', sans-serif;
  font-size: 15px;
  border: none;
  border-radius: 8px 8px 0 0;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.2s;
  background: #e0e0e0;
  color: #333;
}

.tab-btn.active {
  background: #1e40af;
  color: white;
}

.tab-btn:hover {
  background: #3b82f6;
  color: white;
}

.controls {
  max-width: 1400px;
  margin: 0 auto 15px;
  display: flex;
  gap: 10px;
  justify-content: center;
  flex-wrap: wrap;
}

.controls button {
  padding: 12px 24px;
  font-family: 'Noto Sans Khmer', sans-serif;
  font-size: 15px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.2s;
  box-shadow: 0 2px 8px rgba(0,0,0,0.15);
}

.btn-calc {
  background: #f59e0b;
  color: white;
}

.btn-calc:hover {
  background: #d97706;
}

.btn-save {
  background: #1e40af;
  color: white;
}

.btn-save:hover {
  background: #1e3a8a;
}

.btn-load {
  background: #059669;
  color: white;
}

.btn-load:hover {
  background: #047857;
}

.btn-print {
  background: #7c3aed;
  color: white;
}

.btn-print:hover {
  background: #6d28d9;
}

.btn-clear {
  background: #b91c1c;
  color: white;
}

.btn-clear:hover {
  background: #991b1b;
}

.btn-db {
  background: #8b5cf6;
  color: white;
}

.btn-db:hover {
  background: #7c3aed;
}

.page {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  background: white;
  padding: 20px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
  border-radius: 8px;
}

.header {
  text-align: center;
  margin-bottom: 15px;
}

.header-title {
  font-weight: 700;
  font-size: 14px;
  line-height: 1.6;
}

.info-section {
  margin-bottom: 15px;
  font-size: 11px;
}

.info-row {
  display: flex;
  margin-bottom: 3px;
}

.info-label {
  font-weight: 600;
  width: 200px;
}

.info-value {
  flex: 1;
}

input[type="text"], input[type="number"], select {
  border: none;
  border-bottom: 1px dotted #666;
  background: transparent;
  font-family: 'Noto Sans Khmer', sans-serif;
  font-size: 11px;
  padding: 2px 4px;
  width: 100%;
}

input:focus, select:focus {
  outline: none;
  background: #f0f9ff;
  border-bottom: 1px solid #2563eb;
}

.table-title {
  text-align: center;
  font-weight: 700;
  font-size: 14px;
  margin: 15px 0 10px;
}

.section-marker {
  font-weight: 700;
  font-size: 12px;
  margin: 15px 0 8px;
  color: #1e40af;
}

table {
  width: 100%;
  border-collapse: collapse;
  font-size: 10px;
  margin-bottom: 10px;
}

table th,
table td {
  border: 1px solid #000;
  padding: 6px 4px;
  text-align: center;
}

table th {
  background: #1e40af;
  color: white;
  font-weight: 700;
}

table td.editable {
  background: #fff;
  cursor: text;
}

table td.editable:hover {
  background: #fef3c7;
}

table td[contenteditable="true"]:focus {
  background: #dbeafe;
  outline: 2px solid #3b82f6;
}

.total-row {
  background: #fef3c7 !important;
  font-weight: 700;
}

.total-row td {
  background: #fef3c7 !important;
  font-weight: 700;
}

.align-left {
  text-align: left !important;
  padding-left: 8px;
}

.add-row-btn {
  background: #10b981;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 6px;
  cursor: pointer;
  font-family: 'Noto Sans Khmer', sans-serif;
  font-size: 12px;
  margin-bottom: 20px;
  transition: all 0.2s;
}

.add-row-btn:hover {
  background: #059669;
}

.delete-btn {
  background: #ef4444;
  color: white;
  border: none;
  padding: 4px 10px;
  border-radius: 4px;
  cursor: pointer;
  font-family: 'Noto Sans Khmer', sans-serif;
  font-size: 10px;
  transition: all 0.2s;
}

.delete-btn:hover {
  background: #dc2626;
}

.action-col {
  width: 60px;
}

.tab-content {
  display: none;
}

.tab-content.active {
  display: block;
}

.filter-section {
  margin: 15px 0;
  padding: 15px;
  background: #f3f4f6;
  border-radius: 8px;
}

.filter-row {
  display: flex;
  gap: 15px;
  align-items: center;
  flex-wrap: wrap;
}

.filter-item {
  display: flex;
  gap: 8px;
  align-items: center;
}

.filter-item label {
  font-weight: 600;
  font-size: 12px;
}

.filter-item select {
  padding: 6px 12px;
  border: 1px solid #d1d5db;
  border-radius: 6px;
  background: white;
}

@media print {
  body {
    background: white;
    padding: 0;
  }
  
  .tabs, .controls, .add-row-btn, .delete-btn, .action-col, .filter-section {
    display: none !important;
  }
  
  .page {
    margin: 0;
    box-shadow: none;
    padding: 10mm;
    page-break-after: always;
  }

  table {
    page-break-inside: avoid;
    font-size: 9px;
  }

  table th {
    padding: 6px 4px !important;
    font-size: 9px;
  }

  table td {
    padding: 6px 4px !important;
    word-wrap: break-word;
    font-size: 9px;
  }

  .header-title {
    font-size: 12px;
  }

  .info-section {
    font-size: 10px;
  }

  .table-title {
    font-size: 13px;
  }

  .section-marker {
    font-size: 11px;
  }
  
  @page {
    size: A4 landscape;
    margin: 8mm;
  }
}
```

  </style>
</head>
<body>
  <div class="tabs">
    <button class="tab-btn active" onclick="switchTab('main')">📋 តារាងចម្បង</button>
    <button class="tab-btn" onclick="switchTab('database')">💾 SQL Database</button>
    <button class="tab-btn" onclick="switchTab('report')">📊 របាយការណ៍</button>
  </div>

  <div class="controls">
    <button class="btn-calc" onclick="calculateAllTotals()">🔢 គណនាសរុប</button>
    <button class="btn-save" onclick="saveData()">💾 រក្សាទុក</button>
    <button class="btn-load" onclick="loadData()">📂 ផ្ទុក</button>
    <button class="btn-db" onclick="loadFromDatabase()">📊 ផ្ទុក Database</button>
    <button class="btn-print" onclick="window.print()">🖨️ បោះពុម្ព</button>
    <button class="btn-clear" onclick="clearData()">🗑️ លុប</button>
  </div>

  <!-- Tab 1: Main Table -->

  <div id="mainTab" class="tab-content active">
    <div class="page">
      <div class="header">
        <div class="header-title">ព្រះរាជាណាចក្រកម្ពុជា</div>
        <div class="header-title">ជាតិ សាសនា ព្រះមហាក្សត្រ</div>
      </div>

```
  <div class="info-section">
    <div class="info-row">
      <span class="info-label">អាជ្ញាធរកាន់កាប់ទ្រព្យសម្បត្តិរដ្ឋ :</span>
      <span class="info-value"><input type="text" id="authority" value="ក្រសួងអប់រំ យុវជន និងកីឡា"></span>
    </div>
    <div class="info-row">
      <span class="info-label">អង្គភាពប្រើប្រាស់ :</span>
      <span class="info-value"><input type="text" id="unit" value="មន្ទីរអប់រំ យុវជន និងកីឡាខេត្តបន្ទាយមានជ័យ"></span>
    </div>
    <div class="info-row">
      <span class="info-label">អ្នកប្រើប្រាស់ :</span>
      <span class="info-value"><input type="text" id="user" value="ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុកភ្នំស្រុក"></span>
    </div>
    <div class="info-row">
      <span class="info-label">ឈ្មោះសាលារៀន :</span>
      <span class="info-value"><input type="text" id="school" value="សាលាបឋមសិក្សា រោគ"></span>
    </div>
  </div>

  <div class="table-title">តារាងពិនិត្យតាមដានសម្ភារនិងទ្រព្យសម្បត្តិរដ្ឋ</div>
  <div class="table-title" style="font-size: 12px;">លើកទី២ ខែមិថុនា ឆ្នាំ២០២៥</div>

  <!-- ផ្នែកទី១: ដី -->
  <div class="section-marker">I- ដី និងអគារ</div>
  <div class="section-marker" style="font-size: 11px;">ព័ត៌មានអំពី « ដី »</div>

  <table id="landTable">
    <thead>
      <tr>
        <th colspan="4">បរិយាយ</th>
        <th colspan="9">ស្ថានភាព និងការគ្រប់គ្រង</th>
        <th rowspan="3" class="action-col">សកម្មភាព</th>
      </tr>
      <tr>
        <th rowspan="2">ល.រ</th>
        <th rowspan="2">ទីតាំង</th>
        <th rowspan="2">ចំនួន</th>
        <th rowspan="2">ទំហំ<br>(ម២)</th>
        <th colspan="3">ប័ណ្ណកម្មសិទ្ធិ</th>
        <th colspan="2">អ្នកស្នាក់នៅ</th>
        <th colspan="2">ករណីវិវាទ</th>
        <th colspan="2">សម្បទានសេវាសាធារណៈ</th>
      </tr>
      <tr>
        <th>ធ្វើរួច</th>
        <th>មិនទាន់<br>ធ្វើ</th>
        <th>ដាក់ពាក្យ<br>រួច</th>
        <th>មាន<br>កិច្ចសន្យា</th>
        <th>មិនព្រមធ្វើ<br>កិច្ចសន្យា</th>
        <th>មិនបាន<br>ដោះស្រាយ</th>
        <th>តុលាការ</th>
        <th>មាន<br>កិច្ចសន្យា</th>
        <th>គ្មាន<br>កិច្ចសន្យា</th>
      </tr>
    </thead>
    <tbody id="landBody">
      <tr>
        <td>1</td>
        <td class="editable align-left" contenteditable="true">ដីសាលារៀន</td>
        <td class="editable" contenteditable="true">1</td>
        <td class="editable" contenteditable="true">14400</td>
        <td class="editable" contenteditable="true">1</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td><button class="delete-btn" onclick="deleteRow(this, 'landBody')">លុប</button></td>
      </tr>
    </tbody>
    <tfoot>
      <tr class="total-row">
        <td colspan="2"><strong>សរុប</strong></td>
        <td id="landTotal_0">1</td>
        <td id="landTotal_1">14400</td>
        <td id="landTotal_2">1</td>
        <td id="landTotal_3">0</td>
        <td id="landTotal_4">0</td>
        <td id="landTotal_5">0</td>
        <td id="landTotal_6">0</td>
        <td id="landTotal_7">0</td>
        <td id="landTotal_8">0</td>
        <td id="landTotal_9">0</td>
        <td id="landTotal_10">0</td>
        <td></td>
      </tr>
    </tfoot>
  </table>
  <button class="add-row-btn" onclick="addLandRow()">+ បន្ថែមជួរដី</button>

  <!-- ផ្នែកទី២: អគារ -->
  <div class="section-marker" style="font-size: 11px;">ព័ត៌មានអំពី « អគារ »</div>

  <table id="buildingTable">
    <thead>
      <tr>
        <th rowspan="2">ល.រ</th>
        <th rowspan="2">ទីតាំង</th>
        <th colspan="4">ប្រភេទអគារ</th>
        <th colspan="4">ស្ថានភាព</th>
        <th colspan="2">ការប្រើប្រាស់</th>
        <th rowspan="2">ផ្សេងៗ</th>
        <th rowspan="2" class="action-col">សកម្មភាព</th>
      </tr>
      <tr>
        <th>ថ្ម</th>
        <th>ឈើ</th>
        <th>ចម្រុះ</th>
        <th>សរុប</th>
        <th>ល្អ</th>
        <th>មធ្យម</th>
        <th>អន់</th>
        <th>ខូច</th>
        <th>លើស</th>
        <th>ខ្វះ</th>
      </tr>
    </thead>
    <tbody id="buildingBody">
      <tr>
        <td>1</td>
        <td class="editable align-left" contenteditable="true">ដីសាលារៀន</td>
        <td class="editable" contenteditable="true">4</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">4</td>
        <td class="editable" contenteditable="true">3</td>
        <td class="editable" contenteditable="true">1</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true"></td>
        <td><button class="delete-btn" onclick="deleteRow(this, 'buildingBody')">លុប</button></td>
      </tr>
    </tbody>
    <tfoot>
      <tr class="total-row">
        <td colspan="2"><strong>សរុប</strong></td>
        <td id="buildingTotal_0">4</td>
        <td id="buildingTotal_1">0</td>
        <td id="buildingTotal_2">0</td>
        <td id="buildingTotal_3">4</td>
        <td id="buildingTotal_4">3</td>
        <td id="buildingTotal_5">1</td>
        <td id="buildingTotal_6">0</td>
        <td id="buildingTotal_7">0</td>
        <td id="buildingTotal_8">0</td>
        <td id="buildingTotal_9">0</td>
        <td id="buildingTotal_10"></td>
        <td></td>
      </tr>
    </tfoot>
  </table>
  <button class="add-row-btn" onclick="addBuildingRow()">+ បន្ថែមជួរអគារ</button>

  <!-- ផ្នែកទី២: យានយន្ត -->
  <div class="section-marker">II- យានយន្ត និងគ្រឿងចក្រ</div>
  <table id="vehicleTable">
    <thead>
      <tr>
        <th rowspan="2">ល.រ</th>
        <th rowspan="2">បរិយាយ</th>
        <th colspan="5">ស្ថានភាព</th>
        <th colspan="2">ការប្រើប្រាស់</th>
        <th rowspan="2">ផ្សេងៗ</th>
        <th rowspan="2" class="action-col">សកម្មភាព</th>
      </tr>
      <tr>
        <th>សរុប</th>
        <th>ល្អ</th>
        <th>មធ្យម</th>
        <th>អន់</th>
        <th>ខូច</th>
        <th>លើស</th>
        <th>ខ្វះ</th>
      </tr>
    </thead>
    <tbody id="vehicleBody">
      <tr>
        <td>1</td>
        <td class="editable align-left" contenteditable="true">រថយន្ត</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true"></td>
        <td><button class="delete-btn" onclick="deleteRow(this, 'vehicleBody')">លុប</button></td>
      </tr>
    </tbody>
    <tfoot>
      <tr class="total-row">
        <td colspan="2"><strong>សរុប</strong></td>
        <td id="vehicleTotal_0">0</td>
        <td id="vehicleTotal_1">0</td>
        <td id="vehicleTotal_2">0</td>
        <td id="vehicleTotal_3">0</td>
        <td id="vehicleTotal_4">0</td>
        <td id="vehicleTotal_5">0</td>
        <td id="vehicleTotal_6">0</td>
        <td id="vehicleTotal_7"></td>
        <td></td>
      </tr>
    </tfoot>
  </table>
  <button class="add-row-btn" onclick="addVehicleRow()">+ បន្ថែមជួរយានយន្ត</button>

  <!-- ផ្នែកទី៣: បរិក្ខារបច្ចេកទេស -->
  <div class="section-marker">III- បរិក្ខារបច្ចេកទេស និងឱស្សាហកម្ម</div>
  <table id="technicalTable">
    <thead>
      <tr>
        <th rowspan="2">ល.រ</th>
        <th rowspan="2">បរិយាយ</th>
        <th colspan="5">ស្ថានភាព</th>
        <th colspan="2">ការប្រើប្រាស់</th>
        <th rowspan="2">ផ្សេងៗ</th>
        <th rowspan="2" class="action-col">សកម្មភាព</th>
      </tr>
      <tr>
        <th>សរុប</th>
        <th>ល្អ</th>
        <th>មធ្យម</th>
        <th>អន់</th>
        <th>ខូច</th>
        <th>លើស</th>
        <th>ខ្វះ</th>
      </tr>
    </thead>
    <tbody id="technicalBody">
      <tr>
        <td>1</td>
        <td class="editable align-left" contenteditable="true">ម៉ាស៊ីនភ្លើង</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true"></td>
        <td><button class="delete-btn" onclick="deleteRow(this, 'technicalBody')">លុប</button></td>
      </tr>
    </tbody>
    <tfoot>
      <tr class="total-row">
        <td colspan="2"><strong>សរុប</strong></td>
        <td id="technicalTotal_0">0</td>
        <td id="technicalTotal_1">0</td>
        <td id="technicalTotal_2">0</td>
        <td id="technicalTotal_3">0</td>
        <td id="technicalTotal_4">0</td>
        <td id="technicalTotal_5">0</td>
        <td id="technicalTotal_6">0</td>
        <td id="technicalTotal_7"></td>
        <td></td>
      </tr>
    </tfoot>
  </table>
  <button class="add-row-btn" onclick="addTechnicalRow()">+ បន្ថែមជួរបរិក្ខារបច្ចេកទេស</button>

  <!-- ផ្នែកទី៤: សម្ភារ -->
  <div class="section-marker">IV- សម្ភារ និងសង្ហារិម</div>
  <table id="furnitureTable">
    <thead>
      <tr>
        <th rowspan="2">ល.រ</th>
        <th rowspan="2">ឈ្មោះសម្ភារបរិក្ខារ</th>
        <th colspan="5">ស្ថានភាពសម្ភារៈ</th>
        <th colspan="2">ការប្រើប្រាស់</th>
        <th rowspan="2">បុគ្គលិក</th>
        <th rowspan="2">សិស្ស</th>
        <th rowspan="2" class="action-col">សកម្មភាព</th>
      </tr>
      <tr>
        <th>ល្អ</th>
        <th>មធ្យម</th>
        <th>អន់</th>
        <th>ខូច</th>
        <th>សរុប</th>
        <th>លើស</th>
        <th>ខ្វះ</th>
      </tr>
    </thead>
    <tbody id="furnitureBody">
    </tbody>
    <tfoot>
      <tr class="total-row">
        <td colspan="2"><strong>សរុប</strong></td>
        <td id="furnitureTotal_0">0</td>
        <td id="furnitureTotal_1">0</td>
        <td id="furnitureTotal_2">0</td>
        <td id="furnitureTotal_3">0</td>
        <td id="furnitureTotal_4">0</td>
        <td id="furnitureTotal_5">0</td>
        <td id="furnitureTotal_6">0</td>
        <td id="furnitureTotal_7">0</td>
        <td id="furnitureTotal_8">0</td>
        <td></td>
      </tr>
    </tfoot>
  </table>
  <button class="add-row-btn" onclick="addFurnitureRow()">+ បន្ថែមជួរសម្ភារ</button>

  <!-- ហត្ថលេខា -->
  <div style="margin-top: 40px; display: flex; justify-content: space-between; font-size: 11px;">
    <div style="text-align: center; width: 30%;">
      <p>រៀបចំដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
    <div style="text-align: center; width: 30%;">
      <p>ផ្ទៀងផ្ទាត់ដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
    <div style="text-align: center; width: 30%;">
      <p>អនុម័តដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
  </div>
</div>
```

  </div>

  <!-- Tab 2: Database -->

  <div id="databaseTab" class="tab-content">
    <div class="page">
      <div class="header">
        <div class="header-title">ព្រះរាជាណាចក្រកម្ពុជា</div>
        <div class="header-title">ជាតិ សាសនា ព្រះមហាក្សត្រ</div>
      </div>

```
  <div class="info-section">
    <div class="info-row">
      <span class="info-label">អាជ្ញាធរកាន់កាប់ទ្រព្យសម្បត្តិរដ្ឋ :</span>
      <span class="info-value">ក្រសួងអប់រំ យុវជន និងកីឡា</span>
    </div>
    <div class="info-row">
      <span class="info-label">អង្គភាពប្រើប្រាស់ :</span>
      <span class="info-value">មន្ទីរអប់រំ យុវជន និងកីឡាខេត្តបន្ទាយមានជ័យ</span>
    </div>
    <div class="info-row">
      <span class="info-label">ការិយាល័យប្រើប្រាស់ :</span>
      <span class="info-value">ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុកភ្នំស្រុក</span>
    </div>
    <div class="info-row">
      <span class="info-label">ឈ្មោះសាលារៀន :</span>
      <span class="info-value">សាលាបឋមសិក្សា រោគ</span>
    </div>
  </div>

  <div class="table-title">តារាងសម្ភារ និងសង្ហារិម (SQL Database)</div>
  <div class="table-title" style="font-size: 12px;">ឆ្នាំ១៩៩៨-២០២៥</div>

  <div class="filter-section">
    <div class="filter-row">
      <div class="filter-item">
        <label>ឆ្នាំ:</label>
        <select id="filterYear" onchange="filterDatabase()">
          <option value="">ទាំងអស់</option>
        </select>
      </div>
      <div class="filter-item">
        <label>ប្រភេទ:</label>
        <select id="filterType" onchange="filterDatabase()">
          <option value="">ទាំងអស់</option>
          <option value="MOB">MOB - គ្រឿងសង្ហារឹម</option>
          <option value="MBU">MBU - ឧបករណ៍</option>
          <option value="MIN">MIN - បរិក្ខារព័ត៌មាន</option>
        </select>
      </div>
      <div class="filter-item">
        <label>ស្ថានភាព:</label>
        <select id="filterStatus" onchange="filterDatabase()">
          <option value="">ទាំងអស់</option>
          <option value="ល្អ">ល្អ</option>
          <option value="មធ្យម">មធ្យម</option>
          <option value="អន់">អន់</option>
          <option value="ខូច">ខូច</option>
        </select>
      </div>
    </div>
  </div>

  <table id="databaseTable">
    <thead>
      <tr>
        <th style="width: 40px;">ល.រ</th>
        <th style="width: 70px;">ប្រភេទ</th>
        <th style="width: 200px;">ឈ្មោះសម្ភារ</th>
        <th style="width: 60px;">ឆ្នាំ</th>
        <th style="width: 150px;">អ្នកប្រើប្រាស់</th>
        <th style="width: 80px;">ម៉ាក</th>
        <th style="width: 80px;">ជំពូក</th>
        <th style="width: 70px;">បរិមាណ</th>
        <th style="width: 100px;">តម្លៃ(រៀល)</th>
        <th style="width: 80px;">ស្ថានភាព</th>
      </tr>
    </thead>
    <tbody id="databaseBody">
    </tbody>
    <tfoot>
      <tr class="total-row">
        <td colspan="7" style="text-align: right; padding-right: 10px;"><strong>សរុប</strong></td>
        <td id="dbTotalQty">0</td>
        <td id="dbTotalPrice" style="text-align: right; padding-right: 8px;">0</td>
        <td></td>
      </tr>
    </tfoot>
  </table>

  <div style="margin-top: 40px; display: flex; justify-content: space-between; font-size: 11px;">
    <div style="text-align: center; width: 30%;">
      <p>រៀបចំដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
    <div style="text-align: center; width: 30%;">
      <p>ផ្ទៀងផ្ទាត់ដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
    <div style="text-align: center; width: 30%;">
      <p>អនុម័តដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
  </div>
</div>
```

  </div>

  <!-- Tab 3: Report -->

  <div id="reportTab" class="tab-content">
    <div class="page">
      <div class="header">
        <div class="header-title">ព្រះរាជាណាចក្រកម្ពុជា</div>
        <div class="header-title">ជាតិ សាសនា ព្រះមហាក្សត្រ</div>
      </div>

```
  <div class="info-section">
    <div class="info-row">
      <span class="info-label">អាជ្ញាធរកាន់កាប់ទ្រព្យសម្បត្តិរដ្ឋ :</span>
      <span class="info-value">ក្រសួងអប់រំ យុវជន និងកីឡា</span>
    </div>
    <div class="info-row">
      <span class="info-label">អង្គភាពប្រើប្រាស់ :</span>
      <span class="info-value">មន្ទីរអប់រំ យុវជន និងកីឡាខេត្តបន្ទាយមានជ័យ</span>
    </div>
    <div class="info-row">
      <span class="info-label">ការិយាល័យប្រើប្រាស់ :</span>
      <span class="info-value">ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុកភ្នំស្រុក</span>
    </div>
    <div class="info-row">
      <span class="info-label">ឈ្មោះសាលារៀន :</span>
      <span class="info-value">សាលាបឋមសិក្សា រោគ</span>
    </div>
  </div>

  <div class="table-title">របាយការណ៍សង្ខេប - សម្ភារ និងសង្ហារិម</div>
  <div class="table-title" style="font-size: 12px;">ឆ្នាំ១៩៩៨-២០២៥</div>

  <div class="section-marker">សង្ខេបតាមប្រភេទ</div>
  <table id="reportByType">
    <thead>
      <tr>
        <th>ប្រភេទ</th>
        <th>ចំនួនសរុប</th>
        <th>តម្លៃសរុប(រៀល)</th>
        <th>ល្អ</th>
        <th>មធ្យម</th>
        <th>អន់</th>
        <th>ខូច</th>
      </tr>
    </thead>
    <tbody id="reportByTypeBody">
    </tbody>
  </table>

  <div class="section-marker">សង្ខេបតាមឆ្នាំ</div>
  <table id="reportByYear">
    <thead>
      <tr>
        <th>ឆ្នាំ</th>
        <th>ចំនួនសម្ភារ</th>
        <th>តម្លៃសរុប(រៀល)</th>
      </tr>
    </thead>
    <tbody id="reportByYearBody">
    </tbody>
  </table>

  <div class="section-marker">សង្ខេបតាមស្ថានភាព</div>
  <table id="reportByStatus">
    <thead>
      <tr>
        <th>ស្ថានភាព</th>
        <th>ចំនួន</th>
        <th>ភាគរយ</th>
      </tr>
    </thead>
    <tbody id="reportByStatusBody">
    </tbody>
  </table>

  <div style="margin-top: 40px; display: flex; justify-content: space-between; font-size: 11px;">
    <div style="text-align: center; width: 30%;">
      <p>រៀបចំដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
    <div style="text-align: center; width: 30%;">
      <p>ផ្ទៀងផ្ទាត់ដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
    <div style="text-align: center; width: 30%;">
      <p>អនុម័តដោយ</p>
      <p style="margin-top: 60px;">ឈ្មោះ: ...........................</p>
    </div>
  </div>
</div>
```

  </div>

<script>
  const STORAGE_KEY = 'property-tracking-full-data-v3';
  
  // SQL Database
  const SQL_DATABASE = [
    {id: 1, type: 'MOB', name: 'ធុងដែក', year: 1998, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 2, price: 1200000, status: 'អន់'},
    {id: 2, type: 'MOB', name: 'តុសិស្ស៤បង្កុយ', year: 1999, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 9, price: 900000, status: 'អន់'},
    {id: 3, type: 'MOB', name: 'កៅអីគ្រូ', year: 2000, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 4, price: 640000, status: 'មធ្យម'},
    {id: 4, type: 'MOB', name: 'ក្ដារខៀន', year: 2000, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 5, price: 400000, status: 'មធ្យម'},
    {id: 5, type: 'MOB', name: 'ក្ដារខៀនហ្វឺត', year: 2000, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 250000, status: 'អន់'},
    {id: 6, type: 'MOB', name: 'តុសិស្ស២បង្កុយ', year: 2000, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 85, price: 7480000, status: 'អន់'},
    {id: 7, type: 'MOB', name: 'ទូកញ្ចក់', year: 2004, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 250000, status: 'អន់'},
    {id: 8, type: 'MOB', name: 'ធុងដែក', year: 2010, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 200000, status: 'អន់'},
    {id: 9, type: 'MOB', name: 'ធ្នើដាក់សៀវភៅ', year: 2010, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 200000, status: 'មធ្យម'},
    {id: 10, type: 'MOB', name: 'តុសិស្ស២បង្កុយ', year: 2013, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 20, price: 1400000, status: 'អន់'},
    {id: 11, type: 'MOB', name: 'តុសិស្ស២បង្កុយ', year: 2013, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 95, price: 40679000, status: 'អន់'},
    {id: 12, type: 'MOB', name: 'តុអាន', year: 2013, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 2, price: 2848000, status: 'មធ្យម'},
    {id: 13, type: 'MOB', name: 'ធ្នើមុខមួយ', year: 2013, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 2, price: 2377400, status: 'មធ្យម'},
    {id: 14, type: 'MOB', name: 'ក្ដារខៀន', year: 2016, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 2, price: 160000, status: 'មធ្យម'},
    {id: 15, type: 'MOB', name: 'កៅអីជ័រធុនតូច', year: 2017, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 24, price: 192000, status: 'មធ្យម'},
    {id: 16, type: 'MOB', name: 'តុសិស្សអាន(ដែក)', year: 2017, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 12, price: 576000, status: 'មធ្យម'},
    {id: 17, type: 'MOB', name: 'តុគ្រូ', year: 2018, user: 'មន្ទីរអប់រំ', brand: '', chapter: '', qty: 6, price: 1800000, status: 'មធ្យម'},
    {id: 18, type: 'MOB', name: 'ទោងរំអិល', year: 2018, user: 'World vision', brand: '', chapter: '', qty: 1, price: 1080000, status: 'មធ្យម'},
    {id: 19, type: 'MOB', name: 'ក្ដាររំអិល', year: 2019, user: 'World vision', brand: '', chapter: '', qty: 2, price: 1600000, status: 'មធ្យម'},
    {id: 20, type: 'MOB', name: 'ជណ្ដើរស្វា', year: 2019, user: 'World vision', brand: '', chapter: '', qty: 2, price: 1584000, status: 'ល្អ'},
    {id: 21, type: 'MOB', name: 'តុតឿ', year: 2020, user: 'បឋមសិក្សារោគ', brand: '', chapter: '', qty: 4, price: 100000, status: 'ល្អ'},
    {id: 22, type: 'MOB', name: 'ទូដាក់ឯកសារ', year: 2020, user: '', brand: '', chapter: '', qty: 1, price: 750000, status: 'ល្អ'},
    {id: 23, type: 'MOB', name: 'ធ្នើដាក់សៀវភៅតូច', year: 2020, user: '', brand: '', chapter: '', qty: 4, price: 40000, status: 'ល្អ'},
    {id: 24, type: 'MOB', name: 'ធ្នើដាក់សៀវភៅធំ', year: 2020, user: '', brand: '', chapter: '', qty: 4, price: 60000, status: 'ល្អ'},
    {id: 25, type: 'MOB', name: 'ធ្នើមុខពីរ', year: 2020, user: '', brand: '', chapter: '', qty: 2, price: 70000, status: 'ល្អ'},
    {id: 26, type: 'MOB', name: 'ធ្នើមុខមួយ', year: 2020, user: '', brand: '', chapter: '', qty: 4, price: 50000, status: 'ល្អ'},
    {id: 27, type: 'MOB', name: 'តុគ្រូ', year: 2021, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 100000, status: 'ល្អ'},
    {id: 28, type: 'MOB', name: 'តុវែង', year: 2021, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 4, price: 200000, status: 'ល្អ'},
    {id: 29, type: 'MBU', name: 'កង្ហារ', year: 2023, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 4, price: 250000, status: 'មធ្យម'},
    {id: 30, type: 'MBU', name: 'ម៉ូទ័របូមទឹក', year: 2023, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 400000, status: 'មធ្យម'},
    {id: 31, type: 'MBU', name: 'ម៉ូទ័រកាត់ផ្កា', year: 2024, user: 'ក្នុងស្រុក', brand: '', chapter: '', qty: 1, price: 500000, status: 'មធ្យម'},
    {id: 32, type: 'MIN', name: 'ម៉ាស៊ីនព្រីន', year: 2018, user: 'សប្បុរសជន', brand: 'Epson', chapter: '', qty: 1, price: 1200000, status: 'ខូច'},
    {id: 33, type: 'MIN', name: 'កុំព្យូទ័រយួរដៃ', year: 2019, user: 'ក្រសួងអប់រំ', brand: 'Asus', chapter: '', qty: 1, price: 2713500, status: 'ខូច'},
    {id: 34, type: 'MIN', name: 'ម៉ាស៊ីនព្រីន', year: 2019, user: 'ក្រសួងអប់រំ', brand: 'HP', chapter: '', qty: 1, price: 1336500, status: 'ខូច'},
    {id: 35, type: 'MIN', name: 'ម៉ាស៊ីនព្រីន Canon', year: 2023, user: 'ក្នុងស្រុក', brand: 'Canon', chapter: '', qty: 1, price: 1100000, status: 'មធ្យម'},
    {id: 36, type: 'MIN', name: 'កុំព្យូទ័រ Desktop', year: 2023, user: 'ក្នុងស្រុក', brand: 'Dell', chapter: '', qty: 1, price: 1800000, status: 'មធ្យម'},
    {id: 37, type: 'MIN', name: 'ម៉ាស៊ីនព្រីន Color', year: 2024, user: 'សប្បុរសជន', brand: 'Canon', chapter: '', qty: 1, price: 1000000, status: 'មធ្យម'},
    {id: 38, type: 'MIN', name: 'ម៉ាស៊ីនព្រីន HP', year: 2024, user: 'សប្បុរសជន', brand: 'HP', chapter: '', qty: 1, price: 1500000, status: 'មធ្យម'}
  ];

  // Tab switching
  function switchTab(tab) {
    document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    
    if (tab === 'main') {
      document.getElementById('mainTab').classList.add('active');
      event.target.classList.add('active');
    } else if (tab === 'database') {
      document.getElementById('databaseTab').classList.add('active');
      event.target.classList.add('active');
      renderDatabase();
    } else if (tab === 'report') {
      document.getElementById('reportTab').classList.add('active');
      event.target.classList.add('active');
      generateReport();
    }
  }

  // Render database table
  function renderDatabase() {
    const tbody = document.getElementById('databaseBody');
    const filterYear = document.getElementById('filterYear').value;
    const filterType = document.getElementById('filterType').value;
    const filterStatus = document.getElementById('filterStatus').value;
    
    let filteredData = SQL_DATABASE;
    
    if (filterYear) filteredData = filteredData.filter(item => item.year.toString() === filterYear);
    if (filterType) filteredData = filteredData.filter(item => item.type === filterType);
    if (filterStatus) filteredData = filteredData.filter(item => item.status === filterStatus);
    
    tbody.innerHTML = filteredData.map((item, index) => `
      <tr>
        <td>${index + 1}</td>
        <td>${item.type}</td>
        <td class="align-left" style="padding-left: 8px;">${item.name}</td>
        <td>${item.year}</td>
        <td class="align-left" style="padding-left: 8px;">${item.user}</td>
        <td>${item.brand}</td>
        <td>${item.chapter}</td>
        <td>${item.qty}</td>
        <td style="text-align: right; padding-right: 8px;">${item.price.toLocaleString()}</td>
        <td>${item.status}</td>
      </tr>
    `).join('');
    
    const totalQty = filteredData.reduce((sum, item) => sum + item.qty, 0);
    const totalPrice = filteredData.reduce((sum, item) => sum + item.price, 0);
    
    document.getElementById('dbTotalQty').textContent = totalQty;
    document.getElementById('dbTotalPrice').textContent = totalPrice.toLocaleString();
  }

  function filterDatabase() {
    renderDatabase();
  }

  // Initialize year filter
  function initYearFilter() {
    const years = [...new Set(SQL_DATABASE.map(item => item.year))].sort();
    const select = document.getElementById('filterYear');
    years.forEach(year => {
      const option = document.createElement('option');
      option.value = year;
      option.textContent = year;
      select.appendChild(option);
    });
  }

  // Generate report
  function generateReport() {
    // Report by Type
    const byType = {};
    SQL_DATABASE.forEach(item => {
      if (!byType[item.type]) {
        byType[item.type] = { qty: 0, price: 0, good: 0, medium: 0, poor: 0, damaged: 0 };
      }
      byType[item.type].qty += item.qty;
      byType[item.type].price += item.price;
      
      if (item.status === 'ល្អ') byType[item.type].good += item.qty;
      else if (item.status === 'មធ្យម') byType[item.type].medium += item.qty;
      else if (item.status === 'អន់') byType[item.type].poor += item.qty;
      else if (item.status === 'ខូច') byType[item.type].damaged += item.qty;
    });
    
    document.getElementById('reportByTypeBody').innerHTML = Object.entries(byType).map(([type, data]) => `
      <tr>
        <td class="align-left" style="padding-left: 8px;">${type}</td>
        <td>${data.qty}</td>
        <td style="text-align: right; padding-right: 8px;">${data.price.toLocaleString()}</td>
        <td>${data.good}</td>
        <td>${data.medium}</td>
        <td>${data.poor}</td>
        <td>${data.damaged}</td>
      </tr>
    `).join('');
    
    // Report by Year
    const byYear = {};
    SQL_DATABASE.forEach(item => {
      if (!byYear[item.year]) {
        byYear[item.year] = { qty: 0, price: 0 };
      }
      byYear[item.year].qty += item.qty;
      byYear[item.year].price += item.price;
    });
    
    document.getElementById('reportByYearBody').innerHTML = Object.entries(byYear)
      .sort(([a], [b]) => a - b)
      .map(([year, data]) => `
        <tr>
          <td>${year}</td>
          <td>${data.qty}</td>
          <td style="text-align: right; padding-right: 8px;">${data.price.toLocaleString()}</td>
        </tr>
      `).join('');
    
    // Report by Status
    const byStatus = {};
    const total = SQL_DATABASE.reduce((sum, item) => sum + item.qty, 0);
    SQL_DATABASE.forEach(item => {
      if (!byStatus[item.status]) byStatus[item.status] = 0;
      byStatus[item.status] += item.qty;
    });
    
    document.getElementById('reportByStatusBody').innerHTML = Object.entries(byStatus).map(([status, qty]) => `
      <tr>
        <td class="align-left" style="padding-left: 8px;">${status}</td>
        <td>${qty}</td>
        <td>${((qty / total) * 100).toFixed(1)}%</td>
      </tr>
    `).join('');
  }

  // Load from database to furniture table
  function loadFromDatabase() {
    const statusMap = {
      'ល្អ': 'good',
      'មធ្យម': 'medium',
      'អន់': 'poor',
      'ខូច': 'damaged'
    };

    const grouped = {};
    SQL_DATABASE.forEach(item => {
      const key = item.name;
      if (!grouped[key]) {
        grouped[key] = {
          name: item.name,
          good: 0,
          medium: 0,
          poor: 0,
          damaged: 0,
          staff: 0,
          student: 0
        };
      }
      
      const statusField = statusMap[item.status] || 'good';
      grouped[key][statusField] += item.qty;
    });

    const tbody = document.getElementById('furnitureBody');
    tbody.innerHTML = '';
    
          Object.values(grouped).forEach((item, index) => {
      const total = item.good + item.medium + item.poor + item.damaged;
      const row = tbody.insertRow();
      row.innerHTML = `
        <td>${index + 1}</td>
        <td class="editable align-left" contenteditable="true">${item.name}</td>
        <td class="editable" contenteditable="true">${item.good}</td>
        <td class="editable" contenteditable="true">${item.medium}</td>
        <td class="editable" contenteditable="true">${item.poor}</td>
        <td class="editable" contenteditable="true">${item.damaged}</td>
        <td class="editable" contenteditable="true">${total}</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td class="editable" contenteditable="true">0</td>
        <td><button class="delete-btn" onclick="deleteRow(this, 'furnitureBody')">លុប</button></td>
      `;
      enableAutoCalculateForRow(row);
    });
    
    calculateFurnitureTotals();
    alert('✅ បានផ្ទុក Database បានជោគជ័យ!');
  }

  // Calculate totals
  function calculateTableTotals(bodyId, totalPrefix, numericColumns) {
    const tbody = document.getElementById(bodyId);
    if (!tbody) return;
    
    const rows = tbody.querySelectorAll('tr');
    const totals = {};
    
    numericColumns.forEach(col => {
      totals[col] = 0;
    });
    
    rows.forEach(row => {
      const cells = row.querySelectorAll('td');
      numericColumns.forEach(colIndex => {
        if (cells[colIndex]) {
          const value = parseFloat(cells[colIndex].textContent) || 0;
          totals[colIndex] += value;
        }
      });
    });
    
    numericColumns.forEach((colIndex, i) => {
      const totalCell = document.getElementById(`${totalPrefix}_${i}`);
      if (totalCell) {
        totalCell.textContent = totals[colIndex];
      }
    });
  }

  function calculateLandTotals() {
    calculateTableTotals('landBody', 'landTotal', [2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]);
  }

  function calculateBuildingTotals() {
    calculateTableTotals('buildingBody', 'buildingTotal', [2, 3, 4, 5, 6, 7, 8, 9, 10, 11]);
  }

  function calculateVehicleTotals() {
    calculateTableTotals('vehicleBody', 'vehicleTotal', [2, 3, 4, 5, 6, 7, 8]);
  }

  function calculateTechnicalTotals() {
    calculateTableTotals('technicalBody', 'technicalTotal', [2, 3, 4, 5, 6, 7, 8]);
  }

  function calculateFurnitureTotals() {
    calculateTableTotals('furnitureBody', 'furnitureTotal', [2, 3, 4, 5, 6, 7, 8, 9, 10]);
  }

  function calculateAllTotals() {
    calculateLandTotals();
    calculateBuildingTotals();
    calculateVehicleTotals();
    calculateTechnicalTotals();
    calculateFurnitureTotals();
    alert('✅ បានគណនាសរុបរួចរាល់!');
  }

  // Add rows
  function addLandRow() {
    const tbody = document.getElementById('landBody');
    const rowCount = tbody.rows.length + 1;
    const row = tbody.insertRow();
    
    row.innerHTML = `
      <td>${rowCount}</td>
      <td class="editable align-left" contenteditable="true"></td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td><button class="delete-btn" onclick="deleteRow(this, 'landBody')">លុប</button></td>
    `;
    
    enableAutoCalculateForRow(row);
    calculateLandTotals();
  }

  function addBuildingRow() {
    const tbody = document.getElementById('buildingBody');
    const rowCount = tbody.rows.length + 1;
    const row = tbody.insertRow();
    
    row.innerHTML = `
      <td>${rowCount}</td>
      <td class="editable align-left" contenteditable="true"></td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true"></td>
      <td><button class="delete-btn" onclick="deleteRow(this, 'buildingBody')">លុប</button></td>
    `;
    
    enableAutoCalculateForRow(row);
    calculateBuildingTotals();
  }

  function addVehicleRow() {
    const tbody = document.getElementById('vehicleBody');
    const rowCount = tbody.rows.length + 1;
    const row = tbody.insertRow();
    
    row.innerHTML = `
      <td>${rowCount}</td>
      <td class="editable align-left" contenteditable="true"></td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true"></td>
      <td><button class="delete-btn" onclick="deleteRow(this, 'vehicleBody')">លុប</button></td>
    `;
    
    enableAutoCalculateForRow(row);
    calculateVehicleTotals();
  }

  function addTechnicalRow() {
    const tbody = document.getElementById('technicalBody');
    const rowCount = tbody.rows.length + 1;
    const row = tbody.insertRow();
    
    row.innerHTML = `
      <td>${rowCount}</td>
      <td class="editable align-left" contenteditable="true"></td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true"></td>
      <td><button class="delete-btn" onclick="deleteRow(this, 'technicalBody')">លុប</button></td>
    `;
    
    enableAutoCalculateForRow(row);
    calculateTechnicalTotals();
  }

  function addFurnitureRow() {
    const tbody = document.getElementById('furnitureBody');
    const rowCount = tbody.rows.length + 1;
    const row = tbody.insertRow();
    
    row.innerHTML = `
      <td>${rowCount}</td>
      <td class="editable align-left" contenteditable="true"></td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td class="editable" contenteditable="true">0</td>
      <td><button class="delete-btn" onclick="deleteRow(this, 'furnitureBody')">លុប</button></td>
    `;
    
    enableAutoCalculateForRow(row);
    calculateFurnitureTotals();
  }

  // Delete row
  function deleteRow(btn, bodyId) {
    if (confirm('តើអ្នកពិតជាចង់លុបជួរនេះមែនទេ?')) {
      const row = btn.parentNode.parentNode;
      const tbody = document.getElementById(bodyId);
      row.remove();
      
      Array.from(tbody.rows).forEach((r, idx) => {
        r.cells[0].innerHTML = idx + 1;
      });
      
      if (bodyId === 'landBody') calculateLandTotals();
      else if (bodyId === 'buildingBody') calculateBuildingTotals();
      else if (bodyId === 'vehicleBody') calculateVehicleTotals();
      else if (bodyId === 'technicalBody') calculateTechnicalTotals();
      else if (bodyId === 'furnitureBody') calculateFurnitureTotals();
    }
  }

  // Save and load data
  function saveData() {
    try {
      const data = {
        authority: document.getElementById('authority').value,
        unit: document.getElementById('unit').value,
        user: document.getElementById('user').value,
        school: document.getElementById('school').value,
        landBody: getTableData('landBody'),
        buildingBody: getTableData('buildingBody'),
        vehicleBody: getTableData('vehicleBody'),
        technicalBody: getTableData('technicalBody'),
        furnitureBody: getTableData('furnitureBody')
      };

      localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
      alert('✅ បានរក្សាទុកទិន្នន័យដោយជោគជ័យ!');
    } catch (error) {
      alert('❌ មានបញ្ហា: ' + error.message);
    }
  }

  function getTableData(bodyId) {
    const tbody = document.getElementById(bodyId);
    const rows = [];
    
    Array.from(tbody.rows).forEach(row => {
      const rowData = [];
      Array.from(row.cells).forEach((cell, index) => {
        if (index < row.cells.length - 1) {
          rowData.push(cell.innerText.trim());
        }
      });
      rows.push(rowData);
    });
    
    return rows;
  }

  function loadData() {
    try {
      const saved = localStorage.getItem(STORAGE_KEY);
      if (!saved) {
        console.log('មិនមានទិន្នន័យដែលបានរក្សាទុកទេ');
        return;
      }
      
      const data = JSON.parse(saved);

      if (data.authority) document.getElementById('authority').value = data.authority;
      if (data.unit) document.getElementById('unit').value = data.unit;
      if (data.user) document.getElementById('user').value = data.user;
      if (data.school) document.getElementById('school').value = data.school;

      if (data.landBody) loadTableData('landBody', data.landBody);
      if (data.buildingBody) loadTableData('buildingBody', data.buildingBody);
      if (data.vehicleBody) loadTableData('vehicleBody', data.vehicleBody);
      if (data.technicalBody) loadTableData('technicalBody', data.technicalBody);
      if (data.furnitureBody) loadTableData('furnitureBody', data.furnitureBody);

      calculateAllTotals();
      
      alert('✅ បានផ្ទុកទិន្នន័យដោយជោគជ័យ!');
    } catch (error) {
      alert('❌ មានបញ្ហា: ' + error.message);
    }
  }

  function loadTableData(bodyId, rowsData) {
    const tbody = document.getElementById(bodyId);
    tbody.innerHTML = '';
    
    rowsData.forEach((rowData, index) => {
      const row = tbody.insertRow();
      
      for (let i = 0; i < rowData.length; i++) {
        const cell = row.insertCell(i);
        cell.innerText = rowData[i] || '';
        
        if (i === 0) {
          cell.innerText = index + 1;
        } else if (i === 1) {
          cell.className = "editable align-left";
          cell.contentEditable = "true";
        } else {
          cell.className = "editable";
          cell.contentEditable = "true";
        }
      }
      
      const lastCell = row.insertCell(rowData.length);
      lastCell.innerHTML = `<button class="delete-btn" onclick="deleteRow(this, '${bodyId}')">លុប</button>`;
      
      enableAutoCalculateForRow(row);
    });
  }

  function clearData() {
    if (confirm('⚠️ តើអ្នកប្រាកដថាចង់លុបទិន្នន័យទាំងអស់?')) {
      document.querySelectorAll('[contenteditable="true"]').forEach(cell => {
        if (cell.classList.contains('align-left')) {
          cell.textContent = '';
        } else {
          cell.textContent = '0';
        }
      });

      localStorage.removeItem(STORAGE_KEY);
      
      calculateLandTotals();
      calculateBuildingTotals();
      calculateVehicleTotals();
      calculateTechnicalTotals();
      calculateFurnitureTotals();
      
      alert('🗑️ បានលុបទិន្នន័យរួចរាល់!');
    }
  }

  // Auto calculate
  function enableAutoCalculateForRow(row) {
    row.querySelectorAll('[contenteditable="true"]').forEach(cell => {
      cell.addEventListener('blur', function() {
        const tbody = this.closest('tbody');
        if (tbody) {
          const bodyId = tbody.id;
          if (bodyId === 'landBody') calculateLandTotals();
          else if (bodyId === 'buildingBody') calculateBuildingTotals();
          else if (bodyId === 'vehicleBody') calculateVehicleTotals();
          else if (bodyId === 'technicalBody') calculateTechnicalTotals();
          else if (bodyId === 'furnitureBody') calculateFurnitureTotals();
        }
      });
      
      cell.addEventListener('keydown', function(e) {
        if (e.key === 'Enter') {
          e.preventDefault();
          this.blur();
        }
      });
    });
  }

  function enableAutoCalculate() {
    document.querySelectorAll('tbody tr').forEach(row => {
      enableAutoCalculateForRow(row);
    });
  }

  // Initialize
  window.onload = function() {
    enableAutoCalculate();
    initYearFilter();
    renderDatabase();
    
    calculateLandTotals();
    calculateBuildingTotals();
    calculateVehicleTotals();
    calculateTechnicalTotals();
    calculateFurnitureTotals();
  }
</script>

</body>
</html>