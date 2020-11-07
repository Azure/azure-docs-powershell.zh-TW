---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 348732794a0cf16233f9a139e86ed89658fc5ac2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801949"
---
# <span data-ttu-id="11559-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11559-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="11559-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11559-102">SYNOPSIS</span></span>
<span data-ttu-id="11559-103">設定網路安全性群組的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="11559-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11559-104">句法</span><span class="sxs-lookup"><span data-stu-id="11559-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11559-105">說明</span><span class="sxs-lookup"><span data-stu-id="11559-105">DESCRIPTION</span></span>
<span data-ttu-id="11559-106">**AzureRmNetworkSecurityGroup** Cmdlet 會為 Azure 網路安全群組設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="11559-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="11559-107">示例</span><span class="sxs-lookup"><span data-stu-id="11559-107">EXAMPLES</span></span>

### <span data-ttu-id="11559-108">範例1：設定網路安全性群組的目標狀態</span><span class="sxs-lookup"><span data-stu-id="11559-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="11559-109">這個命令會取得名為 Nsg1 的 Azure 網路安全性群組，並將名為 Rdp-Rule 的網路安全規則，新增到使用 AzureRmNetworkSecurityRuleConfig 的 [允許埠3389上的網際網路流量]。</span><span class="sxs-lookup"><span data-stu-id="11559-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="11559-110">此命令會使用 **設定 AzureRmNetworkSecurityGroup** ，將已修改的 Azure 網路安全性群組保持不變。</span><span class="sxs-lookup"><span data-stu-id="11559-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="11559-111">參數</span><span class="sxs-lookup"><span data-stu-id="11559-111">PARAMETERS</span></span>

### <span data-ttu-id="11559-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11559-112">-AsJob</span></span>
<span data-ttu-id="11559-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11559-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11559-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11559-114">-DefaultProfile</span></span>
<span data-ttu-id="11559-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11559-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11559-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11559-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="11559-117">代表 Cmdlet 設定網路安全群組之目標狀態的網路安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="11559-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11559-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11559-118">CommonParameters</span></span>
<span data-ttu-id="11559-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11559-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11559-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11559-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11559-121">輸入</span><span class="sxs-lookup"><span data-stu-id="11559-121">INPUTS</span></span>

### <span data-ttu-id="11559-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11559-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="11559-123">形參 "NetworkSecurityGroup" 接受管線中 "PSNetworkSecurityGroup" 類型的值</span><span class="sxs-lookup"><span data-stu-id="11559-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="11559-124">輸出</span><span class="sxs-lookup"><span data-stu-id="11559-124">OUTPUTS</span></span>

### <span data-ttu-id="11559-125">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="11559-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="11559-126">筆記</span><span class="sxs-lookup"><span data-stu-id="11559-126">NOTES</span></span>

## <span data-ttu-id="11559-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="11559-127">RELATED LINKS</span></span>

[<span data-ttu-id="11559-128">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11559-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="11559-129">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11559-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="11559-130">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11559-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


