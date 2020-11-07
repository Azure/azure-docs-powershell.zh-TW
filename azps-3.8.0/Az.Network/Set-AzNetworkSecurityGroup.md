---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958426"
---
# <span data-ttu-id="e5f1c-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5f1c-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e5f1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f1c-103">更新網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-103">Updates a network security group.</span></span>

## <span data-ttu-id="e5f1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5f1c-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f1c-106">**AzNetworkSecurityGroup** Cmdlet 會更新網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="e5f1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5f1c-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f1c-108">範例1：更新現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="e5f1c-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="e5f1c-109">這個命令會取得名為 Nsg1 的 Azure 網路安全性群組，並將名為 Rdp-Rule 的網路安全規則，新增到使用 AzNetworkSecurityRuleConfig 的 [允許埠3389上的網際網路流量]。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="e5f1c-110">此命令會使用 **設定 AzNetworkSecurityGroup** ，將已修改的 Azure 網路安全性群組保持不變。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="e5f1c-111">參數</span><span class="sxs-lookup"><span data-stu-id="e5f1c-111">PARAMETERS</span></span>

### <span data-ttu-id="e5f1c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5f1c-112">-AsJob</span></span>
<span data-ttu-id="e5f1c-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5f1c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5f1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f1c-114">-DefaultProfile</span></span>
<span data-ttu-id="e5f1c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5f1c-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5f1c-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e5f1c-117">指定代表要設定網路安全性群組之狀態的網路安全性群組物件。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="e5f1c-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e5f1c-118">-Confirm</span></span>
<span data-ttu-id="e5f1c-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f1c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f1c-120">-WhatIf</span></span>
<span data-ttu-id="e5f1c-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5f1c-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f1c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f1c-123">CommonParameters</span></span>
<span data-ttu-id="e5f1c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f1c-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5f1c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f1c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e5f1c-126">INPUTS</span></span>

### <span data-ttu-id="e5f1c-127">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5f1c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e5f1c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e5f1c-128">OUTPUTS</span></span>

### <span data-ttu-id="e5f1c-129">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5f1c-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e5f1c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e5f1c-130">NOTES</span></span>

## <span data-ttu-id="e5f1c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5f1c-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5f1c-132">AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5f1c-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e5f1c-133">新-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5f1c-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e5f1c-134">移除-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5f1c-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


