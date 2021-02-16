---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139426"
---
# <span data-ttu-id="e6c09-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e6c09-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="e6c09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6c09-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c09-103">建立新的 CDN 來源</span><span class="sxs-lookup"><span data-stu-id="e6c09-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="e6c09-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6c09-104">SYNTAX</span></span>

### <span data-ttu-id="e6c09-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e6c09-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c09-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6c09-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c09-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6c09-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c09-108">說明</span><span class="sxs-lookup"><span data-stu-id="e6c09-108">DESCRIPTION</span></span>
<span data-ttu-id="e6c09-109">New-AzCdnOrigin 將在指定的端點中建立新的 CDN 來源。</span><span class="sxs-lookup"><span data-stu-id="e6c09-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="e6c09-110">示例</span><span class="sxs-lookup"><span data-stu-id="e6c09-110">EXAMPLES</span></span>

### <span data-ttu-id="e6c09-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e6c09-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="e6c09-112">這個 Cmdlet 會為指定的端點建立新的 CDN 來源。</span><span class="sxs-lookup"><span data-stu-id="e6c09-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="e6c09-113">它會使用提供的主機名稱作為來源。</span><span class="sxs-lookup"><span data-stu-id="e6c09-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="e6c09-114">參數</span><span class="sxs-lookup"><span data-stu-id="e6c09-114">PARAMETERS</span></span>

### <span data-ttu-id="e6c09-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e6c09-115">-CdnOrigin</span></span>
<span data-ttu-id="e6c09-116">CDN 來源物件。</span><span class="sxs-lookup"><span data-stu-id="e6c09-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="e6c09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c09-117">-DefaultProfile</span></span>
<span data-ttu-id="e6c09-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6c09-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c09-119">-終結點</span><span class="sxs-lookup"><span data-stu-id="e6c09-119">-EndpointName</span></span>
<span data-ttu-id="e6c09-120">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c09-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e6c09-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="e6c09-121">-HostName</span></span>
<span data-ttu-id="e6c09-122">Azure CDN 原始主機名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c09-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="e6c09-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e6c09-123">-HttpPort</span></span>
<span data-ttu-id="e6c09-124">Azure CDN 原始 HTTP 埠。</span><span class="sxs-lookup"><span data-stu-id="e6c09-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="e6c09-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e6c09-125">-HttpsPort</span></span>
<span data-ttu-id="e6c09-126">Azure CDN 起源 HTTPs 埠。</span><span class="sxs-lookup"><span data-stu-id="e6c09-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="e6c09-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="e6c09-127">-OriginHostHeader</span></span>
<span data-ttu-id="e6c09-128">Azure CDN 來源主機標頭。</span><span class="sxs-lookup"><span data-stu-id="e6c09-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="e6c09-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e6c09-129">-OriginName</span></span>
<span data-ttu-id="e6c09-130">Azure CDN 原始名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c09-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="e6c09-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="e6c09-131">-Priority</span></span>
<span data-ttu-id="e6c09-132">Azure CDN 原始優先順序。</span><span class="sxs-lookup"><span data-stu-id="e6c09-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="e6c09-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="e6c09-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="e6c09-134">要包含在要連線到私人連結之核准要求中的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="e6c09-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="e6c09-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="e6c09-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="e6c09-136">Azure CDN 來源私人連結位置。</span><span class="sxs-lookup"><span data-stu-id="e6c09-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="e6c09-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e6c09-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e6c09-138">Azure CDN 來源私人連結資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6c09-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="e6c09-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e6c09-139">-ProfileName</span></span>
<span data-ttu-id="e6c09-140">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c09-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e6c09-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c09-141">-ResourceGroupName</span></span>
<span data-ttu-id="e6c09-142">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="e6c09-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="e6c09-143">寬度</span><span class="sxs-lookup"><span data-stu-id="e6c09-143">-Weight</span></span>
<span data-ttu-id="e6c09-144">Azure CDN 原始重量。</span><span class="sxs-lookup"><span data-stu-id="e6c09-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="e6c09-145">-確認</span><span class="sxs-lookup"><span data-stu-id="e6c09-145">-Confirm</span></span>
<span data-ttu-id="e6c09-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6c09-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6c09-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6c09-147">-WhatIf</span></span>
<span data-ttu-id="e6c09-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6c09-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6c09-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6c09-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6c09-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c09-150">CommonParameters</span></span>
<span data-ttu-id="e6c09-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6c09-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c09-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e6c09-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c09-153">輸入</span><span class="sxs-lookup"><span data-stu-id="e6c09-153">INPUTS</span></span>

### <span data-ttu-id="e6c09-154">所有</span><span class="sxs-lookup"><span data-stu-id="e6c09-154">None</span></span>

## <span data-ttu-id="e6c09-155">輸出</span><span class="sxs-lookup"><span data-stu-id="e6c09-155">OUTPUTS</span></span>

### <span data-ttu-id="e6c09-156">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="e6c09-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e6c09-157">筆記</span><span class="sxs-lookup"><span data-stu-id="e6c09-157">NOTES</span></span>

## <span data-ttu-id="e6c09-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6c09-158">RELATED LINKS</span></span>
