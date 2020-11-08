---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129556"
---
# <span data-ttu-id="c2415-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="c2415-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="c2415-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2415-102">SYNOPSIS</span></span>
<span data-ttu-id="c2415-103">刪除裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="c2415-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="c2415-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2415-104">SYNTAX</span></span>

### <span data-ttu-id="c2415-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2415-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2415-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2415-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2415-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2415-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2415-108">說明</span><span class="sxs-lookup"><span data-stu-id="c2415-108">DESCRIPTION</span></span>
<span data-ttu-id="c2415-109">刪除 Azure IoT 中樞裝置提供服務中的註冊群組。</span><span class="sxs-lookup"><span data-stu-id="c2415-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c2415-110">示例</span><span class="sxs-lookup"><span data-stu-id="c2415-110">EXAMPLES</span></span>

### <span data-ttu-id="c2415-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c2415-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="c2415-112">刪除指定的註冊群組。</span><span class="sxs-lookup"><span data-stu-id="c2415-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="c2415-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c2415-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="c2415-114">刪除所有註冊群組。</span><span class="sxs-lookup"><span data-stu-id="c2415-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="c2415-115">參數</span><span class="sxs-lookup"><span data-stu-id="c2415-115">PARAMETERS</span></span>

### <span data-ttu-id="c2415-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2415-116">-DefaultProfile</span></span>
<span data-ttu-id="c2415-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2415-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2415-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c2415-118">-DpsName</span></span>
<span data-ttu-id="c2415-119">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="c2415-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c2415-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c2415-120">-DpsObject</span></span>
<span data-ttu-id="c2415-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="c2415-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c2415-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2415-122">-Name</span></span>
<span data-ttu-id="c2415-123">註冊群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2415-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="c2415-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2415-124">-PassThru</span></span>
<span data-ttu-id="c2415-125">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="c2415-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="c2415-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c2415-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2415-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2415-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2415-128">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c2415-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c2415-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2415-129">-ResourceId</span></span>
<span data-ttu-id="c2415-130">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2415-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c2415-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c2415-131">-Confirm</span></span>
<span data-ttu-id="c2415-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2415-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2415-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2415-133">-WhatIf</span></span>
<span data-ttu-id="c2415-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2415-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2415-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2415-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2415-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2415-136">CommonParameters</span></span>
<span data-ttu-id="c2415-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2415-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2415-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2415-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2415-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c2415-139">INPUTS</span></span>

### <span data-ttu-id="c2415-140">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="c2415-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c2415-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c2415-141">System.String</span></span>

## <span data-ttu-id="c2415-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c2415-142">OUTPUTS</span></span>

### <span data-ttu-id="c2415-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c2415-143">System.Boolean</span></span>

## <span data-ttu-id="c2415-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c2415-144">NOTES</span></span>

## <span data-ttu-id="c2415-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2415-145">RELATED LINKS</span></span>