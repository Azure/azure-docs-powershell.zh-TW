---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280031"
---
# <span data-ttu-id="065de-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="065de-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="065de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="065de-102">SYNOPSIS</span></span>
<span data-ttu-id="065de-103">更新 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="065de-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="065de-104">句法</span><span class="sxs-lookup"><span data-stu-id="065de-104">SYNTAX</span></span>

### <span data-ttu-id="065de-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="065de-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="065de-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="065de-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="065de-107">說明</span><span class="sxs-lookup"><span data-stu-id="065de-107">DESCRIPTION</span></span>
<span data-ttu-id="065de-108">Set-AzCdnOriginGroup 將在指定的端點內更新指定的原始群組。</span><span class="sxs-lookup"><span data-stu-id="065de-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="065de-109">示例</span><span class="sxs-lookup"><span data-stu-id="065de-109">EXAMPLES</span></span>

### <span data-ttu-id="065de-110">範例1</span><span class="sxs-lookup"><span data-stu-id="065de-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="065de-111">這個 Cmdlet 會更新 [來源] 群組中的 ProbeIntervalInSeconds 屬性。</span><span class="sxs-lookup"><span data-stu-id="065de-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="065de-112">參數</span><span class="sxs-lookup"><span data-stu-id="065de-112">PARAMETERS</span></span>

### <span data-ttu-id="065de-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="065de-113">-CdnOriginGroup</span></span>
<span data-ttu-id="065de-114">CDN 原始群組物件。</span><span class="sxs-lookup"><span data-stu-id="065de-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="065de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065de-115">-DefaultProfile</span></span>
<span data-ttu-id="065de-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="065de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="065de-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="065de-117">-EndpointName</span></span>
<span data-ttu-id="065de-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="065de-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="065de-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="065de-119">-OriginGroupName</span></span>
<span data-ttu-id="065de-120">Azure CDN 原始組名。</span><span class="sxs-lookup"><span data-stu-id="065de-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="065de-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="065de-121">-OriginId</span></span>
<span data-ttu-id="065de-122">Azure CDN 原始群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="065de-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="065de-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="065de-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="065de-124">Health 探測之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="065de-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="065de-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="065de-125">-ProbePath</span></span>
<span data-ttu-id="065de-126">相對於用於判斷原點健康情況之來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="065de-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="065de-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="065de-127">-ProbeProtocol</span></span>
<span data-ttu-id="065de-128">要用於 health 探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="065de-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="065de-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="065de-129">-ProbeRequestType</span></span>
<span data-ttu-id="065de-130">所進行的健康情況探測要求類型。</span><span class="sxs-lookup"><span data-stu-id="065de-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="065de-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="065de-131">-ProfileName</span></span>
<span data-ttu-id="065de-132">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="065de-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="065de-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="065de-133">-ResourceGroupName</span></span>
<span data-ttu-id="065de-134">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="065de-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="065de-135">-確認</span><span class="sxs-lookup"><span data-stu-id="065de-135">-Confirm</span></span>
<span data-ttu-id="065de-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="065de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="065de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="065de-137">-WhatIf</span></span>
<span data-ttu-id="065de-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="065de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="065de-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="065de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="065de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065de-140">CommonParameters</span></span>
<span data-ttu-id="065de-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="065de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065de-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="065de-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065de-143">輸入</span><span class="sxs-lookup"><span data-stu-id="065de-143">INPUTS</span></span>

### <span data-ttu-id="065de-144">System.object</span><span class="sxs-lookup"><span data-stu-id="065de-144">System.Object</span></span>

## <span data-ttu-id="065de-145">輸出</span><span class="sxs-lookup"><span data-stu-id="065de-145">OUTPUTS</span></span>

### <span data-ttu-id="065de-146">System.object</span><span class="sxs-lookup"><span data-stu-id="065de-146">System.Object</span></span>

## <span data-ttu-id="065de-147">筆記</span><span class="sxs-lookup"><span data-stu-id="065de-147">NOTES</span></span>

## <span data-ttu-id="065de-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="065de-148">RELATED LINKS</span></span>
