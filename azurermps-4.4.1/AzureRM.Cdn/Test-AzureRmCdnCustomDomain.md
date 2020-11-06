---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450005"
---
# <span data-ttu-id="adbb6-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="adbb6-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="adbb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="adbb6-103">檢查是否可以將自訂網域新增到端點。</span><span class="sxs-lookup"><span data-stu-id="adbb6-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adbb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="adbb6-104">SYNTAX</span></span>

### <span data-ttu-id="adbb6-105">預設)  (欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="adbb6-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adbb6-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="adbb6-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adbb6-107">說明</span><span class="sxs-lookup"><span data-stu-id="adbb6-107">DESCRIPTION</span></span>
<span data-ttu-id="adbb6-108">**AzureRmCdnCustomDomain** Cmdlet 會驗證 CName 對應，以檢查是否可以將自訂網域新增至端點。</span><span class="sxs-lookup"><span data-stu-id="adbb6-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="adbb6-109">示例</span><span class="sxs-lookup"><span data-stu-id="adbb6-109">EXAMPLES</span></span>

## <span data-ttu-id="adbb6-110">參數</span><span class="sxs-lookup"><span data-stu-id="adbb6-110">PARAMETERS</span></span>

### <span data-ttu-id="adbb6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="adbb6-111">-CdnEndpoint</span></span>
<span data-ttu-id="adbb6-112">指定您要新增自訂網域的終點。</span><span class="sxs-lookup"><span data-stu-id="adbb6-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="adbb6-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="adbb6-113">-CustomDomainHostName</span></span>
<span data-ttu-id="adbb6-114">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="adbb6-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="adbb6-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="adbb6-115">-EndpointName</span></span>
<span data-ttu-id="adbb6-116">指定您要新增自訂網域之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="adbb6-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="adbb6-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="adbb6-117">-ProfileName</span></span>
<span data-ttu-id="adbb6-118">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="adbb6-118">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="adbb6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbb6-119">-ResourceGroupName</span></span>
<span data-ttu-id="adbb6-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="adbb6-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="adbb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbb6-121">-DefaultProfile</span></span>
<span data-ttu-id="adbb6-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="adbb6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adbb6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbb6-123">CommonParameters</span></span>
<span data-ttu-id="adbb6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adbb6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbb6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="adbb6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbb6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="adbb6-126">INPUTS</span></span>

### <span data-ttu-id="adbb6-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="adbb6-127">PSEndpoint</span></span>
<span data-ttu-id="adbb6-128">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="adbb6-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="adbb6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="adbb6-129">OUTPUTS</span></span>

### <span data-ttu-id="adbb6-130">[PSValidateCustomDomainOutput] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="adbb6-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="adbb6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="adbb6-131">NOTES</span></span>

## <span data-ttu-id="adbb6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="adbb6-132">RELATED LINKS</span></span>

[<span data-ttu-id="adbb6-133">AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="adbb6-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="adbb6-134">新-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="adbb6-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="adbb6-135">移除-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="adbb6-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


