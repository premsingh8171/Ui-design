@page "/dashboard"

<div class="header">
    <h1>BCP1PROCESSING</h1>
    <p>Start: 2024-11-20 00:00:01 | End: 2024-11-21 00:00:00</p>
</div>

<div class="dashboard">
    <!-- Gauges Section -->
    <div class="gauges">
        <div class="gauge">
            <h4>Downtime</h4>
            <div class="speed-meter" data-value="7.1" data-min="0" data-max="15" style="--value: 7.1; --min: 0; --max: 15;"></div>
            <p class="gauge-value">7.1</p>
        </div>
        <div class="gauge">
            <h4>Tput v. Sched</h4>
            <div class="speed-meter" data-value="96.1" data-min="0" data-max="100" style="--value: 96.1; --min: 0; --max: 100;"></div>
            <p class="gauge-value">96.1</p>
        </div>
        <div class="gauge">
            <h4>Waste</h4>
            <div class="speed-meter" data-value="0" data-min="0" data-max="10" style="--value: 0; --min: 0; --max: 10;"></div>
            <p class="gauge-value">0.0</p>
        </div>
        <div class="gauge">
            <h4>Labor</h4>
            <div class="speed-meter" data-value="770.9" data-min="0" data-max="1000" style="--value: 770.9; --min: 0; --max: 1000;"></div>
            <p class="gauge-value">770.9</p>
        </div>
        <div class="gauge">
            <h4>OEE</h4>
            <div class="speed-meter" data-value="92.9" data-min="0" data-max="100" style="--value: 92.9; --min: 0; --max: 100;"></div>
            <p class="gauge-value">92.9</p>
        </div>
    </div>

    <!-- Downtime Table -->
    <div class="table-container">
        <h3>Downtime Events</h3>
        <table>
            <thead>
                <tr>
                    <th>Start Time</th>
                    <th>End Time</th>
                    <th>Duration</th>
                    <th>Product</th>
                    <th>Cause</th>
                    <th>Details</th>
                    <th>Operator</th>
                    <th>Manual</th>
                    <th>Comments</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>2024-11-20 20:56:45</td>
                    <td>2024-11-20 22:39:41</td>
                    <td>1.72</td>
                    <td>0350-BKD CHEETOS F</td>
                    <td>Pkg-Automation</td>
                    <td>Details</td>
                    <td>Unspecified</td>
                    <td></td>
                    <td></td>
                </tr>
            </tbody>
        </table>
    </div>

    <!-- Run Right Indicators -->
    <div class="charts">
        <h3>Run Right Indicators</h3>
        <div class="chart">
            <h4>Oven Dwell Time</h4>
            <p>Avg: 6.65</p>
        </div>
        <div class="chart">
            <h4>Oven Temp</h4>
            <p>Avg: 0</p>
        </div>
        <div class="chart">
            <h4>LAB-MOISTURE FRYER 1</h4>
            <p>Avg: 1.2162</p>
        </div>
    </div>
</div>

<style>
    /* Header Styling */
    .header {
        text-align: center;
        background-color: #f4f4f4;
        padding: 1rem;
        border-bottom: 2px solid #ccc;
    }

    .header h1 {
        margin: 0;
    }

    .dashboard {
        padding: 1rem;
    }

    /* Gauges Section */
    .gauges {
        display: flex;
        justify-content: space-around;
        margin-bottom: 2rem;
    }

    .gauge {
        text-align: center;
    }

    .speed-meter {
        width: 100px;
        height: 100px;
        background: conic-gradient(
            red calc(var(--value) / var(--max) * 360deg),
            #e0e0e0 0
        );
        border-radius: 50%;
        margin: 0 auto;
        position: relative;
    }

    .speed-meter::after {
        content: attr(data-value);
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 1.2rem;
        font-weight: bold;
    }

    .gauge-value {
        font-size: 1.1rem;
        font-weight: bold;
        margin-top: 0.5rem;
    }

    /* Table Styling */
    .table-container {
        overflow-x: auto;
        margin-bottom: 2rem;
    }

    table {
        width: 100%;
        border-collapse: collapse;
    }

    th, td {
        padding: 0.5rem;
        text-align: left;
        border: 1px solid #ccc;
    }

    th {
        background-color: #f4f4f4;
    }

    /* Charts Section */
    .charts {
        display: grid;
        gap: 1rem;
    }

    .chart {
        padding: 1rem;
        background: #f9f9f9;
        border: 1px solid #ccc;
        border-radius: 0.5rem;
        text-align: center;
    }
</style>
