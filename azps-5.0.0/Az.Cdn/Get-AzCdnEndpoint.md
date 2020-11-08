---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140987"
---
# <span data-ttu-id="73bdd-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="73bdd-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="73bdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="73bdd-103">取得 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="73bdd-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="73bdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="73bdd-104">SYNTAX</span></span>

### <span data-ttu-id="73bdd-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="73bdd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73bdd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73bdd-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73bdd-107">說明</span><span class="sxs-lookup"><span data-stu-id="73bdd-107">DESCRIPTION</span></span>
<span data-ttu-id="73bdd-108">**AzCdnEndpoint** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 端點及其相關聯的設定資料。</span><span class="sxs-lookup"><span data-stu-id="73bdd-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="73bdd-109">示例</span><span class="sxs-lookup"><span data-stu-id="73bdd-109">EXAMPLES</span></span>

## <span data-ttu-id="73bdd-110">參數</span><span class="sxs-lookup"><span data-stu-id="73bdd-110">PARAMETERS</span></span>

### <span data-ttu-id="73bdd-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="73bdd-111">-CdnProfile</span></span>
<span data-ttu-id="73bdd-112">指定端點所屬的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="73bdd-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="73bdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bdd-113">-DefaultProfile</span></span>
<span data-ttu-id="73bdd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="73bdd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73bdd-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="73bdd-115">-EndpointName</span></span>
<span data-ttu-id="73bdd-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="73bdd-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="73bdd-117">端點的名稱不是端點的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="73bdd-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="73bdd-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="73bdd-118">-ProfileName</span></span>
<span data-ttu-id="73bdd-119">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="73bdd-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="73bdd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bdd-120">-ResourceGroupName</span></span>
<span data-ttu-id="73bdd-121">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73bdd-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="73bdd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bdd-122">CommonParameters</span></span>
<span data-ttu-id="73bdd-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73bdd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bdd-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73bdd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bdd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="73bdd-125">INPUTS</span></span>

### <span data-ttu-id="73bdd-126">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="73bdd-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="73bdd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="73bdd-127">OUTPUTS</span></span>

### <span data-ttu-id="73bdd-128">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="73bdd-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="73bdd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="73bdd-129">NOTES</span></span>

## <span data-ttu-id="73bdd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="73bdd-130">RELATED LINKS</span></span>

[<span data-ttu-id="73bdd-131">新-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="73bdd-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="73bdd-132">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="73bdd-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="73bdd-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="73bdd-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="73bdd-134">開始-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="73bdd-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="73bdd-135">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="73bdd-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


