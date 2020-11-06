---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: eb4215a281b83bd533a7502e3ec538ec4e3a570c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451916"
---
# <span data-ttu-id="43eb6-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="43eb6-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="43eb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="43eb6-103">取得 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="43eb6-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43eb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="43eb6-104">SYNTAX</span></span>

### <span data-ttu-id="43eb6-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43eb6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43eb6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43eb6-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43eb6-107">說明</span><span class="sxs-lookup"><span data-stu-id="43eb6-107">DESCRIPTION</span></span>
<span data-ttu-id="43eb6-108">**AzureRMCdnEndpoint** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 端點及其相關聯的設定資料。</span><span class="sxs-lookup"><span data-stu-id="43eb6-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="43eb6-109">示例</span><span class="sxs-lookup"><span data-stu-id="43eb6-109">EXAMPLES</span></span>

## <span data-ttu-id="43eb6-110">參數</span><span class="sxs-lookup"><span data-stu-id="43eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="43eb6-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="43eb6-111">-CdnProfile</span></span>
<span data-ttu-id="43eb6-112">指定端點所屬的 CDN 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="43eb6-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="43eb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43eb6-113">-DefaultProfile</span></span>
<span data-ttu-id="43eb6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="43eb6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43eb6-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="43eb6-115">-EndpointName</span></span>
<span data-ttu-id="43eb6-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="43eb6-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="43eb6-117">端點的名稱不是端點的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="43eb6-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="43eb6-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="43eb6-118">-ProfileName</span></span>
<span data-ttu-id="43eb6-119">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="43eb6-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="43eb6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43eb6-120">-ResourceGroupName</span></span>
<span data-ttu-id="43eb6-121">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43eb6-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="43eb6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43eb6-122">CommonParameters</span></span>
<span data-ttu-id="43eb6-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43eb6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43eb6-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43eb6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43eb6-125">輸入</span><span class="sxs-lookup"><span data-stu-id="43eb6-125">INPUTS</span></span>

### <span data-ttu-id="43eb6-126">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43eb6-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="43eb6-127">參數： CdnProfile (ByValue) </span><span class="sxs-lookup"><span data-stu-id="43eb6-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="43eb6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="43eb6-128">OUTPUTS</span></span>

### <span data-ttu-id="43eb6-129">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="43eb6-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="43eb6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="43eb6-130">NOTES</span></span>

## <span data-ttu-id="43eb6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="43eb6-131">RELATED LINKS</span></span>

[<span data-ttu-id="43eb6-132">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="43eb6-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="43eb6-133">移除-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="43eb6-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="43eb6-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="43eb6-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="43eb6-135">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="43eb6-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="43eb6-136">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="43eb6-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


