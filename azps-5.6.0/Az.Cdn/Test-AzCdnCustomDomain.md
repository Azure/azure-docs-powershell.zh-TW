---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: b2c061f7755c7891946bcf8ea8f3fa5cdb15439d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910754"
---
# <span data-ttu-id="be23b-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be23b-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="be23b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="be23b-102">SYNOPSIS</span></span>
<span data-ttu-id="be23b-103">檢查是否可以將自訂網域新增到端點。</span><span class="sxs-lookup"><span data-stu-id="be23b-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="be23b-104">語法</span><span class="sxs-lookup"><span data-stu-id="be23b-104">SYNTAX</span></span>

### <span data-ttu-id="be23b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be23b-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be23b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be23b-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be23b-107">描述</span><span class="sxs-lookup"><span data-stu-id="be23b-107">DESCRIPTION</span></span>
<span data-ttu-id="be23b-108">**Test-AzCdnCustomDomain Cmdlet** 會驗證 CName 的映射，以檢查是否可以將自訂網域新增到端點。</span><span class="sxs-lookup"><span data-stu-id="be23b-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="be23b-109">例子</span><span class="sxs-lookup"><span data-stu-id="be23b-109">EXAMPLES</span></span>

## <span data-ttu-id="be23b-110">參數</span><span class="sxs-lookup"><span data-stu-id="be23b-110">PARAMETERS</span></span>

### <span data-ttu-id="be23b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be23b-111">-CdnEndpoint</span></span>
<span data-ttu-id="be23b-112">指定要新增自訂網域的端點。</span><span class="sxs-lookup"><span data-stu-id="be23b-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="be23b-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="be23b-113">-CustomDomainHostName</span></span>
<span data-ttu-id="be23b-114">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="be23b-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be23b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be23b-115">-DefaultProfile</span></span>
<span data-ttu-id="be23b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="be23b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be23b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="be23b-117">-EndpointName</span></span>
<span data-ttu-id="be23b-118">指定要新增自訂網域的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="be23b-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="be23b-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="be23b-119">-ProfileName</span></span>
<span data-ttu-id="be23b-120">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="be23b-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="be23b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be23b-121">-ResourceGroupName</span></span>
<span data-ttu-id="be23b-122">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be23b-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="be23b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be23b-123">CommonParameters</span></span>
<span data-ttu-id="be23b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="be23b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be23b-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be23b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be23b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="be23b-126">INPUTS</span></span>

### <span data-ttu-id="be23b-127">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="be23b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="be23b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="be23b-128">OUTPUTS</span></span>

### <span data-ttu-id="be23b-129">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="be23b-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="be23b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="be23b-130">NOTES</span></span>

## <span data-ttu-id="be23b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="be23b-131">RELATED LINKS</span></span>

[<span data-ttu-id="be23b-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be23b-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="be23b-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be23b-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="be23b-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be23b-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


