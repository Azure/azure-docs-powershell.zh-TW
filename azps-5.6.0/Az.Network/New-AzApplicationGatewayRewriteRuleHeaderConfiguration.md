---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: 6d5bbd0cd0b5581e129e63e7559c09751d8f91cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903121"
---
# <span data-ttu-id="91f1f-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="91f1f-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="91f1f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="91f1f-103">為應用程式閘道建立重寫規則標題組組。</span><span class="sxs-lookup"><span data-stu-id="91f1f-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="91f1f-104">語法</span><span class="sxs-lookup"><span data-stu-id="91f1f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91f1f-105">描述</span><span class="sxs-lookup"><span data-stu-id="91f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="91f1f-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration** Cmdlet 會為 Azure 應用程式閘道建立重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="91f1f-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="91f1f-107">例子</span><span class="sxs-lookup"><span data-stu-id="91f1f-107">EXAMPLES</span></span>

### <span data-ttu-id="91f1f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="91f1f-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="91f1f-109">此命令會建立重寫規則標題組組，並儲存在名為 $hc 的變數中。</span><span class="sxs-lookup"><span data-stu-id="91f1f-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="91f1f-110">參數</span><span class="sxs-lookup"><span data-stu-id="91f1f-110">PARAMETERS</span></span>

### <span data-ttu-id="91f1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f1f-111">-DefaultProfile</span></span>
<span data-ttu-id="91f1f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="91f1f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f1f-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="91f1f-113">-HeaderName</span></span>
<span data-ttu-id="91f1f-114">要重寫的頁眉名稱</span><span class="sxs-lookup"><span data-stu-id="91f1f-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="91f1f-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="91f1f-115">-HeaderValue</span></span>
<span data-ttu-id="91f1f-116">指定標題名稱的集標題值。</span><span class="sxs-lookup"><span data-stu-id="91f1f-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="91f1f-117">如果省略此選項，標題將會刪除</span><span class="sxs-lookup"><span data-stu-id="91f1f-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="91f1f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f1f-118">CommonParameters</span></span>
<span data-ttu-id="91f1f-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91f1f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f1f-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="91f1f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f1f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="91f1f-121">INPUTS</span></span>

### <span data-ttu-id="91f1f-122">沒有</span><span class="sxs-lookup"><span data-stu-id="91f1f-122">None</span></span>

## <span data-ttu-id="91f1f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="91f1f-123">OUTPUTS</span></span>

### <span data-ttu-id="91f1f-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="91f1f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="91f1f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="91f1f-125">NOTES</span></span>

## <span data-ttu-id="91f1f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="91f1f-126">RELATED LINKS</span></span>

[<span data-ttu-id="91f1f-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="91f1f-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="91f1f-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="91f1f-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="91f1f-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="91f1f-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="91f1f-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="91f1f-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="91f1f-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="91f1f-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="91f1f-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="91f1f-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="91f1f-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="91f1f-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
