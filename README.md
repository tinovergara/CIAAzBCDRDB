## Antes de iniciar el Cloud-in-Action

Duration: 60 minutes

### Tarea 1: Despliega el entorno on-premises

1.Despliega la plantilla **SmartHotelHost.json** a un nuevo grupo de recursos. Esta plantilla implementa una máquina virtual que ejecuta Hyper-V anidado, con 4 máquinas virtuales anidadas. Esto comprende el entorno "local" que evaluarás y migrarás durante este laboratorio.

    Puedes implementar la plantilla seleccionando el botón "Deploy to Azure" que aparece a continuación. Deberás crear un nuevo grupo de recursos. El nombre del grupo de recursos sugerido para usar es **SmartHotelHostRG**. También deberás seleccionar una ubicación cercana a ti para implementar la plantilla. Luego, seleccions **Revisar + crear** seguido de **Crear**.
    
    <a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fcloudworkshop.blob.core.windows.net%2Fline-of-business-application-migration%2Fsept-2020%2FSmartHotelHost.json" target="_blank">![Button to deploy the SmartHotelHost template to Azure.](images/BeforeTheHOL/deploy-to-azure.png "Deploy the SmartHotelHost template to Azure")</a>

    > **Note:** The template will take around 6-7 minutes to deploy. Once template deployment is complete, several additional scripts are executed to bootstrap the lab environment. **Allow at least 1 hour from the start of template deployment for the scripts to run.**

### Task 2: Verify the on-premises environment

1. Navigate to the **SmartHotelHost** VM that was deployed by the template in the previous step.

2. Make a note of the public IP address.

3. Open a browser tab and navigate to **http://\<SmartHotelHostIP-Address\>**. You should see the SmartHotel application, which is running on nested VMs within Hyper-V on the SmartHotelHost. (The application doesn't do much: you can refresh the page to see the list of guests or select 'CheckIn' or 'CheckOut' to toggle their status.)

    ![Browser screenshot showing the SmartHotel application.](images/BeforeTheHOL/smarthotel.png)

    > **Note:** If the SmartHotel application is not shown, wait 10 minutes and try again. It takes **at least 1 hour** from the start of template deployment. You can also check the CPU, network and disk activity levels for the SmartHotelHost VM in the Azure portal, to see if the provisioning is still active.

You should follow all steps provided *before* performing the Hands-on lab.
