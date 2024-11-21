# Ui-design

@page "/dashboard"

<h3>BCP1PROCESSING</h3>
<div class="dashboard-container">
    <div class="gauge-container">
        <div class="gauge">
            <h4>Downtime</h4>
            <span class="gauge-value" style="color: red;">7.1</span>
        </div>
        <div class="gauge">
            <h4>Tput v. Sched</h4>
            <span class="gauge-value" style="color: green;">96.1</span>
        </div>
        <div class="gauge">
            <h4>Waste</h4>
            <span class="gauge-value" style="color: green;">0.0</span>
        </div>
        <div class="gauge">
            <h4>Labor</h4>
            <span class="gauge-value" style="color: green;">770.9</span>
        </div>
        <div class="gauge">
            <h4>OEE</h4>
            <span class="gauge-value" style="color: green;">92.9</span>
        </div>
    </div>

    <div class="table-container">
        <h4>Downtime Events</h4>
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

    <div class="charts-container">
        <h4>Run Right Indicators</h4>
        <div class="chart">
            <h5>Oven Dwell Time</h5>
            <p>Avg: 6.65</p>
            <!-- Add your chart here -->
        </div>
        <div class="chart">
            <h5>Oven Temp</h5>
            <p>Avg: 0</p>
            <!-- Add your chart here -->
        </div>
        <div class="chart">
            <h5>LAB-MOISTURE FRYER 1</h5>
            <p>Avg: 1.2162</p>
            <!-- Add your chart here -->
        </div>
    </div>
</div>

<style>
    .dashboard-container {
        display: grid;
        grid-template-rows: auto auto auto;
        gap: 1rem;
    }

    .gauge-container {
        display: flex;
        justify-content: space-around;
    }

    .gauge {
        text-align: center;
    }

    .gauge-value {
        font-size: 1.5rem;
        font-weight: bold;
    }

    .table-container {
        overflow-x: auto;
    }

    table {
        width: 100%;
        border-collapse: collapse;
    }

    th, td {
        padding: 0.5rem;
        border: 1px solid #ddd;
        text-align: left;
    }

    .charts-container {
        display: flex;
        flex-direction: column;
    }

    .chart {
        margin-bottom: 1rem;
    }
</style>
