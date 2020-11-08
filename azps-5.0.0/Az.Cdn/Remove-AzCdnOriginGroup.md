---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140541"
---
# <span data-ttu-id="bd7ca-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bd7ca-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="bd7ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7ca-103">移除 CDN 來源群組</span><span class="sxs-lookup"><span data-stu-id="bd7ca-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="bd7ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd7ca-104">SYNTAX</span></span>

### <span data-ttu-id="bd7ca-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd7ca-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd7ca-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd7ca-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd7ca-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd7ca-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd7ca-108">說明</span><span class="sxs-lookup"><span data-stu-id="bd7ca-108">DESCRIPTION</span></span>
<span data-ttu-id="bd7ca-109">Remove-AzCdnOriginGroup 會從指定的端點中移除 CDN 來源群組。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="bd7ca-110">示例</span><span class="sxs-lookup"><span data-stu-id="bd7ca-110">EXAMPLES</span></span>

### <span data-ttu-id="bd7ca-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bd7ca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="bd7ca-112">這個 Cmdlet 會從指定的端點移除指定的原始群組。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="bd7ca-113">參數</span><span class="sxs-lookup"><span data-stu-id="bd7ca-113">PARAMETERS</span></span>

### <span data-ttu-id="bd7ca-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bd7ca-114">-CdnOriginGroup</span></span>
<span data-ttu-id="bd7ca-115">CDN 原始群組物件。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="bd7ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7ca-116">-DefaultProfile</span></span>
<span data-ttu-id="bd7ca-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd7ca-118">-終結點</span><span class="sxs-lookup"><span data-stu-id="bd7ca-118">-EndpointName</span></span>
<span data-ttu-id="bd7ca-119">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bd7ca-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7ca-120">-OriginGroupName</span></span>
<span data-ttu-id="bd7ca-121">Azure CDN 原始組名。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="bd7ca-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd7ca-122">-PassThru</span></span>
<span data-ttu-id="bd7ca-123">傳回物件（如果已指定）。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-123">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7ca-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bd7ca-124">-ProfileName</span></span>
<span data-ttu-id="bd7ca-125">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bd7ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd7ca-127">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="bd7ca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7ca-128">-ResourceId</span></span>
<span data-ttu-id="bd7ca-129">Azure CDN 原始群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7ca-130">-確認</span><span class="sxs-lookup"><span data-stu-id="bd7ca-130">-Confirm</span></span>
<span data-ttu-id="bd7ca-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd7ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7ca-132">-WhatIf</span></span>
<span data-ttu-id="bd7ca-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd7ca-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd7ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7ca-135">CommonParameters</span></span>
<span data-ttu-id="bd7ca-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7ca-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bd7ca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7ca-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bd7ca-138">INPUTS</span></span>

### <span data-ttu-id="bd7ca-139">所有</span><span class="sxs-lookup"><span data-stu-id="bd7ca-139">None</span></span>

## <span data-ttu-id="bd7ca-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bd7ca-140">OUTPUTS</span></span>

### <span data-ttu-id="bd7ca-141">System.object</span><span class="sxs-lookup"><span data-stu-id="bd7ca-141">System.Boolean</span></span>

## <span data-ttu-id="bd7ca-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bd7ca-142">NOTES</span></span>

## <span data-ttu-id="bd7ca-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd7ca-143">RELATED LINKS</span></span>