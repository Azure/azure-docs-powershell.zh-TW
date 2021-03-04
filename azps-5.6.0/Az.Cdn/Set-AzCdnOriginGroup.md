---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: c70c08ad88491d7624b078babb5e62437c22e116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910289"
---
# <span data-ttu-id="dbf05-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="dbf05-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="dbf05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbf05-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf05-103">更新 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="dbf05-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="dbf05-104">語法</span><span class="sxs-lookup"><span data-stu-id="dbf05-104">SYNTAX</span></span>

### <span data-ttu-id="dbf05-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbf05-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbf05-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf05-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf05-107">描述</span><span class="sxs-lookup"><span data-stu-id="dbf05-107">DESCRIPTION</span></span>
<span data-ttu-id="dbf05-108">Set-AzCdnOriginGroup會更新指定端點內指定的原始群組。</span><span class="sxs-lookup"><span data-stu-id="dbf05-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="dbf05-109">例子</span><span class="sxs-lookup"><span data-stu-id="dbf05-109">EXAMPLES</span></span>

### <span data-ttu-id="dbf05-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="dbf05-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="dbf05-111">此 Cmdlet 會更新原始群組中的IntervalIn以秒為單位的屬性。</span><span class="sxs-lookup"><span data-stu-id="dbf05-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="dbf05-112">參數</span><span class="sxs-lookup"><span data-stu-id="dbf05-112">PARAMETERS</span></span>

### <span data-ttu-id="dbf05-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="dbf05-113">-CdnOriginGroup</span></span>
<span data-ttu-id="dbf05-114">CDN 來源群組物件。</span><span class="sxs-lookup"><span data-stu-id="dbf05-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="dbf05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf05-115">-DefaultProfile</span></span>
<span data-ttu-id="dbf05-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbf05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf05-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dbf05-117">-EndpointName</span></span>
<span data-ttu-id="dbf05-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="dbf05-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="dbf05-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf05-119">-OriginGroupName</span></span>
<span data-ttu-id="dbf05-120">Azure CDN 來源組名。</span><span class="sxs-lookup"><span data-stu-id="dbf05-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="dbf05-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="dbf05-121">-OriginId</span></span>
<span data-ttu-id="dbf05-122">Azure CDN 來源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbf05-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="dbf05-123">-IntervalIn自下拉式</span><span class="sxs-lookup"><span data-stu-id="dbf05-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="dbf05-124">健康狀態小數之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="dbf05-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="dbf05-125">-PathPath</span><span class="sxs-lookup"><span data-stu-id="dbf05-125">-ProbePath</span></span>
<span data-ttu-id="dbf05-126">這是用來判斷來源健康狀態之來源的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="dbf05-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="dbf05-127">-為Protocol</span><span class="sxs-lookup"><span data-stu-id="dbf05-127">-ProbeProtocol</span></span>
<span data-ttu-id="dbf05-128">用於健康調查的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dbf05-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="dbf05-129">-一體式</span><span class="sxs-lookup"><span data-stu-id="dbf05-129">-ProbeRequestType</span></span>
<span data-ttu-id="dbf05-130">已提出健康要求的類型。</span><span class="sxs-lookup"><span data-stu-id="dbf05-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="dbf05-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dbf05-131">-ProfileName</span></span>
<span data-ttu-id="dbf05-132">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="dbf05-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="dbf05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf05-133">-ResourceGroupName</span></span>
<span data-ttu-id="dbf05-134">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="dbf05-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="dbf05-135">-確認</span><span class="sxs-lookup"><span data-stu-id="dbf05-135">-Confirm</span></span>
<span data-ttu-id="dbf05-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dbf05-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf05-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf05-137">-WhatIf</span></span>
<span data-ttu-id="dbf05-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbf05-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf05-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbf05-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf05-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf05-140">CommonParameters</span></span>
<span data-ttu-id="dbf05-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbf05-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf05-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbf05-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf05-143">輸入</span><span class="sxs-lookup"><span data-stu-id="dbf05-143">INPUTS</span></span>

### <span data-ttu-id="dbf05-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="dbf05-144">System.Object</span></span>

## <span data-ttu-id="dbf05-145">輸出</span><span class="sxs-lookup"><span data-stu-id="dbf05-145">OUTPUTS</span></span>

### <span data-ttu-id="dbf05-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="dbf05-146">System.Object</span></span>

## <span data-ttu-id="dbf05-147">筆記</span><span class="sxs-lookup"><span data-stu-id="dbf05-147">NOTES</span></span>

## <span data-ttu-id="dbf05-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbf05-148">RELATED LINKS</span></span>
