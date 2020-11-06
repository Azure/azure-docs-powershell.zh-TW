---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 3ef8248f90e24da8818a0fa1a8ff6b05970be397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443767"
---
# <span data-ttu-id="97513-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97513-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="97513-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97513-102">SYNOPSIS</span></span>
<span data-ttu-id="97513-103">設定網路安全性群組的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="97513-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97513-104">句法</span><span class="sxs-lookup"><span data-stu-id="97513-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97513-105">說明</span><span class="sxs-lookup"><span data-stu-id="97513-105">DESCRIPTION</span></span>
<span data-ttu-id="97513-106">**AzureRmNetworkSecurityGroup** Cmdlet 會為 Azure 網路安全群組設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="97513-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="97513-107">示例</span><span class="sxs-lookup"><span data-stu-id="97513-107">EXAMPLES</span></span>

### <span data-ttu-id="97513-108">範例1：設定網路安全性群組的目標狀態</span><span class="sxs-lookup"><span data-stu-id="97513-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="97513-109">這個命令會取得名為 Nsg1 的 Azure 網路安全性群組，並將名為 Rdp-Rule 的網路安全規則，新增到使用 AzureRmNetworkSecurityRuleConfig 的 [允許埠3389上的網際網路流量]。</span><span class="sxs-lookup"><span data-stu-id="97513-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="97513-110">此命令會使用 **設定 AzureRmNetworkSecurityGroup** ，將已修改的 Azure 網路安全性群組保持不變。</span><span class="sxs-lookup"><span data-stu-id="97513-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="97513-111">參數</span><span class="sxs-lookup"><span data-stu-id="97513-111">PARAMETERS</span></span>

### <span data-ttu-id="97513-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97513-112">-AsJob</span></span>
<span data-ttu-id="97513-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97513-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97513-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97513-114">-DefaultProfile</span></span>
<span data-ttu-id="97513-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97513-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97513-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97513-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="97513-117">代表 Cmdlet 設定網路安全群組之目標狀態的網路安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="97513-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="97513-118">-確認</span><span class="sxs-lookup"><span data-stu-id="97513-118">-Confirm</span></span>
<span data-ttu-id="97513-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97513-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97513-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97513-120">-WhatIf</span></span>
<span data-ttu-id="97513-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97513-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97513-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97513-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97513-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97513-123">CommonParameters</span></span>
<span data-ttu-id="97513-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97513-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97513-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97513-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97513-126">輸入</span><span class="sxs-lookup"><span data-stu-id="97513-126">INPUTS</span></span>

### <span data-ttu-id="97513-127">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97513-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="97513-128">參數： NetworkSecurityGroup (ByValue) </span><span class="sxs-lookup"><span data-stu-id="97513-128">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="97513-129">輸出</span><span class="sxs-lookup"><span data-stu-id="97513-129">OUTPUTS</span></span>

### <span data-ttu-id="97513-130">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97513-130">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="97513-131">筆記</span><span class="sxs-lookup"><span data-stu-id="97513-131">NOTES</span></span>

## <span data-ttu-id="97513-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="97513-132">RELATED LINKS</span></span>

[<span data-ttu-id="97513-133">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97513-133">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="97513-134">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97513-134">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="97513-135">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97513-135">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


