---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971100"
---
# <span data-ttu-id="28fe5-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28fe5-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="28fe5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="28fe5-103">刪除 Azure IoT 中樞裝置置備服務中的共用訪問原則。</span><span class="sxs-lookup"><span data-stu-id="28fe5-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="28fe5-104">句法</span><span class="sxs-lookup"><span data-stu-id="28fe5-104">SYNTAX</span></span>

### <span data-ttu-id="28fe5-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28fe5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28fe5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28fe5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28fe5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="28fe5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28fe5-108">說明</span><span class="sxs-lookup"><span data-stu-id="28fe5-108">DESCRIPTION</span></span>
<span data-ttu-id="28fe5-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="28fe5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="28fe5-110">示例</span><span class="sxs-lookup"><span data-stu-id="28fe5-110">EXAMPLES</span></span>

### <span data-ttu-id="28fe5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="28fe5-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="28fe5-112">在 Azure IoT 中樞裝置提供服務中刪除共用的存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="28fe5-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="28fe5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="28fe5-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="28fe5-114">在 Azure IoT 中樞裝置中使用管線來刪除共用的存取原則 "mypolicy"。</span><span class="sxs-lookup"><span data-stu-id="28fe5-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="28fe5-115">參數</span><span class="sxs-lookup"><span data-stu-id="28fe5-115">PARAMETERS</span></span>

### <span data-ttu-id="28fe5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fe5-116">-DefaultProfile</span></span>
<span data-ttu-id="28fe5-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28fe5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28fe5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28fe5-118">-InputObject</span></span>
<span data-ttu-id="28fe5-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="28fe5-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="28fe5-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="28fe5-120">-KeyName</span></span>
<span data-ttu-id="28fe5-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="28fe5-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="28fe5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="28fe5-122">-Name</span></span>
<span data-ttu-id="28fe5-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="28fe5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="28fe5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28fe5-124">-PassThru</span></span>
<span data-ttu-id="28fe5-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="28fe5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="28fe5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28fe5-126">-ResourceGroupName</span></span>
<span data-ttu-id="28fe5-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="28fe5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="28fe5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28fe5-128">-ResourceId</span></span>
<span data-ttu-id="28fe5-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="28fe5-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="28fe5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="28fe5-130">-Confirm</span></span>
<span data-ttu-id="28fe5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28fe5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28fe5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28fe5-132">-WhatIf</span></span>
<span data-ttu-id="28fe5-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28fe5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28fe5-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28fe5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28fe5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fe5-135">CommonParameters</span></span>
<span data-ttu-id="28fe5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28fe5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fe5-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28fe5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fe5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="28fe5-138">INPUTS</span></span>

### <span data-ttu-id="28fe5-139">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="28fe5-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="28fe5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="28fe5-140">System.String</span></span>

## <span data-ttu-id="28fe5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="28fe5-141">OUTPUTS</span></span>

### <span data-ttu-id="28fe5-142">System.object</span><span class="sxs-lookup"><span data-stu-id="28fe5-142">System.Boolean</span></span>

## <span data-ttu-id="28fe5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="28fe5-143">NOTES</span></span>

## <span data-ttu-id="28fe5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="28fe5-144">RELATED LINKS</span></span>
