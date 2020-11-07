---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f5d750dc795619f32f6c4f16a5fe1e3b5e111106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626106"
---
# <span data-ttu-id="64e5a-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64e5a-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="64e5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="64e5a-103">更新 Azure IoT 中樞裝置置備服務中的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="64e5a-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64e5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="64e5a-104">SYNTAX</span></span>

### <span data-ttu-id="64e5a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="64e5a-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64e5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="64e5a-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="64e5a-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64e5a-108">說明</span><span class="sxs-lookup"><span data-stu-id="64e5a-108">DESCRIPTION</span></span>
<span data-ttu-id="64e5a-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="64e5a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="64e5a-110">示例</span><span class="sxs-lookup"><span data-stu-id="64e5a-110">EXAMPLES</span></span>

### <span data-ttu-id="64e5a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="64e5a-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="64e5a-112">在 Azure IoT 中樞裝置中使用 EnrollmentWrite 許可權更新存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="64e5a-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="64e5a-113">範例1</span><span class="sxs-lookup"><span data-stu-id="64e5a-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzureRmIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="64e5a-114">在 Azure IoT 中樞裝置的 [mypolicy] 中更新存取原則「」使用管線直接 EnrollmentWrite。</span><span class="sxs-lookup"><span data-stu-id="64e5a-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="64e5a-115">參數</span><span class="sxs-lookup"><span data-stu-id="64e5a-115">PARAMETERS</span></span>

### <span data-ttu-id="64e5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e5a-116">-DefaultProfile</span></span>
<span data-ttu-id="64e5a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64e5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64e5a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64e5a-118">-InputObject</span></span>
<span data-ttu-id="64e5a-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="64e5a-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64e5a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="64e5a-120">-KeyName</span></span>
<span data-ttu-id="64e5a-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="64e5a-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64e5a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="64e5a-122">-Name</span></span>
<span data-ttu-id="64e5a-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="64e5a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="64e5a-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="64e5a-124">-Permissions</span></span>
<span data-ttu-id="64e5a-125">IoT 裝置提供服務存取原則許可權</span><span class="sxs-lookup"><span data-stu-id="64e5a-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="64e5a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64e5a-126">-ResourceGroupName</span></span>
<span data-ttu-id="64e5a-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="64e5a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="64e5a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64e5a-128">-ResourceId</span></span>
<span data-ttu-id="64e5a-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="64e5a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="64e5a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="64e5a-130">-Confirm</span></span>
<span data-ttu-id="64e5a-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64e5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64e5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e5a-132">-WhatIf</span></span>
<span data-ttu-id="64e5a-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64e5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e5a-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64e5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64e5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e5a-135">CommonParameters</span></span>
<span data-ttu-id="64e5a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64e5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e5a-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64e5a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e5a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="64e5a-138">INPUTS</span></span>

### <span data-ttu-id="64e5a-139">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="64e5a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="64e5a-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="64e5a-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="64e5a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="64e5a-141">System.String</span></span>

## <span data-ttu-id="64e5a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="64e5a-142">OUTPUTS</span></span>

### <span data-ttu-id="64e5a-143">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="64e5a-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="64e5a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="64e5a-144">NOTES</span></span>

## <span data-ttu-id="64e5a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="64e5a-145">RELATED LINKS</span></span>
