---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970925"
---
# <span data-ttu-id="e0092-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="e0092-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="e0092-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0092-102">SYNOPSIS</span></span>
<span data-ttu-id="e0092-103">為應用程式閘道 waf 建立新的排除規則清單</span><span class="sxs-lookup"><span data-stu-id="e0092-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="e0092-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0092-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0092-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0092-105">DESCRIPTION</span></span>
<span data-ttu-id="e0092-106">**新的-AzApplicationGatewayFirewallExclusionConfig** Cmdlet 為應用程式閘道 waf 新增排除規則清單。</span><span class="sxs-lookup"><span data-stu-id="e0092-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="e0092-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0092-107">EXAMPLES</span></span>

### <span data-ttu-id="e0092-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e0092-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="e0092-109">這個命令會為名為 RequestHeaderNames 的變數及名為 [xyz] 的運算子（名為 StartsWith 及選擇器）建立新的排除規則清單設定。</span><span class="sxs-lookup"><span data-stu-id="e0092-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="e0092-110">[排除清單] 設定會儲存在 $exclusion 1。</span><span class="sxs-lookup"><span data-stu-id="e0092-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="e0092-111">參數</span><span class="sxs-lookup"><span data-stu-id="e0092-111">PARAMETERS</span></span>

### <span data-ttu-id="e0092-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0092-112">-DefaultProfile</span></span>
<span data-ttu-id="e0092-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0092-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0092-114">-運算子</span><span class="sxs-lookup"><span data-stu-id="e0092-114">-Operator</span></span>
<span data-ttu-id="e0092-115">當變數是集合時，請在選取器上操作，以指定將此排除項適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="e0092-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="e0092-116">-選取器</span><span class="sxs-lookup"><span data-stu-id="e0092-116">-Selector</span></span>
<span data-ttu-id="e0092-117">如果變數是集合，則是用來指定將此排除項適用于集合中哪些元素的運算子。</span><span class="sxs-lookup"><span data-stu-id="e0092-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="e0092-118">變數</span><span class="sxs-lookup"><span data-stu-id="e0092-118">-Variable</span></span>
<span data-ttu-id="e0092-119">要排除的變數。</span><span class="sxs-lookup"><span data-stu-id="e0092-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="e0092-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0092-120">CommonParameters</span></span>
<span data-ttu-id="e0092-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0092-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0092-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0092-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0092-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e0092-123">INPUTS</span></span>

### <span data-ttu-id="e0092-124">所有</span><span class="sxs-lookup"><span data-stu-id="e0092-124">None</span></span>

## <span data-ttu-id="e0092-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e0092-125">OUTPUTS</span></span>

### <span data-ttu-id="e0092-126">PSApplicationGatewayFirewallExclusion 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e0092-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="e0092-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e0092-127">NOTES</span></span>

## <span data-ttu-id="e0092-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0092-128">RELATED LINKS</span></span>
