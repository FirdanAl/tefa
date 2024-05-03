<template>
    <div>
        <canvas id="statistik"></canvas>
    </div>
</template>

<script setup>
import Chart from 'char.js/auto'

const labels = [
    'Januari',
    'Pebruari',
    'Maret',
    'April',
    'Mei',
    'Juni',
    'Juli',
    'Agustus',
    'September',
    'Oktober',
    'November',
    'Desember',
];

const data = {
    labels: labels,
    datasets: [{
        label: 'Pengujung',
        data: [1, 5, 7, 4, 10, 6, 8, 9, 0, 2,],
        backgroundColor: [
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
            'rgb(0, 120, 255)',
        ]
    }]
};

const config = {
    type: 'bar',
    data: data,
    options: {}
};

onMounted(() => {
    const myChart = new Chart(
        document.getElementById('statistik'),
    );
})
</script>