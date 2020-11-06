---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: dcfa0968ac70f7a0abc14ee61ee615bee3aee5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452584"
---
# <span data-ttu-id="77b37-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="77b37-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="77b37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77b37-102">SYNOPSIS</span></span>
<span data-ttu-id="77b37-103">取得 CDN 自訂網域。</span><span class="sxs-lookup"><span data-stu-id="77b37-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b37-104">句法</span><span class="sxs-lookup"><span data-stu-id="77b37-104">SYNTAX</span></span>

### <span data-ttu-id="77b37-105">預設)  (欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="77b37-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b37-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="77b37-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77b37-107">說明</span><span class="sxs-lookup"><span data-stu-id="77b37-107">DESCRIPTION</span></span>
<span data-ttu-id="77b37-108">**AzureRmCdnCustomDomain** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 自訂網域及其相關設定。</span><span class="sxs-lookup"><span data-stu-id="77b37-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="77b37-109">示例</span><span class="sxs-lookup"><span data-stu-id="77b37-109">EXAMPLES</span></span>

## <span data-ttu-id="77b37-110">參數</span><span class="sxs-lookup"><span data-stu-id="77b37-110">PARAMETERS</span></span>

### <span data-ttu-id="77b37-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="77b37-111">-CdnEndpoint</span></span>
<span data-ttu-id="77b37-112">指定自訂網域是其成員的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="77b37-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77b37-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="77b37-113">-CustomDomainName</span></span>
<span data-ttu-id="77b37-114">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="77b37-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="77b37-115">自訂網域的名稱與自訂網域的主機名稱不同。</span><span class="sxs-lookup"><span data-stu-id="77b37-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="77b37-116">-終結點</span><span class="sxs-lookup"><span data-stu-id="77b37-116">-EndpointName</span></span>
<span data-ttu-id="77b37-117">指定自訂網域所屬之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="77b37-117">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b37-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="77b37-118">-ProfileName</span></span>
<span data-ttu-id="77b37-119">指定自訂網域所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="77b37-119">Specifies the name of the Profile to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b37-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b37-120">-ResourceGroupName</span></span>
<span data-ttu-id="77b37-121">指定自訂網域所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77b37-121">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b37-122">-DefaultProfile</span></span>
<span data-ttu-id="77b37-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77b37-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77b37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b37-124">CommonParameters</span></span>
<span data-ttu-id="77b37-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77b37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b37-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77b37-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b37-127">輸入</span><span class="sxs-lookup"><span data-stu-id="77b37-127">INPUTS</span></span>

### <span data-ttu-id="77b37-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="77b37-128">PSEndpoint</span></span>
<span data-ttu-id="77b37-129">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="77b37-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="77b37-130">輸出</span><span class="sxs-lookup"><span data-stu-id="77b37-130">OUTPUTS</span></span>

###  
<span data-ttu-id="77b37-131">這個 Cmdlet 會傳回自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="77b37-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="77b37-132">筆記</span><span class="sxs-lookup"><span data-stu-id="77b37-132">NOTES</span></span>

## <span data-ttu-id="77b37-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="77b37-133">RELATED LINKS</span></span>

[<span data-ttu-id="77b37-134">新-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="77b37-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="77b37-135">移除-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="77b37-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


