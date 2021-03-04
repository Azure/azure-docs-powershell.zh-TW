---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 73d5c679e1079f99cc19f2af6c22e2d5b5a491fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914170"
---
# <span data-ttu-id="a92b2-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a92b2-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="a92b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a92b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a92b2-103">載入內容至端點。</span><span class="sxs-lookup"><span data-stu-id="a92b2-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="a92b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a92b2-104">SYNTAX</span></span>

### <span data-ttu-id="a92b2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a92b2-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92b2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a92b2-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a92b2-107">描述</span><span class="sxs-lookup"><span data-stu-id="a92b2-107">DESCRIPTION</span></span>
<span data-ttu-id="a92b2-108">**Publish-AzCdnEndpointContent** Cmdlet 會載入來自 Azure 內容傳遞網路 (CDN 端點) 的內容。</span><span class="sxs-lookup"><span data-stu-id="a92b2-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a92b2-109">例子</span><span class="sxs-lookup"><span data-stu-id="a92b2-109">EXAMPLES</span></span>

## <span data-ttu-id="a92b2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a92b2-110">PARAMETERS</span></span>

### <span data-ttu-id="a92b2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a92b2-111">-CdnEndpoint</span></span>
<span data-ttu-id="a92b2-112">指定 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="a92b2-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="a92b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92b2-113">-DefaultProfile</span></span>
<span data-ttu-id="a92b2-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a92b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92b2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a92b2-115">-EndpointName</span></span>
<span data-ttu-id="a92b2-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a92b2-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a92b2-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="a92b2-117">-LoadContent</span></span>
<span data-ttu-id="a92b2-118">指定此 Cmdlet 所發佈之原始伺服器上內容的相對路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="a92b2-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92b2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a92b2-119">-PassThru</span></span>
<span data-ttu-id="a92b2-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a92b2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a92b2-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a92b2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a92b2-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a92b2-122">-ProfileName</span></span>
<span data-ttu-id="a92b2-123">指定來源伺服器所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="a92b2-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a92b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a92b2-125">指定來源伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a92b2-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a92b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92b2-126">CommonParameters</span></span>
<span data-ttu-id="a92b2-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a92b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92b2-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a92b2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92b2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a92b2-129">INPUTS</span></span>

### <span data-ttu-id="a92b2-130">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a92b2-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="a92b2-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a92b2-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a92b2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a92b2-132">OUTPUTS</span></span>

### <span data-ttu-id="a92b2-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a92b2-133">System.Boolean</span></span>

## <span data-ttu-id="a92b2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a92b2-134">NOTES</span></span>

## <span data-ttu-id="a92b2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a92b2-135">RELATED LINKS</span></span>

[<span data-ttu-id="a92b2-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a92b2-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


