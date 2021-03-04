---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 91144275806c5e3a6913d39990ad68644c71b244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915281"
---
# <span data-ttu-id="53f2b-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="53f2b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="53f2b-103">更新網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="53f2b-103">Updates a network security group.</span></span>

## <span data-ttu-id="53f2b-104">語法</span><span class="sxs-lookup"><span data-stu-id="53f2b-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53f2b-105">描述</span><span class="sxs-lookup"><span data-stu-id="53f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="53f2b-106">**Set-AzNetworkSecurityGroup** Cmdlet 會更新網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="53f2b-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="53f2b-107">例子</span><span class="sxs-lookup"><span data-stu-id="53f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="53f2b-108">範例 1：更新現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="53f2b-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="53f2b-109">此命令會獲得名為 Nsg1 的 Azure 網路安全性群組，並新增名為 Rdp-Rule 的網路安全性規則，以允許埠 3389 上的網際網路流量使用 Add-AzNetworkSecurityRuleConfig 將網際網路流量新增到已取取的網路安全性群組物件。</span><span class="sxs-lookup"><span data-stu-id="53f2b-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="53f2b-110">此命令會持續使用 **Set-AzNetworkSecurityGroup** 修改過的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="53f2b-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="53f2b-111">參數</span><span class="sxs-lookup"><span data-stu-id="53f2b-111">PARAMETERS</span></span>

### <span data-ttu-id="53f2b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53f2b-112">-AsJob</span></span>
<span data-ttu-id="53f2b-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f2b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53f2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f2b-114">-DefaultProfile</span></span>
<span data-ttu-id="53f2b-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53f2b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53f2b-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="53f2b-117">指定代表網路安全性群組應設定之狀態的網路安全性群組物件。</span><span class="sxs-lookup"><span data-stu-id="53f2b-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="53f2b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="53f2b-118">-Confirm</span></span>
<span data-ttu-id="53f2b-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="53f2b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f2b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f2b-120">-WhatIf</span></span>
<span data-ttu-id="53f2b-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53f2b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53f2b-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53f2b-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f2b-123">CommonParameters</span></span>
<span data-ttu-id="53f2b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53f2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f2b-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="53f2b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f2b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="53f2b-126">INPUTS</span></span>

### <span data-ttu-id="53f2b-127">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="53f2b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="53f2b-128">OUTPUTS</span></span>

### <span data-ttu-id="53f2b-129">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="53f2b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="53f2b-130">NOTES</span></span>

## <span data-ttu-id="53f2b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="53f2b-131">RELATED LINKS</span></span>

[<span data-ttu-id="53f2b-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="53f2b-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="53f2b-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53f2b-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


