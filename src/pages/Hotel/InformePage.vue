<template>
    <layautPage title="Informes del
            hotel">
        <div class="w-full">
            <div class="w-full flex gap-10 flex-wrap mb-20 items-center justify-center">
                <div class="w-full">
                    <canvas ref="migrafica2"></canvas>
                </div>
                <div class="w-full">
                    <canvas ref="migrafica1"></canvas>
                </div>
            </div>

            <div class="flex items-center justify-between mb-20 ml-5">
                <ButtonLink text="Regresar" backgroundColor="blue" to="/"></ButtonLink>
            </div>
        </div>
    </layautPage>
</template>
<script>
import LayautPage from "@/components/LayautPage.vue";
import ButtonLink from "@/components/ButtonLink.vue";
import Chart from 'chart.js/auto';

export default {
    mounted() {
        const ctx = this.$refs.migrafica1
        const ctx2 = this.$refs.migrafica2
        let data1 = ['Estandar', 'Junior', 'Suite']
        let data2 = [5, 10, 20];
        let data3 = ['Sencilla', 'Doble', 'Triple', 'Cuadruple']
        let data4 = [5, 20, 10, 30];
        new Chart(ctx, {
            type: 'bar',
            data: {
                labels: data1,
                datasets: [{
                    label: 'Grafico de barras',
                    data: data2,
                    backgroundColor: [
                        '#e11d48',
                        '#9333ea',
                        '#0284c7',
                        '#d97706'
                    ],
                }]
            },
            options: {
                plugins: {
                    title: {
                        display: true,
                        text: 'Habitaciones por tipo'
                    }
                },
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });
        new Chart(ctx2, {
            type: 'bar',
            data: {
                labels: data3,
                datasets: [{
                    label: 'Grafico de barras',
                    data: data4,
                    backgroundColor: [
                        '#e11d48',
                        '#9333ea',
                        '#0284c7',
                        '#d97706'
                    ],
                }]
            },
            options: {
                plugins: {
                    title: {
                        display: true,
                        text: 'Habitaciones por acomodación'
                    }
                },
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });
    },
    components: {
        LayautPage,
        ButtonLink
    },
    data() {
        return {
            id: this.$route.params.id
        }
    },
    methods: {
    }
}
</script>