---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 34d5b4dccb43f604625652f1c39b2250926058d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914177"
---
# <span data-ttu-id="e9b0c-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="e9b0c-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="e9b0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b0c-103">建立新的 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="e9b0c-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="e9b0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9b0c-104">SYNTAX</span></span>

### <span data-ttu-id="e9b0c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9b0c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9b0c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9b0c-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b0c-107">描述</span><span class="sxs-lookup"><span data-stu-id="e9b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="e9b0c-108">此New-AzCdnOriginGroup會于指定的端點內建立新原始群組。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="e9b0c-109">如果這是端點的第一個來源群組，則也必須設定 DefaultOriginGroup 屬性。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="e9b0c-110">例子</span><span class="sxs-lookup"><span data-stu-id="e9b0c-110">EXAMPLES</span></span>

### <span data-ttu-id="e9b0c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e9b0c-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="e9b0c-112">此 Cmdlet 會于指定的端點內建立新原始組。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="e9b0c-113">它會使用所給予的來源識別碼做為一組來源。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="e9b0c-114">參數</span><span class="sxs-lookup"><span data-stu-id="e9b0c-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b0c-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="e9b0c-115">-CdnOriginGroup</span></span>
<span data-ttu-id="e9b0c-116">CDN 來源群組物件。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-116">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b0c-117">-DefaultProfile</span></span>
<span data-ttu-id="e9b0c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9b0c-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e9b0c-119">-EndpointName</span></span>
<span data-ttu-id="e9b0c-120">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b0c-121">-OriginGroupName</span></span>
<span data-ttu-id="e9b0c-122">Azure CDN 來源組名。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-122">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="e9b0c-123">-OriginId</span></span>
<span data-ttu-id="e9b0c-124">Azure CDN 來源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-125">-IntervalIn自下拉式</span><span class="sxs-lookup"><span data-stu-id="e9b0c-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="e9b0c-126">健康狀態小數之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-127">-PathPath</span><span class="sxs-lookup"><span data-stu-id="e9b0c-127">-ProbePath</span></span>
<span data-ttu-id="e9b0c-128">這是用來判斷來源健康狀態之來源的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-129">-為Protocol</span><span class="sxs-lookup"><span data-stu-id="e9b0c-129">-ProbeProtocol</span></span>
<span data-ttu-id="e9b0c-130">用於健康調查的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-131">-一體式</span><span class="sxs-lookup"><span data-stu-id="e9b0c-131">-ProbeRequestType</span></span>
<span data-ttu-id="e9b0c-132">已提出健康要求的類型。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e9b0c-133">-ProfileName</span></span>
<span data-ttu-id="e9b0c-134">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-134">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b0c-135">-ResourceGroupName</span></span>
<span data-ttu-id="e9b0c-136">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-136">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b0c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e9b0c-137">-Confirm</span></span>
<span data-ttu-id="e9b0c-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b0c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b0c-139">-WhatIf</span></span>
<span data-ttu-id="e9b0c-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9b0c-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b0c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b0c-142">CommonParameters</span></span>
<span data-ttu-id="e9b0c-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9b0c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b0c-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9b0c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b0c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e9b0c-145">INPUTS</span></span>

### <span data-ttu-id="e9b0c-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="e9b0c-146">System.Object</span></span>

## <span data-ttu-id="e9b0c-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e9b0c-147">OUTPUTS</span></span>

### <span data-ttu-id="e9b0c-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="e9b0c-148">System.Object</span></span>

## <span data-ttu-id="e9b0c-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e9b0c-149">NOTES</span></span>

## <span data-ttu-id="e9b0c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9b0c-150">RELATED LINKS</span></span>
