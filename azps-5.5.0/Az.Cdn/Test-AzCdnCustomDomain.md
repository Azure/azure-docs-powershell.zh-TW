---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136586"
---
# <span data-ttu-id="05d62-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="05d62-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="05d62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05d62-102">SYNOPSIS</span></span>
<span data-ttu-id="05d62-103">檢查是否可以將自訂網域新增到端點。</span><span class="sxs-lookup"><span data-stu-id="05d62-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="05d62-104">句法</span><span class="sxs-lookup"><span data-stu-id="05d62-104">SYNTAX</span></span>

### <span data-ttu-id="05d62-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="05d62-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d62-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05d62-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05d62-107">說明</span><span class="sxs-lookup"><span data-stu-id="05d62-107">DESCRIPTION</span></span>
<span data-ttu-id="05d62-108">**AzCdnCustomDomain** Cmdlet 會驗證 CName 對應，以檢查是否可以將自訂網域新增至端點。</span><span class="sxs-lookup"><span data-stu-id="05d62-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="05d62-109">示例</span><span class="sxs-lookup"><span data-stu-id="05d62-109">EXAMPLES</span></span>

## <span data-ttu-id="05d62-110">參數</span><span class="sxs-lookup"><span data-stu-id="05d62-110">PARAMETERS</span></span>

### <span data-ttu-id="05d62-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="05d62-111">-CdnEndpoint</span></span>
<span data-ttu-id="05d62-112">指定您要新增自訂網域的終點。</span><span class="sxs-lookup"><span data-stu-id="05d62-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="05d62-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="05d62-113">-CustomDomainHostName</span></span>
<span data-ttu-id="05d62-114">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="05d62-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="05d62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d62-115">-DefaultProfile</span></span>
<span data-ttu-id="05d62-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="05d62-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05d62-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="05d62-117">-EndpointName</span></span>
<span data-ttu-id="05d62-118">指定您要新增自訂網域之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="05d62-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="05d62-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="05d62-119">-ProfileName</span></span>
<span data-ttu-id="05d62-120">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="05d62-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="05d62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d62-121">-ResourceGroupName</span></span>
<span data-ttu-id="05d62-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05d62-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="05d62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d62-123">CommonParameters</span></span>
<span data-ttu-id="05d62-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05d62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d62-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="05d62-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d62-126">輸入</span><span class="sxs-lookup"><span data-stu-id="05d62-126">INPUTS</span></span>

### <span data-ttu-id="05d62-127">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="05d62-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="05d62-128">輸出</span><span class="sxs-lookup"><span data-stu-id="05d62-128">OUTPUTS</span></span>

### <span data-ttu-id="05d62-129">[PSValidateCustomDomainOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="05d62-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="05d62-130">筆記</span><span class="sxs-lookup"><span data-stu-id="05d62-130">NOTES</span></span>

## <span data-ttu-id="05d62-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="05d62-131">RELATED LINKS</span></span>

[<span data-ttu-id="05d62-132">AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="05d62-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="05d62-133">新-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="05d62-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="05d62-134">移除-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="05d62-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


