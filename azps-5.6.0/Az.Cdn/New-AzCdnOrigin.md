---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: cc7350fb76091d3bf2f8bdab5c037a5afbe8b57a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909777"
---
# <span data-ttu-id="02eb1-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="02eb1-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="02eb1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="02eb1-103">建立新的 CDN 來源</span><span class="sxs-lookup"><span data-stu-id="02eb1-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="02eb1-104">語法</span><span class="sxs-lookup"><span data-stu-id="02eb1-104">SYNTAX</span></span>

### <span data-ttu-id="02eb1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="02eb1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02eb1-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="02eb1-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02eb1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02eb1-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02eb1-108">描述</span><span class="sxs-lookup"><span data-stu-id="02eb1-108">DESCRIPTION</span></span>
<span data-ttu-id="02eb1-109">此New-AzCdnOrigin會于指定的端點內建立新的 CDN 來源。</span><span class="sxs-lookup"><span data-stu-id="02eb1-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="02eb1-110">例子</span><span class="sxs-lookup"><span data-stu-id="02eb1-110">EXAMPLES</span></span>

### <span data-ttu-id="02eb1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="02eb1-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="02eb1-112">此 Cmdlet 會為指定的端點建立新的 CDN 來源。</span><span class="sxs-lookup"><span data-stu-id="02eb1-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="02eb1-113">它會使用提供的主機名稱做為來源。</span><span class="sxs-lookup"><span data-stu-id="02eb1-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="02eb1-114">參數</span><span class="sxs-lookup"><span data-stu-id="02eb1-114">PARAMETERS</span></span>

### <span data-ttu-id="02eb1-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="02eb1-115">-CdnOrigin</span></span>
<span data-ttu-id="02eb1-116">CDN 來源物件。</span><span class="sxs-lookup"><span data-stu-id="02eb1-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="02eb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02eb1-117">-DefaultProfile</span></span>
<span data-ttu-id="02eb1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02eb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02eb1-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="02eb1-119">-EndpointName</span></span>
<span data-ttu-id="02eb1-120">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="02eb1-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="02eb1-121">-HostName</span></span>
<span data-ttu-id="02eb1-122">Azure CDN 來源主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="02eb1-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-123">-HTTPPort</span><span class="sxs-lookup"><span data-stu-id="02eb1-123">-HttpPort</span></span>
<span data-ttu-id="02eb1-124">Azure CDN 來源 HTTP 埠。</span><span class="sxs-lookup"><span data-stu-id="02eb1-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-125">-HTTPsPort</span><span class="sxs-lookup"><span data-stu-id="02eb1-125">-HttpsPort</span></span>
<span data-ttu-id="02eb1-126">Azure CDN 來源 HTTPs 埠。</span><span class="sxs-lookup"><span data-stu-id="02eb1-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="02eb1-127">-OriginHostHeader</span></span>
<span data-ttu-id="02eb1-128">Azure CDN 來源主機標題。</span><span class="sxs-lookup"><span data-stu-id="02eb1-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="02eb1-129">-OriginName</span></span>
<span data-ttu-id="02eb1-130">Azure CDN 來源名稱。</span><span class="sxs-lookup"><span data-stu-id="02eb1-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="02eb1-131">-Priority</span></span>
<span data-ttu-id="02eb1-132">Azure CDN 來源優先順序。</span><span class="sxs-lookup"><span data-stu-id="02eb1-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="02eb1-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="02eb1-134">要包含在核准要求中以連結至私人連結的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="02eb1-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="02eb1-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="02eb1-136">Azure CDN 來源私人連結位置。</span><span class="sxs-lookup"><span data-stu-id="02eb1-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="02eb1-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="02eb1-138">Azure CDN 來源私人連結資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="02eb1-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="02eb1-139">-ProfileName</span></span>
<span data-ttu-id="02eb1-140">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="02eb1-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02eb1-141">-ResourceGroupName</span></span>
<span data-ttu-id="02eb1-142">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="02eb1-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-143">-重量</span><span class="sxs-lookup"><span data-stu-id="02eb1-143">-Weight</span></span>
<span data-ttu-id="02eb1-144">Azure CDN 來源粗細。</span><span class="sxs-lookup"><span data-stu-id="02eb1-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb1-145">-確認</span><span class="sxs-lookup"><span data-stu-id="02eb1-145">-Confirm</span></span>
<span data-ttu-id="02eb1-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="02eb1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02eb1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02eb1-147">-WhatIf</span></span>
<span data-ttu-id="02eb1-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02eb1-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02eb1-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02eb1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02eb1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02eb1-150">CommonParameters</span></span>
<span data-ttu-id="02eb1-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02eb1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02eb1-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02eb1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02eb1-153">輸入</span><span class="sxs-lookup"><span data-stu-id="02eb1-153">INPUTS</span></span>

### <span data-ttu-id="02eb1-154">沒有</span><span class="sxs-lookup"><span data-stu-id="02eb1-154">None</span></span>

## <span data-ttu-id="02eb1-155">輸出</span><span class="sxs-lookup"><span data-stu-id="02eb1-155">OUTPUTS</span></span>

### <span data-ttu-id="02eb1-156">Microsoft.Azure.Commands.Cdn.models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="02eb1-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="02eb1-157">筆記</span><span class="sxs-lookup"><span data-stu-id="02eb1-157">NOTES</span></span>

## <span data-ttu-id="02eb1-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="02eb1-158">RELATED LINKS</span></span>
