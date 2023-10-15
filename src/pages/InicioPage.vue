<template>
    <LayautPage2 title="Listado general
            de hoteles">
            <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
                <table class="w-full text-sm text-left bg-blue-600 text-gray-800 ">
                    <thead class="text-xs text-white uppercase ">
                        <tr>
                            <th scope="col" class="px-6 py-3">
                                NIT
                            </th>
                            <th scope="col" class="px-6 py-3">
                                Nombre
                            </th>
                            <th scope="col" class="px-6 py-3">
                                Ciudad
                            </th>
                            <th scope="col" class="px-6 py-3">
                                Direccion
                            </th>
                            <th scope="col" class="px-6 py-3 text-center">
                                N° max de habitaciones
                            </th>
                            <th scope="col" class="px-6 py-3 text-center">
                                Opciones
                            </th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="border-b bg-blue-100 hover:bg-blue-200">
                            <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap">
                                123456789-0
                            </th>
                            <td class="px-6 py-4">
                                Hotel caribe
                            </td>
                            <td class="px-6 py-4">
                                Barranquilla
                            </td>
                            <td class="px-6 py-4">
                                Cr 10 #2-11
                            </td>
                            <td class="px-6 py-4 text-center">
                                100
                            </td>
                            <td class="px-6 py-4 flex items-center justify-center">
                                <IconLink id="1" routePrefix="detallesHoteles" iconClass="bi-file-earmark-text" backgroundColor="bg-yellow-500 hover:bg-yellow-600"></IconLink>
                                <IconLink id="1" routePrefix="editarHotel" iconClass="bi-pen" backgroundColor="bg-blue-500 hover:bg-blue-600"></IconLink>
                                <IconLink id="1" routePrefix="eliminar" iconClass="bi-trash" backgroundColor="bg-red-500 hover:bg-red-600"></IconLink>
                                <IconLink id="1" routePrefix="informe" iconClass="bi-bar-chart-line-fill" backgroundColor="bg-green-500 hover:bg-green-600"></IconLink>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
    </LayautPage2>
</template>
<script>
import LayautPage2  from "@/components/LayautPage2.vue";
import IconLink  from "@/components/IconLink.vue";

export default{
    components:{
        LayautPage2,
        IconLink,
    }
}
</script>