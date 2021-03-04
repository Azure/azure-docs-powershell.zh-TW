---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 21aead3d3dd17b380f466ffdeaf2e5c36c9b1235
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912909"
---
# <span data-ttu-id="8c402-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="8c402-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c402-102">SYNOPSIS</span></span>
<span data-ttu-id="8c402-103">獲得 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="8c402-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="8c402-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c402-104">SYNTAX</span></span>

### <span data-ttu-id="8c402-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8c402-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c402-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c402-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c402-107">描述</span><span class="sxs-lookup"><span data-stu-id="8c402-107">DESCRIPTION</span></span>
<span data-ttu-id="8c402-108">**Get-AzCdnEndpoint** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 端點及其關聯設定資料。</span><span class="sxs-lookup"><span data-stu-id="8c402-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="8c402-109">例子</span><span class="sxs-lookup"><span data-stu-id="8c402-109">EXAMPLES</span></span>

## <span data-ttu-id="8c402-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c402-110">PARAMETERS</span></span>

### <span data-ttu-id="8c402-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="8c402-111">-CdnProfile</span></span>
<span data-ttu-id="8c402-112">指定端點所屬的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8c402-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c402-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c402-113">-DefaultProfile</span></span>
<span data-ttu-id="8c402-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8c402-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c402-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8c402-115">-EndpointName</span></span>
<span data-ttu-id="8c402-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c402-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="8c402-117">端點的名稱不是端點的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="8c402-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="8c402-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8c402-118">-ProfileName</span></span>
<span data-ttu-id="8c402-119">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="8c402-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8c402-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c402-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c402-121">指定端點所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8c402-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8c402-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c402-122">CommonParameters</span></span>
<span data-ttu-id="8c402-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c402-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c402-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c402-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c402-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8c402-125">INPUTS</span></span>

### <span data-ttu-id="8c402-126">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="8c402-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="8c402-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8c402-127">OUTPUTS</span></span>

### <span data-ttu-id="8c402-128">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8c402-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8c402-129">NOTES</span></span>

## <span data-ttu-id="8c402-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c402-130">RELATED LINKS</span></span>

[<span data-ttu-id="8c402-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="8c402-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="8c402-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="8c402-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="8c402-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c402-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


