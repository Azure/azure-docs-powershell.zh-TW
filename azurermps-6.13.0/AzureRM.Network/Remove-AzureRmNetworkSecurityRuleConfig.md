---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: d6ca2ac1e091e3576af51ba8f1a2f50676994ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455179"
---
# <span data-ttu-id="d7bd4-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7bd4-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="d7bd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bd4-103">從網路安全性群組移除網路安全規則。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7bd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7bd4-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7bd4-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="d7bd4-106">**AzureRmNetworkSecurityRuleConfig** Cmdlet 會從 Azure 網路安全群組中移除網路安全規則設定。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="d7bd4-107">示例</span><span class="sxs-lookup"><span data-stu-id="d7bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="d7bd4-108">範例1：移除網路安全規則設定</span><span class="sxs-lookup"><span data-stu-id="d7bd4-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="d7bd4-109">第一個命令會建立名為 rdp 規則的網路安全規則配置，然後將它儲存在 $rule 1 變數中。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="d7bd4-110">第二個命令會使用 $rule 1 中的規則建立網路安全性群組，然後將網路安全性群組儲存在 $nsg 變數中。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="d7bd4-111">第三個命令會從 $nsg 的網路安全群組中移除名為 rdp 規則的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="d7bd4-112">參數</span><span class="sxs-lookup"><span data-stu-id="d7bd4-112">PARAMETERS</span></span>

### <span data-ttu-id="d7bd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bd4-113">-DefaultProfile</span></span>
<span data-ttu-id="d7bd4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7bd4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7bd4-115">-Name</span></span>
<span data-ttu-id="d7bd4-116">指定此 Cmdlet 移除的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7bd4-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7bd4-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d7bd4-118">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="d7bd4-119">此物件包含要移除的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="d7bd4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bd4-120">CommonParameters</span></span>
<span data-ttu-id="d7bd4-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bd4-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7bd4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bd4-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d7bd4-123">INPUTS</span></span>

### <span data-ttu-id="d7bd4-124">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d7bd4-124">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="d7bd4-125">參數： NetworkSecurityGroup (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d7bd4-125">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="d7bd4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d7bd4-126">OUTPUTS</span></span>

### <span data-ttu-id="d7bd4-127">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d7bd4-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d7bd4-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d7bd4-128">NOTES</span></span>

## <span data-ttu-id="d7bd4-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7bd4-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7bd4-130">附加 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7bd4-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d7bd4-131">AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7bd4-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d7bd4-132">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d7bd4-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d7bd4-133">新-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7bd4-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d7bd4-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7bd4-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


