---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: b6c5a95e8966cfe22b520c1f41b87f88cbdb1361
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910290"
---
# <span data-ttu-id="eea6c-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="eea6c-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="eea6c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eea6c-102">SYNOPSIS</span></span>
<span data-ttu-id="eea6c-103">移除 CDN 來源</span><span class="sxs-lookup"><span data-stu-id="eea6c-103">Removes a CDN origin</span></span>

## <span data-ttu-id="eea6c-104">語法</span><span class="sxs-lookup"><span data-stu-id="eea6c-104">SYNTAX</span></span>

### <span data-ttu-id="eea6c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eea6c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea6c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea6c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea6c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea6c-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea6c-108">描述</span><span class="sxs-lookup"><span data-stu-id="eea6c-108">DESCRIPTION</span></span>
<span data-ttu-id="eea6c-109">Remove-AzCdnOrigin會從特定端點刪除 CDN 來源。</span><span class="sxs-lookup"><span data-stu-id="eea6c-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="eea6c-110">如果來源是指定端點內的唯一來源，則刪除將會失敗，因為至少需要 1 個來源。</span><span class="sxs-lookup"><span data-stu-id="eea6c-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="eea6c-111">例子</span><span class="sxs-lookup"><span data-stu-id="eea6c-111">EXAMPLES</span></span>

### <span data-ttu-id="eea6c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="eea6c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="eea6c-113">此 Cmdlet 會從指定的端點移除指定的來源。</span><span class="sxs-lookup"><span data-stu-id="eea6c-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="eea6c-114">參數</span><span class="sxs-lookup"><span data-stu-id="eea6c-114">PARAMETERS</span></span>

### <span data-ttu-id="eea6c-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="eea6c-115">-CdnOrigin</span></span>
<span data-ttu-id="eea6c-116">CDN 來源物件。</span><span class="sxs-lookup"><span data-stu-id="eea6c-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea6c-117">-DefaultProfile</span></span>
<span data-ttu-id="eea6c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eea6c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea6c-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="eea6c-119">-EndpointName</span></span>
<span data-ttu-id="eea6c-120">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="eea6c-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="eea6c-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="eea6c-121">-OriginName</span></span>
<span data-ttu-id="eea6c-122">Azure CDN 來源名稱。</span><span class="sxs-lookup"><span data-stu-id="eea6c-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="eea6c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea6c-123">-PassThru</span></span>
<span data-ttu-id="eea6c-124">如果指定，則 Return 物件。</span><span class="sxs-lookup"><span data-stu-id="eea6c-124">Return object if specified.</span></span>

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

### <span data-ttu-id="eea6c-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="eea6c-125">-ProfileName</span></span>
<span data-ttu-id="eea6c-126">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="eea6c-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="eea6c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea6c-127">-ResourceGroupName</span></span>
<span data-ttu-id="eea6c-128">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eea6c-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="eea6c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea6c-129">-ResourceId</span></span>
<span data-ttu-id="eea6c-130">Azure CDN 來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eea6c-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="eea6c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="eea6c-131">-Confirm</span></span>
<span data-ttu-id="eea6c-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eea6c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea6c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea6c-133">-WhatIf</span></span>
<span data-ttu-id="eea6c-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eea6c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea6c-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eea6c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea6c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea6c-136">CommonParameters</span></span>
<span data-ttu-id="eea6c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eea6c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea6c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eea6c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea6c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="eea6c-139">INPUTS</span></span>

### <span data-ttu-id="eea6c-140">沒有</span><span class="sxs-lookup"><span data-stu-id="eea6c-140">None</span></span>

## <span data-ttu-id="eea6c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="eea6c-141">OUTPUTS</span></span>

### <span data-ttu-id="eea6c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eea6c-142">System.Boolean</span></span>

## <span data-ttu-id="eea6c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="eea6c-143">NOTES</span></span>

## <span data-ttu-id="eea6c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="eea6c-144">RELATED LINKS</span></span>
