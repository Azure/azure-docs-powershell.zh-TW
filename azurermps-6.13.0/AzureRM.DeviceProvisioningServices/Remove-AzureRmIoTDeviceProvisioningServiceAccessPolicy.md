---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451183"
---
# <span data-ttu-id="ec21a-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ec21a-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="ec21a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec21a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec21a-103">刪除 Azure IoT 中樞裝置置備服務中的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="ec21a-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec21a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec21a-104">SYNTAX</span></span>

### <span data-ttu-id="ec21a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec21a-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec21a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ec21a-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec21a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ec21a-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec21a-108">說明</span><span class="sxs-lookup"><span data-stu-id="ec21a-108">DESCRIPTION</span></span>
<span data-ttu-id="ec21a-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="ec21a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ec21a-110">示例</span><span class="sxs-lookup"><span data-stu-id="ec21a-110">EXAMPLES</span></span>

### <span data-ttu-id="ec21a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ec21a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="ec21a-112">在 Azure IoT 中樞裝置提供服務中刪除共用的存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="ec21a-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="ec21a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ec21a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="ec21a-114">在 Azure IoT 中樞裝置中使用管線來刪除共用的存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="ec21a-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="ec21a-115">參數</span><span class="sxs-lookup"><span data-stu-id="ec21a-115">PARAMETERS</span></span>

### <span data-ttu-id="ec21a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec21a-116">-DefaultProfile</span></span>
<span data-ttu-id="ec21a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec21a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec21a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec21a-118">-InputObject</span></span>
<span data-ttu-id="ec21a-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="ec21a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ec21a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ec21a-120">-KeyName</span></span>
<span data-ttu-id="ec21a-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="ec21a-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="ec21a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec21a-122">-Name</span></span>
<span data-ttu-id="ec21a-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="ec21a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ec21a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec21a-124">-PassThru</span></span>
<span data-ttu-id="ec21a-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ec21a-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec21a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec21a-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec21a-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ec21a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ec21a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec21a-128">-ResourceId</span></span>
<span data-ttu-id="ec21a-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ec21a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ec21a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ec21a-130">-Confirm</span></span>
<span data-ttu-id="ec21a-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec21a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec21a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec21a-132">-WhatIf</span></span>
<span data-ttu-id="ec21a-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec21a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec21a-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec21a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec21a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec21a-135">CommonParameters</span></span>
<span data-ttu-id="ec21a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec21a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec21a-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec21a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec21a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ec21a-138">INPUTS</span></span>

### <span data-ttu-id="ec21a-139">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="ec21a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="ec21a-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ec21a-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ec21a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ec21a-141">System.String</span></span>

## <span data-ttu-id="ec21a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ec21a-142">OUTPUTS</span></span>

### <span data-ttu-id="ec21a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="ec21a-143">System.Boolean</span></span>

## <span data-ttu-id="ec21a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ec21a-144">NOTES</span></span>

## <span data-ttu-id="ec21a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec21a-145">RELATED LINKS</span></span>
