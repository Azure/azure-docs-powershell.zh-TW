---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959286"
---
# <span data-ttu-id="dc70f-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="dc70f-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="dc70f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc70f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc70f-103">取得 Azure 防火牆原則規則集合群組</span><span class="sxs-lookup"><span data-stu-id="dc70f-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="dc70f-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc70f-104">SYNTAX</span></span>

### <span data-ttu-id="dc70f-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc70f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc70f-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc70f-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc70f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc70f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc70f-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc70f-108">DESCRIPTION</span></span>
<span data-ttu-id="dc70f-109">**AzFirewallPolicyRuleCollectionGroup** Cmdlet 會從防火牆原則取得提到的 RuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="dc70f-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="dc70f-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc70f-110">EXAMPLES</span></span>

### <span data-ttu-id="dc70f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dc70f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="dc70f-112">這個範例會在防火牆原則中取得規則 collectionGroup $fp</span><span class="sxs-lookup"><span data-stu-id="dc70f-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="dc70f-113">參數</span><span class="sxs-lookup"><span data-stu-id="dc70f-113">PARAMETERS</span></span>

### <span data-ttu-id="dc70f-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dc70f-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="dc70f-115">防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="dc70f-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc70f-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="dc70f-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="dc70f-117">防火牆原則名稱</span><span class="sxs-lookup"><span data-stu-id="dc70f-117">The Firewall policy name</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc70f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc70f-118">-DefaultProfile</span></span>
<span data-ttu-id="dc70f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc70f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc70f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc70f-120">-Name</span></span>
<span data-ttu-id="dc70f-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dc70f-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc70f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc70f-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc70f-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc70f-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc70f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc70f-124">-ResourceId</span></span>
<span data-ttu-id="dc70f-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="dc70f-125">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc70f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc70f-126">CommonParameters</span></span>
<span data-ttu-id="dc70f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc70f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc70f-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc70f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc70f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dc70f-129">INPUTS</span></span>

### <span data-ttu-id="dc70f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="dc70f-130">System.String</span></span>

### <span data-ttu-id="dc70f-131">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc70f-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="dc70f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dc70f-132">OUTPUTS</span></span>

### <span data-ttu-id="dc70f-133">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc70f-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="dc70f-134">[System.object]. IEnumerable ' 1 [PSAzureFirewall，1.12.0.0，system.object，版本 =，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="dc70f-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc70f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="dc70f-135">NOTES</span></span>

## <span data-ttu-id="dc70f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc70f-136">RELATED LINKS</span></span>
