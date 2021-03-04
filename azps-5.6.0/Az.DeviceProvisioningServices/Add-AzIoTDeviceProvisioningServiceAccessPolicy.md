---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f34816ca77955c86f68b421efa221eab57e552cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916740"
---
# <span data-ttu-id="1f258-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1f258-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="1f258-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f258-102">SYNOPSIS</span></span>
<span data-ttu-id="1f258-103">在 Azure IoT Hub 裝置設置服務中新增共用存取策略。</span><span class="sxs-lookup"><span data-stu-id="1f258-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1f258-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f258-104">SYNTAX</span></span>

### <span data-ttu-id="1f258-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f258-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f258-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f258-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f258-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f258-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f258-108">描述</span><span class="sxs-lookup"><span data-stu-id="1f258-108">DESCRIPTION</span></span>
<span data-ttu-id="1f258-109">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="1f258-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1f258-110">例子</span><span class="sxs-lookup"><span data-stu-id="1f258-110">EXAMPLES</span></span>

### <span data-ttu-id="1f258-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f258-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="1f258-112">在 Azure IoT Hub 裝置設置服務中使用 EnrollmentWrite 與 ServiceConfig 許可權，新增新的共用存取原則。</span><span class="sxs-lookup"><span data-stu-id="1f258-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="1f258-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="1f258-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="1f258-114">在 Azure IoT Hub 裝置設置服務中新增新的共用存取策略，並向右加上 EnrollmentRead。</span><span class="sxs-lookup"><span data-stu-id="1f258-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="1f258-115">參數</span><span class="sxs-lookup"><span data-stu-id="1f258-115">PARAMETERS</span></span>

### <span data-ttu-id="1f258-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f258-116">-DefaultProfile</span></span>
<span data-ttu-id="1f258-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f258-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f258-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1f258-118">-DpsObject</span></span>
<span data-ttu-id="1f258-119">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="1f258-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1f258-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1f258-120">-KeyName</span></span>
<span data-ttu-id="1f258-121">IoT 裝置設置服務存取策略金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="1f258-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="1f258-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f258-122">-Name</span></span>
<span data-ttu-id="1f258-123">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="1f258-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1f258-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="1f258-124">-Permissions</span></span>
<span data-ttu-id="1f258-125">IoT 裝置設置服務存取策略許可權</span><span class="sxs-lookup"><span data-stu-id="1f258-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="1f258-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f258-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f258-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="1f258-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1f258-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f258-128">-ResourceId</span></span>
<span data-ttu-id="1f258-129">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1f258-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1f258-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1f258-130">-Confirm</span></span>
<span data-ttu-id="1f258-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f258-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f258-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f258-132">-WhatIf</span></span>
<span data-ttu-id="1f258-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f258-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f258-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f258-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f258-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f258-135">CommonParameters</span></span>
<span data-ttu-id="1f258-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f258-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f258-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1f258-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f258-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1f258-138">INPUTS</span></span>

### <span data-ttu-id="1f258-139">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1f258-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1f258-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1f258-140">System.String</span></span>

## <span data-ttu-id="1f258-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1f258-141">OUTPUTS</span></span>

### <span data-ttu-id="1f258-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="1f258-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="1f258-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1f258-143">NOTES</span></span>

## <span data-ttu-id="1f258-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f258-144">RELATED LINKS</span></span>
