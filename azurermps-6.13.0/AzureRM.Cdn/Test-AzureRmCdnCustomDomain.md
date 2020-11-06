---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e249331f70e0ef0b7e1397f514363787e9dcf0dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452835"
---
# <span data-ttu-id="fdfac-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fdfac-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="fdfac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdfac-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfac-103">檢查是否可以將自訂網域新增到端點。</span><span class="sxs-lookup"><span data-stu-id="fdfac-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdfac-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdfac-104">SYNTAX</span></span>

### <span data-ttu-id="fdfac-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fdfac-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdfac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfac-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdfac-107">說明</span><span class="sxs-lookup"><span data-stu-id="fdfac-107">DESCRIPTION</span></span>
<span data-ttu-id="fdfac-108">**AzureRmCdnCustomDomain** Cmdlet 會驗證 CName 對應，以檢查是否可以將自訂網域新增至端點。</span><span class="sxs-lookup"><span data-stu-id="fdfac-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="fdfac-109">示例</span><span class="sxs-lookup"><span data-stu-id="fdfac-109">EXAMPLES</span></span>

## <span data-ttu-id="fdfac-110">參數</span><span class="sxs-lookup"><span data-stu-id="fdfac-110">PARAMETERS</span></span>

### <span data-ttu-id="fdfac-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fdfac-111">-CdnEndpoint</span></span>
<span data-ttu-id="fdfac-112">指定您要新增自訂網域的終點。</span><span class="sxs-lookup"><span data-stu-id="fdfac-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="fdfac-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="fdfac-113">-CustomDomainHostName</span></span>
<span data-ttu-id="fdfac-114">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="fdfac-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="fdfac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfac-115">-DefaultProfile</span></span>
<span data-ttu-id="fdfac-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fdfac-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdfac-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="fdfac-117">-EndpointName</span></span>
<span data-ttu-id="fdfac-118">指定您要新增自訂網域之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdfac-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="fdfac-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fdfac-119">-ProfileName</span></span>
<span data-ttu-id="fdfac-120">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdfac-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fdfac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfac-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdfac-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdfac-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fdfac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfac-123">CommonParameters</span></span>
<span data-ttu-id="fdfac-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdfac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfac-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdfac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfac-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fdfac-126">INPUTS</span></span>

### <span data-ttu-id="fdfac-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="fdfac-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="fdfac-128">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fdfac-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="fdfac-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fdfac-129">OUTPUTS</span></span>

### <span data-ttu-id="fdfac-130">[PSValidateCustomDomainOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="fdfac-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="fdfac-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fdfac-131">NOTES</span></span>

## <span data-ttu-id="fdfac-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdfac-132">RELATED LINKS</span></span>

[<span data-ttu-id="fdfac-133">AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fdfac-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="fdfac-134">新-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fdfac-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="fdfac-135">移除-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fdfac-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


