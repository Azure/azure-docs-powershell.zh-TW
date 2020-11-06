---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: 0912ba8913bae430c3878dc0bde578420a5ea429
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445696"
---
# <span data-ttu-id="01b6f-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="01b6f-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="01b6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="01b6f-103">取得 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="01b6f-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01b6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="01b6f-104">SYNTAX</span></span>

### <span data-ttu-id="01b6f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="01b6f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b6f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b6f-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01b6f-107">說明</span><span class="sxs-lookup"><span data-stu-id="01b6f-107">DESCRIPTION</span></span>
<span data-ttu-id="01b6f-108">**AzureRmCdnOrigin** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 來源伺服器及其設定資料。</span><span class="sxs-lookup"><span data-stu-id="01b6f-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="01b6f-109">示例</span><span class="sxs-lookup"><span data-stu-id="01b6f-109">EXAMPLES</span></span>

## <span data-ttu-id="01b6f-110">參數</span><span class="sxs-lookup"><span data-stu-id="01b6f-110">PARAMETERS</span></span>

### <span data-ttu-id="01b6f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01b6f-111">-CdnEndpoint</span></span>
<span data-ttu-id="01b6f-112">指定原始所歸屬的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="01b6f-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="01b6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b6f-113">-DefaultProfile</span></span>
<span data-ttu-id="01b6f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="01b6f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01b6f-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="01b6f-115">-EndpointName</span></span>
<span data-ttu-id="01b6f-116">指定原始伺服器所屬端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="01b6f-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="01b6f-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="01b6f-117">-OriginName</span></span>
<span data-ttu-id="01b6f-118">指定原始伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="01b6f-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="01b6f-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="01b6f-119">-ProfileName</span></span>
<span data-ttu-id="01b6f-120">指定原始伺服器所屬之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="01b6f-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="01b6f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b6f-121">-ResourceGroupName</span></span>
<span data-ttu-id="01b6f-122">指定原始伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="01b6f-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="01b6f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b6f-123">CommonParameters</span></span>
<span data-ttu-id="01b6f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01b6f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b6f-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01b6f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b6f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="01b6f-126">INPUTS</span></span>

### <span data-ttu-id="01b6f-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="01b6f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="01b6f-128">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="01b6f-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="01b6f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="01b6f-129">OUTPUTS</span></span>

### <span data-ttu-id="01b6f-130">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="01b6f-130">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="01b6f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="01b6f-131">NOTES</span></span>

## <span data-ttu-id="01b6f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="01b6f-132">RELATED LINKS</span></span>

[<span data-ttu-id="01b6f-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="01b6f-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


