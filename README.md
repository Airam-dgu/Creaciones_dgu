#1:TABLA 1: Presupuesto de Venta
#PRODUCTO R- 1 SEMESTRE
pR_1S_UV=6000  #Unidades a vender Producto R Primer Semestre
pR_1S_PV= 500  #Precio de Venta Producto R Primer Semestre
importventa_PR_1S= (pR_1S_UV * pR_1S_PV)

#PRODUCTO R- 2 SEMESTRE
pR_2S_UV=4000  #Unidades a vender Producto R Primer Semestre
pR_2S_PV= 520  #Precio de Venta Producto R Primer Semestre
importventa_PR_2S= (pR_2S_UV * pR_2S_PV)


#TOTAL AÑO PRODUCTO R
totalPR_Año=(importventa_PR_1S + importventa_PR_2S)



from tabulate import tabulate 
print("\033[1mPRESUPUESTO DE OPERACION\033[0m")
print(" ")

print("\033[4mPresupuesto de venta\033[0m")
print("")
matriz1 = [[ "Unidades a vender"   , pR_1S_UV, pR_2S_UV, ""]]
matriz2 = [[ "Precio de venta"   , pR_1S_PV, pR_2S_PV, ""]]
matriz3 =[[ ("\033[1mImporte de venta\033[0m")   , importventa_PR_1S,importventa_PR_2S, totalPR_Año]]
print(tabulate(matriz1,headers=['\033[1;35mPRODUCTO R\033[0m', '1er Semestre', '2do Semestre', 'Total Año']))
print(tabulate(matriz2,headers=['              ', '            ', '              ', ]))
print(tabulate(matriz3,headers=['             ', '            ', '              ',   ]))
print(" ")
#-------------------------------------------------------------------------------------
#PRODUCTO S- 1 SEMESTRE
pS_1S_UV=4000 #Unidades a vender Producto S Primer Semestre
pS_1S_PV= 400  #Precio de Venta Producto S Primer Semestre
importventa_PS_1S= (pS_1S_UV * pS_1S_PV)

#PRODUCTO S- 2 SEMESTRE
pS_2S_UV=3000  #Unidades a vender Producto S Primer Semestre
pS_2S_PV= 420  #Precio de Venta Producto S Primer Semestre
importventa_PS_2S= (pS_2S_UV * pS_2S_PV)


#TOTAL AÑO PRODUCTO S
totalPS_Año=(importventa_PS_1S + importventa_PS_2S)


from tabulate import tabulate 
matriz1 = [[ "Unidades a vender"   , pS_1S_UV, pS_2S_UV, ""]]
matriz2 = [[ "Precio de venta"   , pS_1S_PV, pS_2S_PV, ""]]
matriz3 =[[ ("\033[1mImporte de venta\033[0m")   , importventa_PS_1S,importventa_PS_2S, totalPS_Año]]
print(tabulate(matriz1,headers=['\033[1;32mPRODUCTO S\033[0m', '1er Semestre', '2do Semestre', 'Total Año']))
print(tabulate(matriz2,headers=['              ', '            ', '              ', ]))
print(tabulate(matriz3,headers=['             ', '            ', '              ',   ]))
print(" ")
#-------------------------------------------------------------------------------------
#PRODUCTO P- 1 SEMESTRE
pP_1S_UV=3000 #Unidades a vender Producto P Primer Semestre
pP_1S_PV= 550  #Precio de Venta Producto P Primer Semestre
importventa_PP_1S= (pP_1S_UV * pP_1S_PV)

#PRODUCTO S- 2 SEMESTRE
pP_2S_UV=2000  #Unidades a vender Producto P Primer Semestre
pP_2S_PV= 560  #Precio de Venta Producto P Primer Semestre
importventa_PP_2S= (pP_2S_UV * pP_2S_PV)


#TOTAL AÑO PRODUCTO P
totalPP_Año=(importventa_PP_1S + importventa_PP_2S)




from tabulate import tabulate 
matriz1 = [[ "Unidades a vender"   , pP_1S_UV, pP_2S_UV, ""]]
matriz2 = [[ "Precio de venta"   , pP_1S_PV, pP_2S_PV, ""]]
matriz3 =[[ ("\033[1mImporte de venta\033[0m")   , importventa_PP_1S,importventa_PP_2S, totalPP_Año]]
print(" ")

print(tabulate(matriz1,headers=['\033[1;34mPRODUCTO P\033[0m', '1er Semestre', '2do Semestre', 'Total Año']))
print(tabulate(matriz2,headers=['              ', '            ', '              ', ]))
print(tabulate(matriz3,headers=['              ', '            ', '              ',   ]))
#____________________________________________________________________________________
#TOTAL VENTAS POR SEMESTRE
total_Vent_Sem=(totalPR_Año + totalPS_Año + totalPP_Año)
sum1ersem=(importventa_PR_1S+importventa_PS_1S+importventa_PP_1S)
sum2dosem=(importventa_PR_2S+importventa_PS_2S+importventa_PP_2S)

matriz3 =[[ ("\033[1;33mTotal de venta \n por semestre\033[0m")   , sum1ersem,sum2dosem,total_Vent_Sem]]
print(" ")

print(tabulate(matriz1,headers=['              ', '1er Semestre', '2do Semestre', 'Total Año']))
print(tabulate(matriz2,headers=['              ', '            ', '              ', ]))
print(tabulate(matriz3,headers=['              ', '            ', '              ',   ]))
print(" ")



#2:TABLA 2: Determinacion de saldo de clientes y flujo de entrada
saldo_clientes=80_000
ventas=10_710_000
tot_clientes=saldo_clientes+ventas

#entradas efectivo
porCobrar=140_000
porcen=90
porCobrarporc=ventas * porcen/100
totaentradas= porCobrar + porCobrarporc
saldoclientes2024=(tot_clientes-totaentradas )

print("\033[4mDeterminación del saldo de Clientes y Flujo de Entradas\033[0m")
print("")
matriz4= [[ "Saldo de clientes\n 31-Dic-2024","             ",saldo_clientes]]
matriz6= [[ "ventas___________"," ",   ventas]]
matriz7=[[ "Total de Clientes             ","             ",tot_clientes]]
matriz8=[["Entradas de efectivo           ","             ","           "]]
matriz9=[["Por Cobranza 2024              ", f"{porCobrar:,.0f}"            ""]]
matriz10=[["Por cobrar con  \nporcentaje     ",  f"{porCobrarporc:,.0f}"                 ""]]
matriz11=[["Total de entrada\n2024         ", "            ", f"{totaentradas:,.0f}"]]
matriz12=[[("\033[1;33mSaldo del\ncliente 2024 \033[0m"),"          ",f"{saldoclientes2024:,.0f}"]]

print(tabulate(matriz4,headers= ['     Importe',       'Total', ]))
print(tabulate(matriz6,headers= ['            ', '            ',  ]))
print(tabulate(matriz7,headers= ['            ', '            ',  ]))
print(tabulate(matriz9,headers= ['            ', '            ',  ]))
print(tabulate(matriz10,headers=['             ', '            ', ]))
print(tabulate(matriz11,headers=['             ', '            ', ]))
print(tabulate(matriz12,headers=['                ', '           ', ]))

print(" ")

#3:TABLA 3: Presupuesto de produccion
