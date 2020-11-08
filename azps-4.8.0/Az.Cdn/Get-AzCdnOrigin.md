---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128377"
---
# <span data-ttu-id="a95bb-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a95bb-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="a95bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a95bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a95bb-103">取得 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="a95bb-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="a95bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="a95bb-104">SYNTAX</span></span>

### <span data-ttu-id="a95bb-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a95bb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a95bb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a95bb-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a95bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="a95bb-107">DESCRIPTION</span></span>
<span data-ttu-id="a95bb-108">**AzCdnOrigin** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 來源伺服器及其設定資料。</span><span class="sxs-lookup"><span data-stu-id="a95bb-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="a95bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="a95bb-109">EXAMPLES</span></span>

## <span data-ttu-id="a95bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="a95bb-110">PARAMETERS</span></span>

### <span data-ttu-id="a95bb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a95bb-111">-CdnEndpoint</span></span>
<span data-ttu-id="a95bb-112">指定原始所歸屬的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="a95bb-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95bb-113">-DefaultProfile</span></span>
<span data-ttu-id="a95bb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a95bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a95bb-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="a95bb-115">-EndpointName</span></span>
<span data-ttu-id="a95bb-116">指定原始伺服器所屬端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95bb-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a95bb-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="a95bb-117">-OriginName</span></span>
<span data-ttu-id="a95bb-118">指定原始伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95bb-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="a95bb-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a95bb-119">-ProfileName</span></span>
<span data-ttu-id="a95bb-120">指定原始伺服器所屬之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95bb-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a95bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="a95bb-122">指定原始伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95bb-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a95bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95bb-123">CommonParameters</span></span>
<span data-ttu-id="a95bb-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a95bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95bb-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a95bb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95bb-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a95bb-126">INPUTS</span></span>

### <span data-ttu-id="a95bb-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="a95bb-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a95bb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a95bb-128">OUTPUTS</span></span>

### <span data-ttu-id="a95bb-129">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="a95bb-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="a95bb-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a95bb-130">NOTES</span></span>

## <span data-ttu-id="a95bb-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a95bb-131">RELATED LINKS</span></span>

[<span data-ttu-id="a95bb-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a95bb-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)

