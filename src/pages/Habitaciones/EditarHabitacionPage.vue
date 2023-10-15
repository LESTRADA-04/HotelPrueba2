<template>
    <layautPage title="Editar Habitacion">
        <form class="px-8 pt-6 pb-8 mb-4 w-full">
            <div class="flex items-center justify-between mb-10">
                <div class="flex items-start justify-between flex-col">
                    <div class="flex items-center justify-between">
                        <img src="@/assets/logo.png" alt="hotel" class="w-16">
                        <h2 class="px-5 text-3xl font-bold">Hotel caribe</h2>
                    </div>
                    <p class="text-lg font-semibold">Habitaciones: <span>100</span></p>
                </div>
            </div>
            <div class="mb-4">
                <div class="grid grid-flow-row md:grid-flow-col gap-3">
                    <div class="sm:col-span-4 justify-center">
                        <label for="nombre" class="block mb-2 text-sm font-medium text-gray-900 ">Codigo de
                            habitacion</label>
                        <input type="text" id="nombre"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                            placeholder="Codigo de habitacion" required value="10">
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500"><span class="font-medium">Error!</span>
                            Mensaje.</p>
                    </div>

                    <div class="sm:col-span-4 justify-center">
                        <label for="countries" class="block mb-2 text-sm font-medium text-gray-900">Tipo de
                            habitacion</label>
                        <select id="countries"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5">
                            <option value="ESTANDAR">ESTANDAR</option>
                            <option selected value="JUNIOR">JUNIOR</option>
                            <option value="SUITE">SUITE</option>
                        </select>

                        <p class="mt-2 text-sm text-red-600 dark:text-red-500"><span class="font-medium">Error!</span>
                            Mensaje.</p>
                    </div>
                </div>
            </div>
            <div class="mb-4">
                <div class="grid grid-flow-row md:grid-flow-col gap-3">
                    <div class="sm:col-span-4 justify-center">
                        <label for="countries" class="block mb-2 text-sm font-medium text-gray-900">Tipo de
                            acomodacion</label>
                        <select id="countries"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 ">
                            <option value="ESTANDAR">SENCILLA</option>
                            <option value="JUNIOR">DOBLE</option>
                            <option selected value="SUITE">TRIPLE</option>
                            <option value="SUITE">CUADRUPLE</option>
                        </select>
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500"><span class="font-medium">Error!</span>
                            Mensaje.</p>
                    </div>
                </div>
            </div>
            <div class="flex items-center justify-between">
                <ButtonLink text="Regresar" backgroundColor="blue" :to="'/detallesHoteles/Habitaciones/' + this.id">
                </ButtonLink>
            </div>
        </form>
    </layautPage>
</template>
<script>
import LayautPage from "@/components/LayautPage.vue";
import ButtonLink from "@/components/ButtonLink.vue";
export default {
    components: {
        LayautPage,
        ButtonLink
    },
    data() {
        return {
            id: this.$route.params.id
        }
    },
}
</script>