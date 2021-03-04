---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a60fa0e305d05ae5d944a69705c3cb3f392b28f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912657"
---
# <span data-ttu-id="cc0f0-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc0f0-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="cc0f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="cc0f0-103">從網路安全性群組移除網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="cc0f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc0f0-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc0f0-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc0f0-105">DESCRIPTION</span></span>
<span data-ttu-id="cc0f0-106">**Remove-AzNetworkSecurityRuleConfig** Cmdlet 會從 Azure 網路安全性群組移除網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="cc0f0-107">例子</span><span class="sxs-lookup"><span data-stu-id="cc0f0-107">EXAMPLES</span></span>

### <span data-ttu-id="cc0f0-108">範例 1：移除網路安全性規則組</span><span class="sxs-lookup"><span data-stu-id="cc0f0-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="cc0f0-109">第一個命令會建立名為 rdp-rule 的網路安全性規則組，然後將它儲存在 $rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="cc0f0-110">第二個命令會使用 $rule 1 中的規則建立網路安全性群組，然後將網路安全性群組儲存在$nsg變數中。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="cc0f0-111">第三個命令會從 $nsg 中的網路安全性群組移除名為 rdp-rule 的網路安全性規則$nsg。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="cc0f0-112">第四個命令會保存變更。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-112">The forth command saves the change.</span></span>

## <span data-ttu-id="cc0f0-113">參數</span><span class="sxs-lookup"><span data-stu-id="cc0f0-113">PARAMETERS</span></span>

### <span data-ttu-id="cc0f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0f0-114">-DefaultProfile</span></span>
<span data-ttu-id="cc0f0-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc0f0-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc0f0-116">-Name</span></span>
<span data-ttu-id="cc0f0-117">指定此 Cmdlet 移除的網路安全性規則組組名稱。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc0f0-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc0f0-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cc0f0-119">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="cc0f0-120">此物件包含要移除的網路安全性規則組組。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="cc0f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0f0-121">CommonParameters</span></span>
<span data-ttu-id="cc0f0-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0f0-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cc0f0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0f0-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cc0f0-124">INPUTS</span></span>

### <span data-ttu-id="cc0f0-125">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc0f0-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cc0f0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cc0f0-126">OUTPUTS</span></span>

### <span data-ttu-id="cc0f0-127">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc0f0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cc0f0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="cc0f0-128">NOTES</span></span>

## <span data-ttu-id="cc0f0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc0f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="cc0f0-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc0f0-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cc0f0-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc0f0-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cc0f0-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc0f0-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="cc0f0-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc0f0-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cc0f0-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc0f0-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


