---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 6ea379b1ad1629dc0ba3e7d747256c86153c651d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456488"
---
# <span data-ttu-id="7655c-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="7655c-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="7655c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7655c-102">SYNOPSIS</span></span>
<span data-ttu-id="7655c-103">建立新的已停用規則群組設定。</span><span class="sxs-lookup"><span data-stu-id="7655c-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7655c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7655c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7655c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7655c-105">DESCRIPTION</span></span>
<span data-ttu-id="7655c-106">**新的-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** Cmdlet 會建立新的停用規則群組設定。</span><span class="sxs-lookup"><span data-stu-id="7655c-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="7655c-107">示例</span><span class="sxs-lookup"><span data-stu-id="7655c-107">EXAMPLES</span></span>

### <span data-ttu-id="7655c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7655c-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="7655c-109">此命令會針對名為「要求-942-應用程式-SQLI」的規則群組建立新的停用規則群組設定，並停用規則942130與規則942140。</span><span class="sxs-lookup"><span data-stu-id="7655c-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="7655c-110">新的停用規則群組設定會儲存在 $disabledRuleGroup 1。</span><span class="sxs-lookup"><span data-stu-id="7655c-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="7655c-111">參數</span><span class="sxs-lookup"><span data-stu-id="7655c-111">PARAMETERS</span></span>

### <span data-ttu-id="7655c-112">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="7655c-112">-RuleGroupName</span></span>
<span data-ttu-id="7655c-113">將停用之規則群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7655c-113">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="7655c-114">-規則</span><span class="sxs-lookup"><span data-stu-id="7655c-114">-Rules</span></span>
<span data-ttu-id="7655c-115">將停用的規則清單。</span><span class="sxs-lookup"><span data-stu-id="7655c-115">The list of rules that will be disabled.</span></span>
<span data-ttu-id="7655c-116">如果是 null，則會停用規則群組的所有規則。</span><span class="sxs-lookup"><span data-stu-id="7655c-116">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7655c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7655c-117">-DefaultProfile</span></span>
<span data-ttu-id="7655c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7655c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7655c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7655c-119">CommonParameters</span></span>
<span data-ttu-id="7655c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7655c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7655c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7655c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7655c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7655c-122">INPUTS</span></span>

### <span data-ttu-id="7655c-123">所有</span><span class="sxs-lookup"><span data-stu-id="7655c-123">None</span></span>

## <span data-ttu-id="7655c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7655c-124">OUTPUTS</span></span>

### <span data-ttu-id="7655c-125">PSApplicationGatewayFirewallDisabledRuleGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7655c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="7655c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7655c-126">NOTES</span></span>

## <span data-ttu-id="7655c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7655c-127">RELATED LINKS</span></span>

[<span data-ttu-id="7655c-128">新-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7655c-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7655c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7655c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

