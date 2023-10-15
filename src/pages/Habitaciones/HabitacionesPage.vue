<template>
    <layautPage title="Habitaciones del
            hotel">
        <div class="px-8 pt-6 pb-8 mb-4 w-full">

            <div class="flex items-center justify-between mb-10">
                <div class="flex items-start justify-between flex-col">
                    <div class="flex items-center justify-between">
                        <img src="@/assets/logo.png" alt="hotel" class="w-16">
                        <h2 class="px-5 text-3xl font-bold">Hotel caribe</h2>
                    </div>
                    <p class="text-lg font-semibold">Habitaciones: <span>100</span></p>
                </div>
                <ButtonLink text="Crear habitaciones" backgroundColor="green"
                    :to="'/detallesHoteles/Habitaciones/CrearHabitacion/' + this.id"></ButtonLink>
            </div>
            <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
                <table class="w-full text-sm text-left bg-blue-600 text-gray-800 ">
                    <thead class="text-xs text-white uppercase ">
                        <tr>
                            <th scope="col" class="px-6 py-3">
                                Tipo
                            </th>
                            <th scope="col" class="px-6 py-3">
                                Acomodacion
                            </th>
                            <th scope="col" class="px-6 py-3">
                                Codigo
                            </th>
                            <th scope="col" class="px-6 py-3 text-center">
                                Opciones
                            </th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="border-b bg-blue-100 hover:bg-blue-200">
                            <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap">
                                JUNIOR
                            </th>
                            <td class="px-6 py-4">
                                TRIPLE
                            </td>
                            <td class="px-6 py-4">
                                10
                            </td>
                            <td class="px-6 py-4 flex items-center justify-center">
                                <IconLink id="1" routePrefix="detallesHoteles/Habitaciones/editar" iconClass="bi-pen"
                                    backgroundColor="bg-blue-500 hover:bg-blue-600"></IconLink>
                                <IconLink id="1" routePrefix="detallesHoteles/Habitaciones/eliminar" iconClass="bi-trash"
                                    backgroundColor="bg-red-500 hover:bg-red-600"></IconLink>
                            </td>
                        </tr>
                        <tr class="border-b bg-blue-100 hover:bg-blue-200">
                            <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap">
                                ESTANDAR
                            </th>
                            <td class="px-6 py-4">
                                SENCILLA
                            </td>
                            <td class="px-6 py-4">
                                20
                            </td>
                            <td class="px-6 py-4 flex items-center justify-center">
                                <IconLink id="1" routePrefix="detallesHoteles/Habitaciones/editar" iconClass="bi-pen"
                                    backgroundColor="bg-blue-500 hover:bg-blue-600"></IconLink>
                                <IconLink id="1" routePrefix="detallesHoteles/Habitaciones/eliminar" iconClass="bi-trash"
                                    backgroundColor="bg-red-500 hover:bg-red-600"></IconLink>
                            </td>
                        </tr>

                    </tbody>
                </table>
            </div>
            <div class="flex items-center justify-between mt-10">
                <ButtonLink text="Regresar" backgroundColor="blue" :to="'/detallesHoteles/' + this.id"></ButtonLink>
            </div>
        </div>

    </layautPage>
</template>
<script>
import LayautPage from "@/components/LayautPage.vue";
import ButtonLink from "@/components/ButtonLink.vue";
import IconLink from "@/components/IconLink.vue";
export default {
    components: {
        LayautPage,
        ButtonLink,
        IconLink
    },
    data() {
        return {
            id: this.$route.params.id
        }
    },
}
</script>