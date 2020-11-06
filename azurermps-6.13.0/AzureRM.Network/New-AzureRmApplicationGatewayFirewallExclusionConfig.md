---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450239"
---
# <span data-ttu-id="2abb3-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="2abb3-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="2abb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2abb3-102">SYNOPSIS</span></span>
<span data-ttu-id="2abb3-103">為應用程式閘道 waf 建立新的排除規則清單</span><span class="sxs-lookup"><span data-stu-id="2abb3-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2abb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="2abb3-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2abb3-105">說明</span><span class="sxs-lookup"><span data-stu-id="2abb3-105">DESCRIPTION</span></span>
<span data-ttu-id="2abb3-106">**新的-AzureRmApplicationGatewayFirewallExclusionConfig** Cmdlet 為應用程式閘道 waf 新增排除規則清單。</span><span class="sxs-lookup"><span data-stu-id="2abb3-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="2abb3-107">示例</span><span class="sxs-lookup"><span data-stu-id="2abb3-107">EXAMPLES</span></span>

### <span data-ttu-id="2abb3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2abb3-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="2abb3-109">這個命令會為名為 RequestHeaderNames 的變數及名為 [xyz] 的運算子（名為 StartsWith 及選擇器）建立新的排除規則清單設定。</span><span class="sxs-lookup"><span data-stu-id="2abb3-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="2abb3-110">[排除清單] 設定會儲存在 $exclusion 1。</span><span class="sxs-lookup"><span data-stu-id="2abb3-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="2abb3-111">參數</span><span class="sxs-lookup"><span data-stu-id="2abb3-111">PARAMETERS</span></span>

### <span data-ttu-id="2abb3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abb3-112">-DefaultProfile</span></span>
<span data-ttu-id="2abb3-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2abb3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2abb3-114">-運算子</span><span class="sxs-lookup"><span data-stu-id="2abb3-114">-Operator</span></span>
<span data-ttu-id="2abb3-115">當變數是集合時，請在選取器上操作，以指定將此排除項適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="2abb3-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="2abb3-116">-選取器</span><span class="sxs-lookup"><span data-stu-id="2abb3-116">-Selector</span></span>
<span data-ttu-id="2abb3-117">如果變數是集合，則是用來指定將此排除項適用于集合中哪些元素的運算子。</span><span class="sxs-lookup"><span data-stu-id="2abb3-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="2abb3-118">變數</span><span class="sxs-lookup"><span data-stu-id="2abb3-118">-Variable</span></span>
<span data-ttu-id="2abb3-119">要排除的變數。</span><span class="sxs-lookup"><span data-stu-id="2abb3-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="2abb3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abb3-120">CommonParameters</span></span>
<span data-ttu-id="2abb3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2abb3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abb3-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2abb3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abb3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2abb3-123">INPUTS</span></span>

### <span data-ttu-id="2abb3-124">所有</span><span class="sxs-lookup"><span data-stu-id="2abb3-124">None</span></span>

## <span data-ttu-id="2abb3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2abb3-125">OUTPUTS</span></span>

### <span data-ttu-id="2abb3-126">PSApplicationGatewayFirewallExclusion 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2abb3-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="2abb3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2abb3-127">NOTES</span></span>

## <span data-ttu-id="2abb3-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2abb3-128">RELATED LINKS</span></span>
