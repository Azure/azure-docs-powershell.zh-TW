---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 7f5d41774af2f5ee74c5d343fa9b143801c139f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965457"
---
# <span data-ttu-id="b9990-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9990-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b9990-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9990-102">SYNOPSIS</span></span>
<span data-ttu-id="b9990-103">從網路安全性群組移除網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="b9990-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="b9990-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9990-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9990-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9990-105">DESCRIPTION</span></span>
<span data-ttu-id="b9990-106">**AzNetworkSecurityRuleConfig** Cmdlet 會從 Azure 網路安全群組中移除網路安全規則設定。</span><span class="sxs-lookup"><span data-stu-id="b9990-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="b9990-107">示例</span><span class="sxs-lookup"><span data-stu-id="b9990-107">EXAMPLES</span></span>

### <span data-ttu-id="b9990-108">範例1：移除網路安全規則設定</span><span class="sxs-lookup"><span data-stu-id="b9990-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="b9990-109">第一個命令會建立名為 rdp 規則的網路安全規則配置，然後將它儲存在 $rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="b9990-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="b9990-110">第二個命令會使用 $rule 1 中的規則建立網路安全性群組，然後將網路安全性群組儲存在 $nsg 變數中。</span><span class="sxs-lookup"><span data-stu-id="b9990-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="b9990-111">第三個命令會從 $nsg 的網路安全群組中移除名為 rdp 規則的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="b9990-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="b9990-112">第四個命令會儲存變更。</span><span class="sxs-lookup"><span data-stu-id="b9990-112">The forth command saves the change.</span></span>

## <span data-ttu-id="b9990-113">參數</span><span class="sxs-lookup"><span data-stu-id="b9990-113">PARAMETERS</span></span>

### <span data-ttu-id="b9990-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9990-114">-DefaultProfile</span></span>
<span data-ttu-id="b9990-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9990-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9990-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9990-116">-Name</span></span>
<span data-ttu-id="b9990-117">指定此 Cmdlet 移除的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b9990-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9990-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9990-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b9990-119">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="b9990-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b9990-120">此物件包含要移除的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="b9990-120">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9990-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9990-121">CommonParameters</span></span>
<span data-ttu-id="b9990-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9990-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9990-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9990-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9990-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b9990-124">INPUTS</span></span>

### <span data-ttu-id="b9990-125">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b9990-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b9990-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b9990-126">OUTPUTS</span></span>

### <span data-ttu-id="b9990-127">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b9990-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b9990-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b9990-128">NOTES</span></span>

## <span data-ttu-id="b9990-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9990-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9990-130">附加 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9990-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9990-131">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9990-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9990-132">新-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9990-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="b9990-133">新-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9990-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9990-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9990-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


