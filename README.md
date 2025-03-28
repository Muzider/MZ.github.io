<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>标准工程图</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            font-size: 14px;
            background-color: white;
            margin: 0;
            padding: 20px;
        }

        h1 {
            font-weight: bold;
            font-size: 18px;
            color: #007BFF;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            border: 1px solid #DDD;
            margin-bottom: 20px;
        }

        th {
            background-color: #007BFF;
            color: white;
            padding: 10px;
            text-align: center; /* 表头内容居中 */
        }

        td {
            padding: 10px;
            border: 1px solid #DDD;
            text-align: center; /* 表格单元格内容居中 */
        }

        tr:nth-child(even) {
            background-color: #F9F9F9;
        }

        input[type="text"],
        input[type="date"],
        select {
            width: 100%;
            padding: 5px;
            box-sizing: border-box;
        }

        button {
            padding: 5px 10px;
            margin-right: 5px;
        }

       .additional-section {
            display: flex;
            margin-top: 20px;
        }

       .section {
            flex: 1;
            border: 1px solid #DDD;
            padding: 10px;
            margin-right: 10px;
        }

       .section:last-child {
            margin-right: 0;
        }

       .section h2 {
            font-size: 16px;
            color: #007BFF;
            margin-top: 0;
        }
    </style>
</head>

<body>
    <h1>标准工程图</h1>
    <table>
        <tbody>
            <tr>
                <td>船号：</td>
                <td><input type="text" placeholder="请输入船号" id="shipNumber" /></td>
                <td>分段号：</td>
                <td><input type="text" placeholder="请输入分段号" id="sectionNumber" /></td>
            </tr>
            <tr>
                <td>开始日期：</td>
                <td><input type="date" id="startDate" /></td>
                <td>结束日期：</td>
                <td><input type="date" id="endDate" /></td>
            </tr>
            <tr>
                <td>作业班组：</td>
                <td><input type="text" placeholder="请输入作业班组" id="workTeam" /></td>
                <td>版本信息：</td>
                <td><input type="text" placeholder="请输入版本信息" id="versionInfo" /></td>
            </tr>
        </tbody>
    </table>
    <table id="taskTable">
        <thead>
            <tr>
                <th>序号</th>
                <th onclick="sortTable(1)">标准工序</th>
                <th onclick="sortTable(2)">工种</th>
                <th onclick="sortTable(3)">内容</th>
                <th onclick="sortTable(4)">人员</th>
                <th onclick="sortTable(5)">计划工时</th>
                <th onclick="sortTable(6)">实动工时</th>
                <th onclick="sortTable(7)">第1天</th>
                <th onclick="sortTable(8)">第2天</th>
                <th onclick="sortTable(9)">第3天</th>
                <th onclick="sortTable(10)">第4天</th>
                <th onclick="sortTable(11)">第5天</th>
                <th onclick="sortTable(12)">第6天</th>
                <th onclick="sortTable(13)">第7天</th>
                <th>备注</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td contenteditable="true">胎架制作</td>
                <td>
                    <select>
                        <option value="装配">装配</option>
                        <option value="焊接">焊接</option>
                    </select>
                </td>
                <td contenteditable="true">制作胎架的具体内容</td>
                <td contenteditable="true">王五</td>
                <td contenteditable="false">10</td>
                <td contenteditable="false">8</td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="true">胎架制作备注</td>
            </tr>
            <tr>
                <td>2</td>
                <td contenteditable="true">甲板拼板</td>
                <td>
                    <select>
                        <option value="装配">装配</option>
                        <option value="焊接">焊接</option>
                    </select>
                </td>
                <td contenteditable="true">拼接甲板的具体内容</td>
                <td contenteditable="true">赵六</td>
                <td contenteditable="false">8</td>
                <td contenteditable="false">6</td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="true">甲板拼板备注</td>
            </tr>
            <tr>
                <td>3</td>
                <td contenteditable="true">甲板焊接</td>
                <td>
                    <select>
                        <option value="装配">装配</option>
                        <option value="焊接">焊接</option>
                    </select>
                </td>
                <td contenteditable="true">焊接甲板的具体内容</td>
                <td contenteditable="true">孙七</td>
                <td contenteditable="false">6</td>
                <td contenteditable="false">5</td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="true">甲板焊接备注</td>
            </tr>
            <tr>
                <td>4</td>
                <td contenteditable="true">外板吊装</td>
                <td>
                    <select>
                        <option value="装配">装配</option>
                        <option value="焊接">焊接</option>
                    </select>
                </td>
                <td contenteditable="true">吊装外板的具体内容</td>
                <td contenteditable="true">周八</td>
                <td contenteditable="false">12</td>
                <td contenteditable="false">10</td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="true">外板吊装备注</td>
            </tr>
            <tr>
                <td>5</td>
                <td contenteditable="true">外板点焊</td>
                <td>
                    <select>
                        <option value="装配">装配</option>
                        <option value="焊接">焊接</option>
                    </select>
                </td>
                <td contenteditable="true">点焊外板的具体内容</td>
                <td contenteditable="true">吴九</td>
                <td contenteditable="false">8</td>
                <td contenteditable="false">7</td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="false"></td>
                <td contenteditable="true">外板点焊备注</td>
            </tr>
            <tr>
                <td colspan="5" style="text-align: right;">装配计划总工时</td>
                <td id="assemblyPlanTotalHours">0</td>
                <td colspan="9"></td>
            </tr>
            <tr>
                <td colspan="5" style="text-align: right;">装配实动总工时</td>
                <td id="assemblyActualTotalHours">0</td>
                <td colspan="9"></td>
            </tr>
            <tr>
                <td colspan="5" style="text-align: right;">焊接计划总工时</td>
                <td id="weldingPlanTotalHours">0</td>
                <td colspan="9"></td>
            </tr>
            <tr>
                <td colspan="5" style="text-align: right;">焊接实动总工时</td>
                <td id="weldingActualTotalHours">0</td>
                <td colspan="9"></td>
            </tr>
        </tbody>
    </table>
    <button onclick="saveData()">保存</button>
    <button onclick="editData()">编辑</button>
    <button onclick="deleteData()">删除</button>
    <button onclick="loadData()">加载数据</button>

    <div class="additional-section">
        <div class="section">
            <h2>安全事项</h2>
            <textarea rows="10" cols="30" placeholder="请输入安全事项" id="safetyMatters"></textarea>
        </div>
        <div class="section">
            <h2>DAP 图</h2>
            <img id="dapImage" src="https://dummyimage.com/300x200/000/fff&text=DAP+图" alt="DAP 图">
            <input type="file" id="imageUpload" accept="image/*">
            <button onclick="uploadImage()">上传</button>
            <button onclick="downloadImage()">下载</button>
        </div>
        <div class="section">
            <h2>托盘信息</h2>
            <table>
                <thead>
                    <tr>
                        <th>托盘编号</th>
                        <th>托盘明细</th>
                        <th>需求日期</th>
                        <th>是否确认</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><input type="text" placeholder="编号" id="trayNumber" /></td>
                        <td><input type="text" placeholder="明细" id="trayDetails" /></td>
                        <td><input type="date" id="demandDate" /></td>
                        <td>
                            <select id="isConfirmed">
                                <option value="是">是</option>
                                <option value="否">否</option>
                            </select>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>

    <script>
        function sortTable(n) {
            var table, rows, switching, i, x, y, shouldSwitch, dir, switchcount = 0;
            table = document.getElementById("taskTable");
            switching = true;
            dir = "asc";
            while (switching) {
                switching = false;
                rows = table.rows;
                for (i = 1; i < (rows.length - 5); i++) {
                    shouldSwitch = false;
                    x = rows[i].getElementsByTagName("TD")[n];
                    y = rows[i + 1].getElementsByTagName("TD")[n];
                    if (dir == "asc") {
                        if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
                            shouldSwitch = true;
                            break;
                        }
                    } else if (dir == "desc") {
                        if (x.innerHTML.toLowerCase() < y.innerHTML.toLowerCase()) {
                            shouldSwitch = true;
                            break;
                        }
                    }
                }
                if (shouldSwitch) {
                    rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
                    switching = true;
                    switchcount++;
                } else {
                    if (switchcount == 0 && dir == "asc") {
                        dir = "desc";
                        switching = true;
                    }
                }
            }
        }

        function saveData() {
            const shipNumber = document.getElementById('shipNumber').value;
            const sectionNumber = document.getElementById('sectionNumber').value;
            const startDate = document.getElementById('startDate').value;
            const endDate = document.getElementById('endDate').value;
            const workTeam = document.getElementById('workTeam').value;
            const versionInfo = document.getElementById('versionInfo').value;
            const safetyMatters = document.getElementById('safetyMatters').value;
            const trayNumber = document.getElementById('trayNumber').value;
            const trayDetails = document.getElementById('trayDetails').value;
            const demandDate = document.getElementById('demandDate').value;
            const isConfirmed = document.getElementById('isConfirmed').value;

            const taskRows = document.querySelectorAll('#taskTable tbody tr:not(:nth-last-child(-n+4))');
            const tasks = [];
            taskRows.forEach(row => {
                const cells = row.cells;
                const task = {
                    sequence: cells[0].textContent,
                    process: cells[1].textContent,
                    jobType: cells[2].querySelector('select').value,
                    content: cells[3].textContent,
                    person: cells[4].textContent,
                    planHours: cells[5].textContent,
                    actualHours: cells[6].textContent,
                    day1: cells[7].textContent,
                    day2: cells[8].textContent,
                    day3: cells[9].textContent,
                    day4: cells[10].textContent,
                    day5: cells[11].textContent,
                    day6: cells[12].textContent,
                    day7: cells[13].textContent,
                    remarks: cells[14].textContent
                };
                tasks.push(task);
            });

            const data = {
                shipNumber,
                sectionNumber,
                startDate,
                endDate,
                workTeam,
                versionInfo,
                safetyMatters,
                trayNumber,
                trayDetails,
                demandDate,
                isConfirmed,
                tasks
            };

            localStorage.setItem('engineeringData', JSON.stringify(data));
            alert("保存成功");
        }

        function loadData() {
            const data = JSON.parse(localStorage.getItem('engineeringData'));
            if (data) {
                document.getElementById('shipNumber').value = data.shipNumber;
                document.getElementById('sectionNumber').value = data.sectionNumber;
                document.getElementById('startDate').value = data.startDate;
                document.getElementById('endDate').value = data.endDate;
                document.getElementById('workTeam').value = data.workTeam;
                document.getElementById('versionInfo').value = data.versionInfo;
                document.getElementById('safetyMatters').value = data.safetyMatters;
                document.getElementById('trayNumber').value = data.trayNumber;
                document.getElementById('trayDetails').value = data.trayDetails;
                document.getElementById('demandDate').value = data.demandDate;
                document.getElementById('isConfirmed').value = data.isConfirmed;

                const taskRows = document.querySelectorAll('#taskTable tbody tr:not(:nth-last-child(-n+4))');
                data.tasks.forEach((task, index) => {
                    const cells = taskRows[index].cells;
                    cells[0].textContent = task.sequence;
                    cells[1].textContent = task.process;
                    cells[2].querySelector('select').value = task.jobType;
                    cells[3].textContent = task.content;
                    cells[4].textContent = task.person;
                    cells[5].textContent = task.planHours;
                    cells[6].textContent = task.actualHours;
                    cells[7].textContent = task.day1;
                    cells[8].textContent = task.day2;
                    cells[9].textContent = task.day3;
                    cells[10].textContent = task.day4;
                    cells[11].textContent = task.day5;
                    cells[12].textContent = task.day6;
                    cells[13].textContent = task.day7;
                    cells[14].textContent = task.remarks;
                });
            }
            alert("数据加载成功");
        }

        function editData() {
            const hoursCells = document.querySelectorAll('#taskTable tbody td:nth-child(n+6):nth-child(-n+13)');
            hoursCells.forEach(cell => {
                cell.contentEditable = true;
            });
            alert("进入编辑模式");
        }

        function deleteData() {
            // 可以添加删除逻辑
            alert("删除操作");
        }

        function calculateTotalHours() {
            const rows = document.querySelectorAll('#taskTable tbody tr:not(:nth-last-child(-n+4))');
            let assemblyPlanTotal = 0;
            let assemblyActualTotal = 0;
            let weldingPlanTotal = 0;
            let weldingActualTotal = 0;
            rows.forEach(row => {
                const jobTypeCell = row.cells[2];
                const planHoursCell = row.cells[5];
                const actualHoursCell = row.cells[6];
                const jobType = jobTypeCell.querySelector('select').value;
                const planHours = parseFloat(planHoursCell.textContent);
                const actualHours = parseFloat(actualHoursCell.textContent);
                if (!isNaN(planHours)) {
                    if (jobType === '装配') {
                        assemblyPlanTotal += planHours;
                    } else if (jobType === '焊接') {
                        weldingPlanTotal += planHours;
                    }
                }
                if (!isNaN(actualHours)) {
                    if (jobType === '装配') {
                        assemblyActualTotal += actualHours;
                    } else if (jobType === '焊接') {
                        weldingActualTotal += actualHours;
                    }
                }
            });
            document.getElementById('assemblyPlanTotalHours').textContent = assemblyPlanTotal;
            document.getElementById('assemblyActualTotalHours').textContent = assemblyActualTotal;
            document.getElementById('weldingPlanTotalHours').textContent = weldingPlanTotal;
            document.getElementById('weldingActualTotalHours').textContent = weldingActualTotal;
        }

        function uploadImage() {
            const input = document.getElementById('imageUpload');
            const file = input.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function (e) {
                    const img = document.getElementById('dapImage');
                    img.src = e.target.result;
                };
                reader.readAsDataURL(file);
            }
        }

        function downloadImage() {
            const img = document.getElementById('dapImage');
            const link = document.createElement('a');
            link.href = img.src;
            link.download = 'dap_image.png';
            link.click();
        }

        // 添加事件监听器，当计划工时或实动工时内容发生变化时重新计算总工时
        const planHoursCells = document.querySelectorAll('#taskTable tbody td:nth-child(6)');
        const actualHoursCells = document.querySelectorAll('#taskTable tbody td:nth-child(7)');

        planHoursCells.forEach(cell => {
            cell.addEventListener('input', calculateTotalHours);
        });

        actualHoursCells.forEach(cell => {
            cell.addEventListener('input', calculateTotalHours);
        });

        window.onload = function () {
            loadData();
            calculateTotalHours();
        };
    </script>
</body>

</html>    
