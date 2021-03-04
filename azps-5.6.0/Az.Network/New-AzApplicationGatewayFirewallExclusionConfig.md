---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 029ba60169ee22d86d9e54661296f04bf2242713
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904973"
---
# <span data-ttu-id="6ac63-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="6ac63-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="6ac63-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ac63-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac63-103">為應用程式閘道 waf 建立新的排除規則清單</span><span class="sxs-lookup"><span data-stu-id="6ac63-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="6ac63-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ac63-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac63-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ac63-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac63-106">**New-AzApplicationGatewayFirewallExclusionConfig** Cmdlet 應用程式閘道 waf 的新排除規則清單。</span><span class="sxs-lookup"><span data-stu-id="6ac63-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="6ac63-107">例子</span><span class="sxs-lookup"><span data-stu-id="6ac63-107">EXAMPLES</span></span>

### <span data-ttu-id="6ac63-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6ac63-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="6ac63-109">此命令會針對名為 RequestHeaderNames 的變數和名為 StartsWith 和選擇器且名為 xyz 的運算子，建立一個新的排除規則清單組。</span><span class="sxs-lookup"><span data-stu-id="6ac63-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="6ac63-110">排除清單組會儲存于 $exclusion 1。</span><span class="sxs-lookup"><span data-stu-id="6ac63-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="6ac63-111">參數</span><span class="sxs-lookup"><span data-stu-id="6ac63-111">PARAMETERS</span></span>

### <span data-ttu-id="6ac63-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac63-112">-DefaultProfile</span></span>
<span data-ttu-id="6ac63-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ac63-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ac63-114">-運算子</span><span class="sxs-lookup"><span data-stu-id="6ac63-114">-Operator</span></span>
<span data-ttu-id="6ac63-115">當變數是集合時，請于選取器上操作，以指定此排除專案適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="6ac63-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="6ac63-116">-選取器</span><span class="sxs-lookup"><span data-stu-id="6ac63-116">-Selector</span></span>
<span data-ttu-id="6ac63-117">當變數是集合時，運算子會用來指定此排除範圍適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="6ac63-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="6ac63-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="6ac63-118">-Variable</span></span>
<span data-ttu-id="6ac63-119">要排除的變數。</span><span class="sxs-lookup"><span data-stu-id="6ac63-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="6ac63-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac63-120">CommonParameters</span></span>
<span data-ttu-id="6ac63-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ac63-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac63-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6ac63-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac63-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6ac63-123">INPUTS</span></span>

### <span data-ttu-id="6ac63-124">沒有</span><span class="sxs-lookup"><span data-stu-id="6ac63-124">None</span></span>

## <span data-ttu-id="6ac63-125">輸出</span><span class="sxs-lookup"><span data-stu-id="6ac63-125">OUTPUTS</span></span>

### <span data-ttu-id="6ac63-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="6ac63-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="6ac63-127">筆記</span><span class="sxs-lookup"><span data-stu-id="6ac63-127">NOTES</span></span>

## <span data-ttu-id="6ac63-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ac63-128">RELATED LINKS</span></span>
