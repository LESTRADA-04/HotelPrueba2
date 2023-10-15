<template>
    <layautPage title="Detalles del
            hotel">
        <!-- Formulario -->
        <form class="px-8 pt-6 pb-8 mb-4 w-full">
            <div class="mb-4">
                <div class="grid grid-flow-row md:grid-flow-col gap-3">
                    <div class="sm:col-span-4 justify-center">
                        <label for="nit" class="block mb-2 text-sm font-medium text-gray-900 ">NIT</label>
                        <input type="text" id="nit"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                            placeholder="0000000000-0" required value="123456789-0" disabled>
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500 hidden"><span
                                class="font-medium">Error!</span> Mensaje.</p>
                    </div>
                    <div class="sm:col-span-4 justify-center">
                        <label for="nombre" class="block mb-2 text-sm font-medium text-gray-900 ">Nombre</label>
                        <input type="text" id="nombre"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                            placeholder="Nombre del hotel" required value="Hotel caribe" disabled>
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500 hidden"><span
                                class="font-medium">Error!</span> Mensaje.</p>
                    </div>
                </div>
            </div>
            <div class="mb-4">
                <div class="grid grid-flow-row md:grid-flow-col gap-3">
                    <div class="sm:col-span-4 justify-center">
                        <label for="ciudad" class="block mb-2 text-sm font-medium text-gray-900 ">Ciudad</label>
                        <input type="text" id="ciudad"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                            placeholder="Nombre de la ciudad" required value="Barranquilla" disabled>
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500 hidden"><span
                                class="font-medium">Error!</span> Mensaje.</p>
                    </div>
                    <div class="sm:col-span-4 justify-center">
                        <label for="direccion" class="block mb-2 text-sm font-medium text-gray-900 ">Dirección</label>
                        <input type="text" id="direccion"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                            placeholder="Cr 10 #2-11" required value="Cr 10 #2-11" disabled>
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500 hidden"><span
                                class="font-medium">Error!</span> Mensaje.</p>
                    </div>
                </div>
            </div>
            <div class="mb-4">
                <div class="grid grid-flow-row md:grid-flow-col gap-3">
                    <div class="sm:col-span-4 justify-center">
                        <label for="num_habitaciones" class="block mb-2 text-sm font-medium text-gray-900 ">Numero maximo de
                            habitaciones</label>
                        <input type="number" id="num_habitaciones"
                            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                            placeholder="0" required value="100" disabled>
                        <p class="mt-2 text-sm text-red-600 dark:text-red-500 hidden"><span
                                class="font-medium">Error!</span> Mensaje.</p>
                    </div>
                </div>
            </div>
            <div class="flex items-center justify-between">
                <ButtonLink text="Regresar" backgroundColor="blue" to="/"></ButtonLink>
                <ButtonLink text="Habitaciones" backgroundColor="yellow" :to="'Habitaciones/' + this.id"></ButtonLink>
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