---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916584"
---
# <span data-ttu-id="9fcc5-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9fcc5-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="9fcc5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9fcc5-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcc5-103">獲得 CDN 原始伺服器。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="9fcc5-104">語法</span><span class="sxs-lookup"><span data-stu-id="9fcc5-104">SYNTAX</span></span>

### <span data-ttu-id="9fcc5-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9fcc5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fcc5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fcc5-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fcc5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fcc5-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fcc5-108">描述</span><span class="sxs-lookup"><span data-stu-id="9fcc5-108">DESCRIPTION</span></span>
<span data-ttu-id="9fcc5-109">**Get-AzCdnOrigin** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 來源伺服器及其組組資料。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="9fcc5-110">例子</span><span class="sxs-lookup"><span data-stu-id="9fcc5-110">EXAMPLES</span></span>

## <span data-ttu-id="9fcc5-111">參數</span><span class="sxs-lookup"><span data-stu-id="9fcc5-111">PARAMETERS</span></span>

### <span data-ttu-id="9fcc5-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fcc5-112">-CdnEndpoint</span></span>
<span data-ttu-id="9fcc5-113">指定來源所屬的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="9fcc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcc5-114">-DefaultProfile</span></span>
<span data-ttu-id="9fcc5-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9fcc5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fcc5-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9fcc5-116">-EndpointName</span></span>
<span data-ttu-id="9fcc5-117">指定來源伺服器所屬的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="9fcc5-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="9fcc5-118">-OriginName</span></span>
<span data-ttu-id="9fcc5-119">指定原始伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="9fcc5-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9fcc5-120">-ProfileName</span></span>
<span data-ttu-id="9fcc5-121">指定來源伺服器所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="9fcc5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fcc5-122">-ResourceGroupName</span></span>
<span data-ttu-id="9fcc5-123">指定來源伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="9fcc5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fcc5-124">-ResourceId</span></span>
<span data-ttu-id="9fcc5-125">Azure CDN 來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="9fcc5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcc5-126">CommonParameters</span></span>
<span data-ttu-id="9fcc5-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9fcc5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcc5-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fcc5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcc5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9fcc5-129">INPUTS</span></span>

### <span data-ttu-id="9fcc5-130">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fcc5-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9fcc5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9fcc5-131">OUTPUTS</span></span>

### <span data-ttu-id="9fcc5-132">Microsoft.Azure.Commands.Cdn.models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="9fcc5-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="9fcc5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9fcc5-133">NOTES</span></span>

## <span data-ttu-id="9fcc5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fcc5-134">RELATED LINKS</span></span>

[<span data-ttu-id="9fcc5-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="9fcc5-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


