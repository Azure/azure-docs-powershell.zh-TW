---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 78380af20ce5905b5c004424c1e17ac977de40ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790482"
---
# <span data-ttu-id="dd65e-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd65e-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="dd65e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd65e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd65e-103">更新網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="dd65e-103">Updates a network security group.</span></span>

## <span data-ttu-id="dd65e-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd65e-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd65e-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd65e-105">DESCRIPTION</span></span>
<span data-ttu-id="dd65e-106">**AzNetworkSecurityGroup** Cmdlet 會更新網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="dd65e-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="dd65e-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd65e-107">EXAMPLES</span></span>

### <span data-ttu-id="dd65e-108">範例1：更新現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="dd65e-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="dd65e-109">這個命令會取得名為 Nsg1 的 Azure 網路安全性群組，並將名為 Rdp-Rule 的網路安全規則，新增到使用 AzNetworkSecurityRuleConfig 的 [允許埠3389上的網際網路流量]。</span><span class="sxs-lookup"><span data-stu-id="dd65e-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="dd65e-110">此命令會使用 **設定 AzNetworkSecurityGroup** ，將已修改的 Azure 網路安全性群組保持不變。</span><span class="sxs-lookup"><span data-stu-id="dd65e-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="dd65e-111">參數</span><span class="sxs-lookup"><span data-stu-id="dd65e-111">PARAMETERS</span></span>

### <span data-ttu-id="dd65e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd65e-112">-AsJob</span></span>
<span data-ttu-id="dd65e-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd65e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd65e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd65e-114">-DefaultProfile</span></span>
<span data-ttu-id="dd65e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd65e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd65e-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd65e-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="dd65e-117">指定代表要設定網路安全性群組之狀態的網路安全性群組物件。</span><span class="sxs-lookup"><span data-stu-id="dd65e-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="dd65e-118">-確認</span><span class="sxs-lookup"><span data-stu-id="dd65e-118">-Confirm</span></span>
<span data-ttu-id="dd65e-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd65e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd65e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd65e-120">-WhatIf</span></span>
<span data-ttu-id="dd65e-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd65e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd65e-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd65e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd65e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd65e-123">CommonParameters</span></span>
<span data-ttu-id="dd65e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd65e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd65e-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd65e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd65e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="dd65e-126">INPUTS</span></span>

### <span data-ttu-id="dd65e-127">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd65e-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="dd65e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dd65e-128">OUTPUTS</span></span>

### <span data-ttu-id="dd65e-129">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd65e-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="dd65e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dd65e-130">NOTES</span></span>

## <span data-ttu-id="dd65e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd65e-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd65e-132">AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd65e-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dd65e-133">新-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd65e-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dd65e-134">移除-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd65e-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


