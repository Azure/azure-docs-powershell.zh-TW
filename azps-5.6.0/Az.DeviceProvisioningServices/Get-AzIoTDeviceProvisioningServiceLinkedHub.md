---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 5aff957c16fa6fefb52706f70016092a37cdcb3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909033"
---
# <span data-ttu-id="5a357-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5a357-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5a357-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a357-102">SYNOPSIS</span></span>
<span data-ttu-id="5a357-103">列出 Azure IoT 中心裝置設置服務中連結 IoT 中樞的所有或顯示詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5a357-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5a357-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a357-104">SYNTAX</span></span>

### <span data-ttu-id="5a357-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5a357-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a357-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a357-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a357-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5a357-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a357-108">描述</span><span class="sxs-lookup"><span data-stu-id="5a357-108">DESCRIPTION</span></span>
<span data-ttu-id="5a357-109">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="5a357-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5a357-110">例子</span><span class="sxs-lookup"><span data-stu-id="5a357-110">EXAMPLES</span></span>

### <span data-ttu-id="5a357-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a357-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="5a357-112">在「myiotdps」中列出所有連結的 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="5a357-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="5a357-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="5a357-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="5a357-114">顯示 Azure IoT 中心裝置布布服務中連結 IoT 中樞 「myiothub1」的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5a357-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5a357-115">參數</span><span class="sxs-lookup"><span data-stu-id="5a357-115">PARAMETERS</span></span>

### <span data-ttu-id="5a357-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a357-116">-DefaultProfile</span></span>
<span data-ttu-id="5a357-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a357-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a357-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5a357-118">-DpsObject</span></span>
<span data-ttu-id="5a357-119">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="5a357-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a357-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5a357-120">-LinkedHubName</span></span>
<span data-ttu-id="5a357-121">連結 IoT 中樞的主機名稱稱</span><span class="sxs-lookup"><span data-stu-id="5a357-121">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a357-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a357-122">-Name</span></span>
<span data-ttu-id="5a357-123">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="5a357-123">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a357-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a357-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a357-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="5a357-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a357-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a357-126">-ResourceId</span></span>
<span data-ttu-id="5a357-127">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5a357-127">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a357-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a357-128">CommonParameters</span></span>
<span data-ttu-id="5a357-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a357-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a357-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5a357-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a357-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5a357-131">INPUTS</span></span>

### <span data-ttu-id="5a357-132">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5a357-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5a357-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5a357-133">System.String</span></span>

## <span data-ttu-id="5a357-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5a357-134">OUTPUTS</span></span>

### <span data-ttu-id="5a357-135">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5a357-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5a357-136">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="5a357-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="5a357-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5a357-137">NOTES</span></span>

## <span data-ttu-id="5a357-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a357-138">RELATED LINKS</span></span>
