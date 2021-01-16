---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278007"
---
# <span data-ttu-id="8c14c-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="8c14c-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="8c14c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c14c-102">SYNOPSIS</span></span>
<span data-ttu-id="8c14c-103">[全部清單] 或 [顯示 Azure IoT 中心裝置的詳細資料] 提供服務。</span><span class="sxs-lookup"><span data-stu-id="8c14c-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="8c14c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c14c-104">SYNTAX</span></span>

### <span data-ttu-id="8c14c-105">ListIotDpsByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="8c14c-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c14c-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="8c14c-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c14c-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c14c-107">DESCRIPTION</span></span>
<span data-ttu-id="8c14c-108">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="8c14c-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8c14c-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c14c-109">EXAMPLES</span></span>

### <span data-ttu-id="8c14c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8c14c-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="8c14c-111">列出訂閱中的所有 Azure IoT 中樞裝置配中服務。</span><span class="sxs-lookup"><span data-stu-id="8c14c-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="8c14c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8c14c-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="8c14c-113">列出資源群組 ' myresourcegroup」中的所有 Azure IoT 中樞裝置提供服務。</span><span class="sxs-lookup"><span data-stu-id="8c14c-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="8c14c-114">範例3</span><span class="sxs-lookup"><span data-stu-id="8c14c-114">Example 3</span></span>
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

<span data-ttu-id="8c14c-115">顯示 Azure IoT 中樞裝置預配服務 ' myiotdps」的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c14c-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="8c14c-116">參數</span><span class="sxs-lookup"><span data-stu-id="8c14c-116">PARAMETERS</span></span>

### <span data-ttu-id="8c14c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c14c-117">-DefaultProfile</span></span>
<span data-ttu-id="8c14c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c14c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c14c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c14c-119">-Name</span></span>
<span data-ttu-id="8c14c-120">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="8c14c-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8c14c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c14c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c14c-122">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="8c14c-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8c14c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c14c-123">CommonParameters</span></span>
<span data-ttu-id="8c14c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c14c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c14c-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c14c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c14c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8c14c-126">INPUTS</span></span>

### <span data-ttu-id="8c14c-127">所有</span><span class="sxs-lookup"><span data-stu-id="8c14c-127">None</span></span>

## <span data-ttu-id="8c14c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8c14c-128">OUTPUTS</span></span>

### <span data-ttu-id="8c14c-129">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="8c14c-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="8c14c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8c14c-130">NOTES</span></span>

## <span data-ttu-id="8c14c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c14c-131">RELATED LINKS</span></span>
