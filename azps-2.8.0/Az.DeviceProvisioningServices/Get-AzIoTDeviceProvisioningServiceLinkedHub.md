---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ec7f6e6bd402086084bee387be6a0563a6bf0c5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612526"
---
# <span data-ttu-id="b1db0-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="b1db0-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="b1db0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1db0-102">SYNOPSIS</span></span>
<span data-ttu-id="b1db0-103">[全部清單] 或 [顯示 Azure IoT 中心設備提供服務中連結的 IoT 中心] 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b1db0-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b1db0-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1db0-104">SYNTAX</span></span>

### <span data-ttu-id="b1db0-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1db0-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1db0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1db0-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1db0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1db0-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1db0-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1db0-108">DESCRIPTION</span></span>
<span data-ttu-id="b1db0-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="b1db0-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b1db0-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1db0-110">EXAMPLES</span></span>

### <span data-ttu-id="b1db0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b1db0-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="b1db0-112">在 "myiotdps" 中列出所有連結的 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="b1db0-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="b1db0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b1db0-113">Example 2</span></span>
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

<span data-ttu-id="b1db0-114">顯示 Azure IoT 中樞裝置提供服務中連結 IoT 中樞「myiothub1」的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b1db0-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b1db0-115">參數</span><span class="sxs-lookup"><span data-stu-id="b1db0-115">PARAMETERS</span></span>

### <span data-ttu-id="b1db0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1db0-116">-DefaultProfile</span></span>
<span data-ttu-id="b1db0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1db0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1db0-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="b1db0-118">-DpsObject</span></span>
<span data-ttu-id="b1db0-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="b1db0-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b1db0-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="b1db0-120">-LinkedHubName</span></span>
<span data-ttu-id="b1db0-121">連結 IoT 中樞的主機名稱</span><span class="sxs-lookup"><span data-stu-id="b1db0-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="b1db0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1db0-122">-Name</span></span>
<span data-ttu-id="b1db0-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="b1db0-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b1db0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1db0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1db0-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b1db0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b1db0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1db0-126">-ResourceId</span></span>
<span data-ttu-id="b1db0-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b1db0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b1db0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1db0-128">CommonParameters</span></span>
<span data-ttu-id="b1db0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1db0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1db0-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1db0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1db0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b1db0-131">INPUTS</span></span>

### <span data-ttu-id="b1db0-132">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="b1db0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b1db0-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b1db0-133">System.String</span></span>

## <span data-ttu-id="b1db0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b1db0-134">OUTPUTS</span></span>

### <span data-ttu-id="b1db0-135">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="b1db0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="b1db0-136">PSIotHubDefinitions （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="b1db0-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="b1db0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b1db0-137">NOTES</span></span>

## <span data-ttu-id="b1db0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1db0-138">RELATED LINKS</span></span>
