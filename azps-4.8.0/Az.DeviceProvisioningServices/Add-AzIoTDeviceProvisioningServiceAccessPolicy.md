---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969753"
---
# <span data-ttu-id="d6481-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d6481-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d6481-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6481-102">SYNOPSIS</span></span>
<span data-ttu-id="d6481-103">在 Azure IoT 中樞裝置預配服務中新增新的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="d6481-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d6481-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6481-104">SYNTAX</span></span>

### <span data-ttu-id="d6481-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6481-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6481-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6481-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6481-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6481-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6481-108">說明</span><span class="sxs-lookup"><span data-stu-id="d6481-108">DESCRIPTION</span></span>
<span data-ttu-id="d6481-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="d6481-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d6481-110">示例</span><span class="sxs-lookup"><span data-stu-id="d6481-110">EXAMPLES</span></span>

### <span data-ttu-id="d6481-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d6481-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="d6481-112">在具備 EnrollmentWrite 和 ServiceConfig 許可權的 Azure IoT 中樞裝置預配服務中新增新的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="d6481-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="d6481-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d6481-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="d6481-114">在具備 EnrollmentRead 許可權的 Azure IoT 中樞裝置預配服務中新增新的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="d6481-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="d6481-115">參數</span><span class="sxs-lookup"><span data-stu-id="d6481-115">PARAMETERS</span></span>

### <span data-ttu-id="d6481-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6481-116">-DefaultProfile</span></span>
<span data-ttu-id="d6481-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6481-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6481-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d6481-118">-DpsObject</span></span>
<span data-ttu-id="d6481-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="d6481-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d6481-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d6481-120">-KeyName</span></span>
<span data-ttu-id="d6481-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="d6481-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="d6481-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6481-122">-Name</span></span>
<span data-ttu-id="d6481-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="d6481-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d6481-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="d6481-124">-Permissions</span></span>
<span data-ttu-id="d6481-125">IoT 裝置提供服務存取原則許可權</span><span class="sxs-lookup"><span data-stu-id="d6481-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="d6481-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6481-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6481-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d6481-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d6481-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6481-128">-ResourceId</span></span>
<span data-ttu-id="d6481-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d6481-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d6481-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d6481-130">-Confirm</span></span>
<span data-ttu-id="d6481-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6481-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6481-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6481-132">-WhatIf</span></span>
<span data-ttu-id="d6481-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6481-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6481-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6481-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6481-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6481-135">CommonParameters</span></span>
<span data-ttu-id="d6481-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6481-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6481-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6481-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6481-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d6481-138">INPUTS</span></span>

### <span data-ttu-id="d6481-139">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="d6481-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d6481-140">System.object</span><span class="sxs-lookup"><span data-stu-id="d6481-140">System.String</span></span>

## <span data-ttu-id="d6481-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d6481-141">OUTPUTS</span></span>

### <span data-ttu-id="d6481-142">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="d6481-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="d6481-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d6481-143">NOTES</span></span>

## <span data-ttu-id="d6481-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6481-144">RELATED LINKS</span></span>