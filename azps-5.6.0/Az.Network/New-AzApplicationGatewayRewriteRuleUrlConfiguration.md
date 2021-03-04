---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: e9b0b8cdbee1e4d5c488e51f537d18cca2ef681a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901969"
---
# <span data-ttu-id="fe9cf-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe9cf-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="fe9cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fe9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9cf-103">為應用程式閘道建立重寫規則 URL 組組。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="fe9cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="fe9cf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe9cf-105">描述</span><span class="sxs-lookup"><span data-stu-id="fe9cf-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9cf-106">**AzApplicationGatewayRewriteRuleUrlConfiguration** Cmdlet 會為 Azure 應用程式閘道建立重寫規則 URL 組。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="fe9cf-107">例子</span><span class="sxs-lookup"><span data-stu-id="fe9cf-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9cf-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fe9cf-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="fe9cf-109">此命令會建立重寫規則 URL 組組，並儲存在名為 $urlConfiguration 的變數中。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="fe9cf-110">如果您想要更新任何現有的 UrlConfiguration，您可以建立新 UrlConfiguration，並將新的 UrlConfiguration 指派給重寫規則動作集的 UrlConfiguration 屬性來執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="fe9cf-111">參數</span><span class="sxs-lookup"><span data-stu-id="fe9cf-111">PARAMETERS</span></span>

### <span data-ttu-id="fe9cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9cf-112">-DefaultProfile</span></span>
<span data-ttu-id="fe9cf-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe9cf-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="fe9cf-114">-ModifiedPath</span></span>
<span data-ttu-id="fe9cf-115">URL 路徑值。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-115">Url path value.</span></span>

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

### <span data-ttu-id="fe9cf-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="fe9cf-116">-ModifiedQueryString</span></span>
<span data-ttu-id="fe9cf-117">Url 查詢字串值。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-117">Url query string value.</span></span>

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

### <span data-ttu-id="fe9cf-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="fe9cf-118">-Reroute</span></span>
<span data-ttu-id="fe9cf-119">標出以使用修改路徑重新評估路徑要求路由規則中提供的 URL 路徑地圖。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9cf-120">CommonParameters</span></span>
<span data-ttu-id="fe9cf-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fe9cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9cf-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe9cf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9cf-123">輸入</span><span class="sxs-lookup"><span data-stu-id="fe9cf-123">INPUTS</span></span>

### <span data-ttu-id="fe9cf-124">沒有</span><span class="sxs-lookup"><span data-stu-id="fe9cf-124">None</span></span>

## <span data-ttu-id="fe9cf-125">輸出</span><span class="sxs-lookup"><span data-stu-id="fe9cf-125">OUTPUTS</span></span>

### <span data-ttu-id="fe9cf-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe9cf-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="fe9cf-127">筆記</span><span class="sxs-lookup"><span data-stu-id="fe9cf-127">NOTES</span></span>

## <span data-ttu-id="fe9cf-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe9cf-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe9cf-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe9cf-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe9cf-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe9cf-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe9cf-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe9cf-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe9cf-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe9cf-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe9cf-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe9cf-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe9cf-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fe9cf-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="fe9cf-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fe9cf-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)