---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958136"
---
# <span data-ttu-id="59bbc-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59bbc-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="59bbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="59bbc-103">取得 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="59bbc-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="59bbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="59bbc-104">SYNTAX</span></span>

### <span data-ttu-id="59bbc-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="59bbc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59bbc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59bbc-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59bbc-107">說明</span><span class="sxs-lookup"><span data-stu-id="59bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="59bbc-108">**AzCdnEndpoint** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 端點及其相關聯的設定資料。</span><span class="sxs-lookup"><span data-stu-id="59bbc-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="59bbc-109">示例</span><span class="sxs-lookup"><span data-stu-id="59bbc-109">EXAMPLES</span></span>

## <span data-ttu-id="59bbc-110">參數</span><span class="sxs-lookup"><span data-stu-id="59bbc-110">PARAMETERS</span></span>

### <span data-ttu-id="59bbc-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="59bbc-111">-CdnProfile</span></span>
<span data-ttu-id="59bbc-112">指定端點所屬的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="59bbc-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="59bbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bbc-113">-DefaultProfile</span></span>
<span data-ttu-id="59bbc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="59bbc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59bbc-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="59bbc-115">-EndpointName</span></span>
<span data-ttu-id="59bbc-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="59bbc-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="59bbc-117">端點的名稱不是端點的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="59bbc-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="59bbc-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="59bbc-118">-ProfileName</span></span>
<span data-ttu-id="59bbc-119">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="59bbc-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="59bbc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59bbc-120">-ResourceGroupName</span></span>
<span data-ttu-id="59bbc-121">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59bbc-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="59bbc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bbc-122">CommonParameters</span></span>
<span data-ttu-id="59bbc-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59bbc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bbc-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59bbc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bbc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="59bbc-125">INPUTS</span></span>

### <span data-ttu-id="59bbc-126">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59bbc-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="59bbc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="59bbc-127">OUTPUTS</span></span>

### <span data-ttu-id="59bbc-128">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="59bbc-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="59bbc-129">筆記</span><span class="sxs-lookup"><span data-stu-id="59bbc-129">NOTES</span></span>

## <span data-ttu-id="59bbc-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="59bbc-130">RELATED LINKS</span></span>

[<span data-ttu-id="59bbc-131">新-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59bbc-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="59bbc-132">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59bbc-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="59bbc-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59bbc-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="59bbc-134">開始-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59bbc-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="59bbc-135">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59bbc-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


