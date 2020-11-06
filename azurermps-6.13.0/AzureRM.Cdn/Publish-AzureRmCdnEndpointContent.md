---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a4a2479c6dc7c116ff7da9151fcd5dea5ec26660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450272"
---
# <span data-ttu-id="efad5-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="efad5-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="efad5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efad5-102">SYNOPSIS</span></span>
<span data-ttu-id="efad5-103">將內容載入到端點。</span><span class="sxs-lookup"><span data-stu-id="efad5-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efad5-104">句法</span><span class="sxs-lookup"><span data-stu-id="efad5-104">SYNTAX</span></span>

### <span data-ttu-id="efad5-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="efad5-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efad5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efad5-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efad5-107">說明</span><span class="sxs-lookup"><span data-stu-id="efad5-107">DESCRIPTION</span></span>
<span data-ttu-id="efad5-108">**AzureRmCdnEndpointContent** Cmdlet 會從來源伺服器載入 Azure 內容傳遞網路 (CDN) 端點的內容。</span><span class="sxs-lookup"><span data-stu-id="efad5-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="efad5-109">示例</span><span class="sxs-lookup"><span data-stu-id="efad5-109">EXAMPLES</span></span>

## <span data-ttu-id="efad5-110">參數</span><span class="sxs-lookup"><span data-stu-id="efad5-110">PARAMETERS</span></span>

### <span data-ttu-id="efad5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="efad5-111">-CdnEndpoint</span></span>
<span data-ttu-id="efad5-112">Sepcifies CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="efad5-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="efad5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efad5-113">-DefaultProfile</span></span>
<span data-ttu-id="efad5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="efad5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efad5-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="efad5-115">-EndpointName</span></span>
<span data-ttu-id="efad5-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="efad5-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="efad5-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="efad5-117">-LoadContent</span></span>
<span data-ttu-id="efad5-118">指定此 Cmdlet 發佈之原始伺服器內容的相對路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="efad5-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="efad5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efad5-119">-PassThru</span></span>
<span data-ttu-id="efad5-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="efad5-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="efad5-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="efad5-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="efad5-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="efad5-122">-ProfileName</span></span>
<span data-ttu-id="efad5-123">指定原始伺服器所屬之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="efad5-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="efad5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efad5-124">-ResourceGroupName</span></span>
<span data-ttu-id="efad5-125">指定原始伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efad5-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="efad5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efad5-126">CommonParameters</span></span>
<span data-ttu-id="efad5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efad5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efad5-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efad5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efad5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="efad5-129">INPUTS</span></span>

### <span data-ttu-id="efad5-130">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="efad5-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="efad5-131">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="efad5-131">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="efad5-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="efad5-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="efad5-133">輸出</span><span class="sxs-lookup"><span data-stu-id="efad5-133">OUTPUTS</span></span>

### <span data-ttu-id="efad5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="efad5-134">System.Boolean</span></span>

## <span data-ttu-id="efad5-135">筆記</span><span class="sxs-lookup"><span data-stu-id="efad5-135">NOTES</span></span>

## <span data-ttu-id="efad5-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="efad5-136">RELATED LINKS</span></span>

[<span data-ttu-id="efad5-137">取消發佈-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="efad5-137">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


