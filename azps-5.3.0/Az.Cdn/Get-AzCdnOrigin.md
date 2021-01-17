---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449945"
---
# <span data-ttu-id="fbd27-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fbd27-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="fbd27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbd27-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd27-103">取得 CDN 來源伺服器。</span><span class="sxs-lookup"><span data-stu-id="fbd27-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="fbd27-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbd27-104">SYNTAX</span></span>

### <span data-ttu-id="fbd27-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fbd27-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbd27-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbd27-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbd27-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbd27-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbd27-108">說明</span><span class="sxs-lookup"><span data-stu-id="fbd27-108">DESCRIPTION</span></span>
<span data-ttu-id="fbd27-109">**AzCdnOrigin** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 來源伺服器及其設定資料。</span><span class="sxs-lookup"><span data-stu-id="fbd27-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="fbd27-110">示例</span><span class="sxs-lookup"><span data-stu-id="fbd27-110">EXAMPLES</span></span>

## <span data-ttu-id="fbd27-111">參數</span><span class="sxs-lookup"><span data-stu-id="fbd27-111">PARAMETERS</span></span>

### <span data-ttu-id="fbd27-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbd27-112">-CdnEndpoint</span></span>
<span data-ttu-id="fbd27-113">指定原始所歸屬的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="fbd27-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="fbd27-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd27-114">-DefaultProfile</span></span>
<span data-ttu-id="fbd27-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fbd27-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbd27-116">-終結點</span><span class="sxs-lookup"><span data-stu-id="fbd27-116">-EndpointName</span></span>
<span data-ttu-id="fbd27-117">指定原始伺服器所屬端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbd27-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="fbd27-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="fbd27-118">-OriginName</span></span>
<span data-ttu-id="fbd27-119">指定原始伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbd27-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="fbd27-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fbd27-120">-ProfileName</span></span>
<span data-ttu-id="fbd27-121">指定原始伺服器所屬之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbd27-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="fbd27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd27-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbd27-123">指定原始伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbd27-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="fbd27-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbd27-124">-ResourceId</span></span>
<span data-ttu-id="fbd27-125">Azure CDN 來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbd27-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="fbd27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd27-126">CommonParameters</span></span>
<span data-ttu-id="fbd27-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbd27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd27-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fbd27-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd27-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fbd27-129">INPUTS</span></span>

### <span data-ttu-id="fbd27-130">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="fbd27-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="fbd27-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fbd27-131">OUTPUTS</span></span>

### <span data-ttu-id="fbd27-132">PSOrigin 中的 [Microsoft.]</span><span class="sxs-lookup"><span data-stu-id="fbd27-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="fbd27-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fbd27-133">NOTES</span></span>

## <span data-ttu-id="fbd27-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbd27-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbd27-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fbd27-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


