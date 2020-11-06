---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 2da931326b9f900dbf3af3cfcb2e504b413cef33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612509"
---
# <span data-ttu-id="c0c90-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0c90-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="c0c90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0c90-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c90-103">更新 Azure IoT 中樞裝置置備服務中的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="c0c90-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c0c90-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0c90-104">SYNTAX</span></span>

### <span data-ttu-id="c0c90-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0c90-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0c90-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0c90-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c90-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c0c90-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c90-108">說明</span><span class="sxs-lookup"><span data-stu-id="c0c90-108">DESCRIPTION</span></span>
<span data-ttu-id="c0c90-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="c0c90-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c0c90-110">示例</span><span class="sxs-lookup"><span data-stu-id="c0c90-110">EXAMPLES</span></span>

### <span data-ttu-id="c0c90-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c0c90-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="c0c90-112">在 Azure IoT 中樞裝置中使用 EnrollmentWrite 許可權更新存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="c0c90-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="c0c90-113">範例1</span><span class="sxs-lookup"><span data-stu-id="c0c90-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="c0c90-114">在 Azure IoT 中樞裝置的 [mypolicy] 中更新存取原則「」使用管線直接 EnrollmentWrite。</span><span class="sxs-lookup"><span data-stu-id="c0c90-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="c0c90-115">參數</span><span class="sxs-lookup"><span data-stu-id="c0c90-115">PARAMETERS</span></span>

### <span data-ttu-id="c0c90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c90-116">-DefaultProfile</span></span>
<span data-ttu-id="c0c90-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0c90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c90-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0c90-118">-InputObject</span></span>
<span data-ttu-id="c0c90-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="c0c90-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c0c90-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c0c90-120">-KeyName</span></span>
<span data-ttu-id="c0c90-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="c0c90-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="c0c90-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0c90-122">-Name</span></span>
<span data-ttu-id="c0c90-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="c0c90-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c0c90-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="c0c90-124">-Permissions</span></span>
<span data-ttu-id="c0c90-125">IoT 裝置提供服務存取原則許可權</span><span class="sxs-lookup"><span data-stu-id="c0c90-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="c0c90-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c90-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0c90-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c0c90-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0c90-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0c90-128">-ResourceId</span></span>
<span data-ttu-id="c0c90-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c0c90-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c0c90-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c0c90-130">-Confirm</span></span>
<span data-ttu-id="c0c90-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0c90-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c90-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c90-132">-WhatIf</span></span>
<span data-ttu-id="c0c90-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0c90-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c90-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0c90-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c90-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c90-135">CommonParameters</span></span>
<span data-ttu-id="c0c90-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0c90-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c90-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0c90-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c90-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c0c90-138">INPUTS</span></span>

### <span data-ttu-id="c0c90-139">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="c0c90-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="c0c90-140">System.object</span><span class="sxs-lookup"><span data-stu-id="c0c90-140">System.String</span></span>

## <span data-ttu-id="c0c90-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c0c90-141">OUTPUTS</span></span>

### <span data-ttu-id="c0c90-142">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="c0c90-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="c0c90-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c0c90-143">NOTES</span></span>

## <span data-ttu-id="c0c90-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0c90-144">RELATED LINKS</span></span>
