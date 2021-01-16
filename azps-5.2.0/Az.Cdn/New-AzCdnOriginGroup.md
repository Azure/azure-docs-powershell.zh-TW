---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282251"
---
# <span data-ttu-id="71627-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="71627-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="71627-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71627-102">SYNOPSIS</span></span>
<span data-ttu-id="71627-103">建立新的 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="71627-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="71627-104">句法</span><span class="sxs-lookup"><span data-stu-id="71627-104">SYNTAX</span></span>

### <span data-ttu-id="71627-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71627-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71627-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71627-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71627-107">說明</span><span class="sxs-lookup"><span data-stu-id="71627-107">DESCRIPTION</span></span>
<span data-ttu-id="71627-108">New-AzCdnOriginGroup 會在指定的端點中建立新的原始群組。</span><span class="sxs-lookup"><span data-stu-id="71627-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="71627-109">如果這是端點的第一個原始群組，則也必須設定 DefaultOriginGroup 屬性。</span><span class="sxs-lookup"><span data-stu-id="71627-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="71627-110">示例</span><span class="sxs-lookup"><span data-stu-id="71627-110">EXAMPLES</span></span>

### <span data-ttu-id="71627-111">範例1</span><span class="sxs-lookup"><span data-stu-id="71627-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="71627-112">這個 Cmdlet 會在指定的端點中建立新的原始群組。</span><span class="sxs-lookup"><span data-stu-id="71627-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="71627-113">它會使用指定的原始 id 作為來源集合。</span><span class="sxs-lookup"><span data-stu-id="71627-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="71627-114">參數</span><span class="sxs-lookup"><span data-stu-id="71627-114">PARAMETERS</span></span>

### <span data-ttu-id="71627-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="71627-115">-CdnOriginGroup</span></span>
<span data-ttu-id="71627-116">CDN 原始群組物件。</span><span class="sxs-lookup"><span data-stu-id="71627-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="71627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71627-117">-DefaultProfile</span></span>
<span data-ttu-id="71627-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71627-119">-終結點</span><span class="sxs-lookup"><span data-stu-id="71627-119">-EndpointName</span></span>
<span data-ttu-id="71627-120">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="71627-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="71627-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="71627-121">-OriginGroupName</span></span>
<span data-ttu-id="71627-122">Azure CDN 原始組名。</span><span class="sxs-lookup"><span data-stu-id="71627-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="71627-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="71627-123">-OriginId</span></span>
<span data-ttu-id="71627-124">Azure CDN 原始群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="71627-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="71627-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="71627-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="71627-126">Health 探測之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="71627-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="71627-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="71627-127">-ProbePath</span></span>
<span data-ttu-id="71627-128">相對於用於判斷原點健康情況之來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="71627-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="71627-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="71627-129">-ProbeProtocol</span></span>
<span data-ttu-id="71627-130">要用於 health 探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="71627-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="71627-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="71627-131">-ProbeRequestType</span></span>
<span data-ttu-id="71627-132">所進行的健康情況探測要求類型。</span><span class="sxs-lookup"><span data-stu-id="71627-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="71627-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="71627-133">-ProfileName</span></span>
<span data-ttu-id="71627-134">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="71627-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="71627-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71627-135">-ResourceGroupName</span></span>
<span data-ttu-id="71627-136">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="71627-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="71627-137">-確認</span><span class="sxs-lookup"><span data-stu-id="71627-137">-Confirm</span></span>
<span data-ttu-id="71627-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71627-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71627-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71627-139">-WhatIf</span></span>
<span data-ttu-id="71627-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71627-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71627-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71627-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71627-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71627-142">CommonParameters</span></span>
<span data-ttu-id="71627-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71627-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71627-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71627-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71627-145">輸入</span><span class="sxs-lookup"><span data-stu-id="71627-145">INPUTS</span></span>

### <span data-ttu-id="71627-146">System.object</span><span class="sxs-lookup"><span data-stu-id="71627-146">System.Object</span></span>

## <span data-ttu-id="71627-147">輸出</span><span class="sxs-lookup"><span data-stu-id="71627-147">OUTPUTS</span></span>

### <span data-ttu-id="71627-148">System.object</span><span class="sxs-lookup"><span data-stu-id="71627-148">System.Object</span></span>

## <span data-ttu-id="71627-149">筆記</span><span class="sxs-lookup"><span data-stu-id="71627-149">NOTES</span></span>

## <span data-ttu-id="71627-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="71627-150">RELATED LINKS</span></span>
