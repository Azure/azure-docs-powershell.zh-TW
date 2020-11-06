---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448110"
---
# <span data-ttu-id="fb476-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb476-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="fb476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb476-102">SYNOPSIS</span></span>
<span data-ttu-id="fb476-103">設定網路安全性群組的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="fb476-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb476-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb476-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb476-105">說明</span><span class="sxs-lookup"><span data-stu-id="fb476-105">DESCRIPTION</span></span>
<span data-ttu-id="fb476-106">**AzureRmNetworkSecurityGroup** Cmdlet 會為 Azure 網路安全群組設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="fb476-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="fb476-107">示例</span><span class="sxs-lookup"><span data-stu-id="fb476-107">EXAMPLES</span></span>

### <span data-ttu-id="fb476-108">範例1：設定網路安全性群組的目標狀態</span><span class="sxs-lookup"><span data-stu-id="fb476-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="fb476-109">這個命令會取得名為 Nsg1 的 Azure 網路安全性群組，並將名為 Rdp-Rule 的網路安全規則，新增到使用 AzureRmNetworkSecurityRuleConfig 的 [允許埠3389上的網際網路流量]。</span><span class="sxs-lookup"><span data-stu-id="fb476-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="fb476-110">此命令會使用 **設定 AzureRmNetworkSecurityGroup** ，將已修改的 Azure 網路安全性群組保持不變。</span><span class="sxs-lookup"><span data-stu-id="fb476-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="fb476-111">參數</span><span class="sxs-lookup"><span data-stu-id="fb476-111">PARAMETERS</span></span>

### <span data-ttu-id="fb476-112">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb476-112">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fb476-113">代表 Cmdlet 設定網路安全群組之目標狀態的網路安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="fb476-113">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="fb476-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb476-114">-DefaultProfile</span></span>
<span data-ttu-id="fb476-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb476-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb476-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb476-116">CommonParameters</span></span>
<span data-ttu-id="fb476-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb476-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb476-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb476-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb476-119">輸入</span><span class="sxs-lookup"><span data-stu-id="fb476-119">INPUTS</span></span>

### <span data-ttu-id="fb476-120">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb476-120">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="fb476-121">形參 "NetworkSecurityGroup" 接受管線中 "PSNetworkSecurityGroup" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fb476-121">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="fb476-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fb476-122">OUTPUTS</span></span>

### <span data-ttu-id="fb476-123">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fb476-123">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fb476-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fb476-124">NOTES</span></span>

## <span data-ttu-id="fb476-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb476-125">RELATED LINKS</span></span>

[<span data-ttu-id="fb476-126">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb476-126">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="fb476-127">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb476-127">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="fb476-128">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb476-128">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


