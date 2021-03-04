---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902761"
---
# <span data-ttu-id="c6a92-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="c6a92-101">Update-AzSignalR</span></span>

## <span data-ttu-id="c6a92-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6a92-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a92-103">更新 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="c6a92-103">Update a SignalR service.</span></span>

## <span data-ttu-id="c6a92-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6a92-104">SYNTAX</span></span>

### <span data-ttu-id="c6a92-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6a92-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6a92-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a92-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6a92-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a92-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a92-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6a92-108">DESCRIPTION</span></span>
<span data-ttu-id="c6a92-109">更新 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="c6a92-109">Update a SignalR service.</span></span>
<span data-ttu-id="c6a92-110">如果未指定，下列值將會用於參數：</span><span class="sxs-lookup"><span data-stu-id="c6a92-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="c6a92-111">`ResourceGroupName`：預設資源群組的設定者 `Set-AzDefault -ResourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="c6a92-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="c6a92-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="c6a92-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="c6a92-113">例子</span><span class="sxs-lookup"><span data-stu-id="c6a92-113">EXAMPLES</span></span>

### <span data-ttu-id="c6a92-114">更新特定的 SignalR 服務。</span><span class="sxs-lookup"><span data-stu-id="c6a92-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="c6a92-115">指定 ServiceMode 和 AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="c6a92-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="c6a92-116">參數</span><span class="sxs-lookup"><span data-stu-id="c6a92-116">PARAMETERS</span></span>

### <span data-ttu-id="c6a92-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="c6a92-117">-AllowedOrigin</span></span>
<span data-ttu-id="c6a92-118">SignalR 服務的允許來源。</span><span class="sxs-lookup"><span data-stu-id="c6a92-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="c6a92-119">若要允許全部使用，請使用 "\*"，然後從清單中移除所有其他來源。</span><span class="sxs-lookup"><span data-stu-id="c6a92-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="c6a92-120">不允許斜線做為網域的一部分或 TLD 之後</span><span class="sxs-lookup"><span data-stu-id="c6a92-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6a92-121">-AsJob</span></span>
<span data-ttu-id="c6a92-122">在背景工作中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6a92-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="c6a92-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a92-123">-DefaultProfile</span></span>
<span data-ttu-id="c6a92-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6a92-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a92-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6a92-125">-InputObject</span></span>
<span data-ttu-id="c6a92-126">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="c6a92-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6a92-127">-Name</span></span>
<span data-ttu-id="c6a92-128">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c6a92-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a92-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6a92-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c6a92-130">The resource group name.</span></span>
<span data-ttu-id="c6a92-131">如果沒有指定，將會使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="c6a92-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6a92-132">-ResourceId</span></span>
<span data-ttu-id="c6a92-133">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a92-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="c6a92-134">-ServiceMode</span></span>
<span data-ttu-id="c6a92-135">SignalR 服務的服務模式。</span><span class="sxs-lookup"><span data-stu-id="c6a92-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="c6a92-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6a92-136">-Sku</span></span>
<span data-ttu-id="c6a92-137">SignalR 服務 SKU。</span><span class="sxs-lookup"><span data-stu-id="c6a92-137">The SignalR service SKU.</span></span>
<span data-ttu-id="c6a92-138">預設為 「Standard_S1」。</span><span class="sxs-lookup"><span data-stu-id="c6a92-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="c6a92-139">-標記</span><span class="sxs-lookup"><span data-stu-id="c6a92-139">-Tag</span></span>
<span data-ttu-id="c6a92-140">SignalR 服務的標記。</span><span class="sxs-lookup"><span data-stu-id="c6a92-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="c6a92-141">-UnitCount</span></span>
<span data-ttu-id="c6a92-142">SignalR 服務單位元數目，值只從 {1， 2， 5， 10， 20， 50， 100}。</span><span class="sxs-lookup"><span data-stu-id="c6a92-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="c6a92-143">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="c6a92-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a92-144">-確認</span><span class="sxs-lookup"><span data-stu-id="c6a92-144">-Confirm</span></span>
<span data-ttu-id="c6a92-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6a92-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a92-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a92-146">-WhatIf</span></span>
<span data-ttu-id="c6a92-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6a92-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6a92-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6a92-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a92-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a92-149">CommonParameters</span></span>
<span data-ttu-id="c6a92-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6a92-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a92-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6a92-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a92-152">輸入</span><span class="sxs-lookup"><span data-stu-id="c6a92-152">INPUTS</span></span>

### <span data-ttu-id="c6a92-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a92-153">System.String</span></span>

### <span data-ttu-id="c6a92-154">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c6a92-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c6a92-155">輸出</span><span class="sxs-lookup"><span data-stu-id="c6a92-155">OUTPUTS</span></span>

### <span data-ttu-id="c6a92-156">Microsoft.Azure.Commands.SignalR.models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c6a92-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c6a92-157">筆記</span><span class="sxs-lookup"><span data-stu-id="c6a92-157">NOTES</span></span>

## <span data-ttu-id="c6a92-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6a92-158">RELATED LINKS</span></span>
