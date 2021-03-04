---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ee86af7862ad22b34e159f1d5097d5d30a4cba8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917762"
---
# <span data-ttu-id="3bd47-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3bd47-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3bd47-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3bd47-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd47-103">列出 Azure IoT Hub 裝置設置服務的所有或顯示詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bd47-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="3bd47-104">語法</span><span class="sxs-lookup"><span data-stu-id="3bd47-104">SYNTAX</span></span>

### <span data-ttu-id="3bd47-105">ListIotDpsByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="3bd47-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd47-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="3bd47-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bd47-107">描述</span><span class="sxs-lookup"><span data-stu-id="3bd47-107">DESCRIPTION</span></span>
<span data-ttu-id="3bd47-108">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="3bd47-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3bd47-109">例子</span><span class="sxs-lookup"><span data-stu-id="3bd47-109">EXAMPLES</span></span>

### <span data-ttu-id="3bd47-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3bd47-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="3bd47-111">列出訂閱中所有 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="3bd47-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="3bd47-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="3bd47-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="3bd47-113">列出資源群組 "myresourcegroup" 中所有 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="3bd47-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="3bd47-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="3bd47-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="3bd47-115">顯示 Azure IoT Hub 裝置設置服務 "myiotdps" 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3bd47-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="3bd47-116">參數</span><span class="sxs-lookup"><span data-stu-id="3bd47-116">PARAMETERS</span></span>

### <span data-ttu-id="3bd47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd47-117">-DefaultProfile</span></span>
<span data-ttu-id="3bd47-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bd47-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd47-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bd47-119">-Name</span></span>
<span data-ttu-id="3bd47-120">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="3bd47-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd47-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd47-121">-ResourceGroupName</span></span>
<span data-ttu-id="3bd47-122">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="3bd47-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd47-123">CommonParameters</span></span>
<span data-ttu-id="3bd47-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3bd47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd47-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3bd47-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd47-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3bd47-126">INPUTS</span></span>

### <span data-ttu-id="3bd47-127">沒有</span><span class="sxs-lookup"><span data-stu-id="3bd47-127">None</span></span>

## <span data-ttu-id="3bd47-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3bd47-128">OUTPUTS</span></span>

### <span data-ttu-id="3bd47-129">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3bd47-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="3bd47-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3bd47-130">NOTES</span></span>

## <span data-ttu-id="3bd47-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bd47-131">RELATED LINKS</span></span>
