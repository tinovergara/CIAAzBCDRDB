## Antes de iniciar el Cloud-in-Action

Duración: 60 minutos

### Tarea 1: Despliega el entorno on-premises

1. Despliega la plantilla **SmartHotelHost.json** a un nuevo grupo de recursos. Esta plantilla implementa una máquina virtual que ejecuta Hyper-V anidado, con 4 máquinas virtuales anidadas. Esto comprende el entorno "local" que evaluarás y migrarás durante este laboratorio.

    Puedes implementar la plantilla seleccionando el botón "Deploy to Azure" que aparece a continuación. Deberás crear un nuevo grupo de recursos. El nombre del grupo de recursos sugerido para usar es **SmartHotelHostRG**. También deberás seleccionar una ubicación cercana a ti para implementar la plantilla. Luego, seleccions **Revisar + crear** seguido de **Crear**.
    
    <a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fstoragetino.blob.core.windows.net%2Fsmarthotel%2FSmartHotelHost.json" target="_blank">![Button to deploy the SmartHotelHost template to Azure.](deploy-to-azure.png "Despliega la plantilla SmartHotelHost a Azure")</a>

    > **Nota:** La implementación de la plantilla demorará entre 6 y 7 minutos. Una vez que se completa la implementación de la plantilla, se ejecutan varios scripts adicionales para iniciar el entorno de laboratorio. **Espera al menos 1 hora desde el inicio de la implementación de la plantilla para que se ejecuten los scripts.**

### Tarea 2: Verifica el entorno on-premises

1. Navega hasta la máquina virtual **SmartHotelHost** que implementó la plantilla en el paso anterior.

2. Anota la dirección IP Pública.

3. Abre una pestaña de tu navegador y navega a **http://\<SmartHotelHostIP-Address\>**. Deberías ver la aplicación SmartHotel, que se ejecuta en máquinas virtuales anidadas dentro de Hyper-V en SmartHotelHost. (La aplicación no hace mucho: puedes actualizar la página para ver la lista de invitados o seleccionar 'CheckIn' o 'CheckOut' para alternar su estado.)

    ![Browser screenshot showing the SmartHotel application.](smarthotel.png)

    > **Nota:** Si no se muestra la aplicación SmartHotel, espera 10 minutos y vuelve a intentarlo. Requiere **al menos 1 hora** desde el inicio de la implementación de la plantilla. También puedes comprobar los niveles de actividad de CPU, red y disco de la máquina virtual SmartHotelHost en el portal de Azure para ver si el aprovisionamiento sigue activo.

Debes seguir todos los pasos proporcionados *antes* de realizar el laboratorio práctico.
