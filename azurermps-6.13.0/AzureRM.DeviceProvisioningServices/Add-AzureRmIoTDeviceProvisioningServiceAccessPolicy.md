---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 23d9e40fe6d25fbd2a6bb3e23959d1a4bf087af2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453764"
---
# <span data-ttu-id="4ee3b-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4ee3b-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="4ee3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ee3b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee3b-103">在 Azure IoT 中樞裝置預配服務中新增新的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ee3b-104">SYNTAX</span></span>

### <span data-ttu-id="4ee3b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4ee3b-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ee3b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ee3b-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ee3b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ee3b-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee3b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4ee3b-108">DESCRIPTION</span></span>
<span data-ttu-id="4ee3b-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4ee3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="4ee3b-110">EXAMPLES</span></span>

### <span data-ttu-id="4ee3b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4ee3b-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="4ee3b-112">在具備 EnrollmentWrite 和 ServiceConfig 許可權的 Azure IoT 中樞裝置預配服務中新增新的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="4ee3b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4ee3b-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="4ee3b-114">在具備 EnrollmentRead 許可權的 Azure IoT 中樞裝置預配服務中新增新的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="4ee3b-115">參數</span><span class="sxs-lookup"><span data-stu-id="4ee3b-115">PARAMETERS</span></span>

### <span data-ttu-id="4ee3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee3b-116">-DefaultProfile</span></span>
<span data-ttu-id="4ee3b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee3b-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4ee3b-118">-DpsObject</span></span>
<span data-ttu-id="4ee3b-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="4ee3b-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4ee3b-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4ee3b-120">-KeyName</span></span>
<span data-ttu-id="4ee3b-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="4ee3b-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee3b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ee3b-122">-Name</span></span>
<span data-ttu-id="4ee3b-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="4ee3b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4ee3b-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="4ee3b-124">-Permissions</span></span>
<span data-ttu-id="4ee3b-125">IoT 裝置提供服務存取原則許可權</span><span class="sxs-lookup"><span data-stu-id="4ee3b-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee3b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee3b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ee3b-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="4ee3b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ee3b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ee3b-128">-ResourceId</span></span>
<span data-ttu-id="4ee3b-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4ee3b-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4ee3b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="4ee3b-130">-Confirm</span></span>
<span data-ttu-id="4ee3b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee3b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee3b-132">-WhatIf</span></span>
<span data-ttu-id="4ee3b-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee3b-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee3b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee3b-135">CommonParameters</span></span>
<span data-ttu-id="4ee3b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee3b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee3b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4ee3b-138">INPUTS</span></span>

### <span data-ttu-id="4ee3b-139">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="4ee3b-140">參數： DpsObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4ee3b-140">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="4ee3b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4ee3b-141">System.String</span></span>

## <span data-ttu-id="4ee3b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4ee3b-142">OUTPUTS</span></span>

### <span data-ttu-id="4ee3b-143">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="4ee3b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4ee3b-144">NOTES</span></span>

## <span data-ttu-id="4ee3b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ee3b-145">RELATED LINKS</span></span>
