---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436545"
---
# <span data-ttu-id="87aea-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87aea-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="87aea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87aea-102">SYNOPSIS</span></span>
<span data-ttu-id="87aea-103">更新 Azure IoT 中樞裝置置備服務中的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="87aea-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="87aea-104">句法</span><span class="sxs-lookup"><span data-stu-id="87aea-104">SYNTAX</span></span>

### <span data-ttu-id="87aea-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="87aea-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87aea-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87aea-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87aea-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="87aea-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87aea-108">說明</span><span class="sxs-lookup"><span data-stu-id="87aea-108">DESCRIPTION</span></span>
<span data-ttu-id="87aea-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="87aea-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="87aea-110">示例</span><span class="sxs-lookup"><span data-stu-id="87aea-110">EXAMPLES</span></span>

### <span data-ttu-id="87aea-111">範例1</span><span class="sxs-lookup"><span data-stu-id="87aea-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="87aea-112">在 Azure IoT 中樞裝置中使用 EnrollmentWrite 許可權更新存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="87aea-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="87aea-113">範例1</span><span class="sxs-lookup"><span data-stu-id="87aea-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="87aea-114">在 Azure IoT 中樞裝置的 [mypolicy] 中更新存取原則「」使用管線直接 EnrollmentWrite。</span><span class="sxs-lookup"><span data-stu-id="87aea-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="87aea-115">參數</span><span class="sxs-lookup"><span data-stu-id="87aea-115">PARAMETERS</span></span>

### <span data-ttu-id="87aea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87aea-116">-DefaultProfile</span></span>
<span data-ttu-id="87aea-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87aea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87aea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87aea-118">-InputObject</span></span>
<span data-ttu-id="87aea-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="87aea-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="87aea-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="87aea-120">-KeyName</span></span>
<span data-ttu-id="87aea-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="87aea-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="87aea-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="87aea-122">-Name</span></span>
<span data-ttu-id="87aea-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="87aea-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="87aea-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="87aea-124">-Permissions</span></span>
<span data-ttu-id="87aea-125">IoT 裝置提供服務存取原則許可權</span><span class="sxs-lookup"><span data-stu-id="87aea-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="87aea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87aea-126">-ResourceGroupName</span></span>
<span data-ttu-id="87aea-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="87aea-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87aea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87aea-128">-ResourceId</span></span>
<span data-ttu-id="87aea-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="87aea-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="87aea-130">-確認</span><span class="sxs-lookup"><span data-stu-id="87aea-130">-Confirm</span></span>
<span data-ttu-id="87aea-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87aea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87aea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87aea-132">-WhatIf</span></span>
<span data-ttu-id="87aea-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87aea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87aea-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87aea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87aea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87aea-135">CommonParameters</span></span>
<span data-ttu-id="87aea-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87aea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87aea-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87aea-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87aea-138">輸入</span><span class="sxs-lookup"><span data-stu-id="87aea-138">INPUTS</span></span>

### <span data-ttu-id="87aea-139">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="87aea-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="87aea-140">System.object</span><span class="sxs-lookup"><span data-stu-id="87aea-140">System.String</span></span>

## <span data-ttu-id="87aea-141">輸出</span><span class="sxs-lookup"><span data-stu-id="87aea-141">OUTPUTS</span></span>

### <span data-ttu-id="87aea-142">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="87aea-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="87aea-143">筆記</span><span class="sxs-lookup"><span data-stu-id="87aea-143">NOTES</span></span>

## <span data-ttu-id="87aea-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="87aea-144">RELATED LINKS</span></span>
