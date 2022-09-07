# Creacion-de-VM-con-CLI-Azure
Creación de una máquina virtual de azure con Cloudshell - CLI

Iniciamos sesión en portal.azure.com
![image](https://user-images.githubusercontent.com/106035353/188752947-e5f596ba-ac84-4a5b-bfac-d9aed39c8290.png)


Hacemos click en Cloudshell:

![image](https://user-images.githubusercontent.com/106035353/188753063-950b6b84-9fe7-451e-b635-3ca9be76cfa5.png)


Elegimos consola:bash :

![image](https://user-images.githubusercontent.com/106035353/188753150-a2a3b7c9-06e8-47c1-8a31-f00d906ec72f.png)

Hacemos click en mostrar configuración avanzada

![image](https://user-images.githubusercontent.com/106035353/188753479-a3cae2d4-eb81-4a8d-8302-28d977c766ab.png)


Hacemos click en mostrar configuración avanzada

![image](https://user-images.githubusercontent.com/106035353/188753569-bf01962e-ba97-4ce5-9ce8-6b830c9cde51.png)


Escribimos los siguientes datos:
El nombre del grupo de recursos: “lab15” (ejemplo)

El nombre de la cuenta de almacenamiento en crear nuevo: “almacenamientoclouds1”

Recurso compartido de archivo: “recursocompartidocloudshell”

Elegimos la Región de Cloudshell: “Este de EEUU”

![image](https://user-images.githubusercontent.com/106035353/188753668-75f85722-785c-4266-8637-bd99f4bea487.png)


*Hacemos clic en Crear almacenamiento

En el shell escribimos el comando:

az	-> nos muestra los distintos comandos

![image](https://user-images.githubusercontent.com/106035353/188753763-c1038db5-300f-498b-97f4-94f8e0ee9afb.png)

(Para limpiar el shell escribimos el comando “clear”)

![image](https://user-images.githubusercontent.com/106035353/188757228-f9c3b3b0-32fe-4874-a178-29fcf4f92fc8.png)


Escribimos el comando:
az group list - - output table 
(Para mostrar la lista de grupo de recursos)

![image](https://user-images.githubusercontent.com/106035353/188757280-004ade83-eabe-4bad-ac43-1e775d71fc96.png)


Para crear una VM escribimos los siguientes comandos con los datos:

az vm create \
- - name myVMCLI \
- - resource-group lab15 \
- - image UbuntuLTS \
- - location EastUS \
- - admin-username azureuser \
- - admin-password Pa$$w0rd1234

![image](https://user-images.githubusercontent.com/106035353/188757527-1b4f350b-f0d1-4e9e-b0fd-bcc87d355117.png)


Podemos apreciar los recursos creados en el panel:

![image](https://user-images.githubusercontent.com/106035353/188757592-fb71d262-2035-4cb7-9b2b-fdf4bc2338bd.png)


Para recuperar información sobre la VM escribimos el comando:

az vm show - - resource-group lab15 - - name myVMCLI - - show-details - - output table

![image](https://user-images.githubusercontent.com/106035353/188757645-d008fb41-ba53-495e-8085-351ddd4585a6.png)


Para detener la VM escribimos:

az vm stop - - resource - group lab15 - - name myVMCLI

![image](https://user-images.githubusercontent.com/106035353/188757704-601fda82-3dae-4f4e-9ab2-f2e06811d90b.png)


Comprobar estado VM:

az vm show - - resource-group lab15 - - name myVMCLI - - showdetails - - output table

![image](https://user-images.githubusercontent.com/106035353/188758284-6c0cc957-f228-4d9b-8840-51b7a61d8ba6.png)


Para mostrar todos los comandos de los recursos:
az help

![image](https://user-images.githubusercontent.com/106035353/188758337-d8534f21-2a49-4430-859b-f5382f2aebde.png)


Por último eliminamos el grupo de recursos por cuestión de limpieza y para evitar costos:

![image](https://user-images.githubusercontent.com/106035353/188758427-9b567637-417b-4539-be63-dfa62c65be65.png)




