---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437495"
---
# <span data-ttu-id="54944-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54944-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="54944-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54944-102">SYNOPSIS</span></span>
<span data-ttu-id="54944-103">從網路介面移除網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="54944-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="54944-104">句法</span><span class="sxs-lookup"><span data-stu-id="54944-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54944-105">說明</span><span class="sxs-lookup"><span data-stu-id="54944-105">DESCRIPTION</span></span>
<span data-ttu-id="54944-106">**AzNetworkInterfaceIpConfig** Cmdlet 會從 Azure 網路介面移除網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="54944-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="54944-107">示例</span><span class="sxs-lookup"><span data-stu-id="54944-107">EXAMPLES</span></span>

### <span data-ttu-id="54944-108">範例1：從網路介面刪除 IP 設定</span><span class="sxs-lookup"><span data-stu-id="54944-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="54944-109">第一個命令會取得稱為 mynic 的網路介面，並將它儲存在 $nic 的變數中。</span><span class="sxs-lookup"><span data-stu-id="54944-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="54944-110">第二個命令會移除與此網路介面相關聯的 IP 配置（即，稱為 IPConfig-1）。</span><span class="sxs-lookup"><span data-stu-id="54944-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="54944-111">第三個命令會設定對網路介面所做的變更。</span><span class="sxs-lookup"><span data-stu-id="54944-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="54944-112">參數</span><span class="sxs-lookup"><span data-stu-id="54944-112">PARAMETERS</span></span>

### <span data-ttu-id="54944-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54944-113">-DefaultProfile</span></span>
<span data-ttu-id="54944-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54944-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54944-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="54944-115">-Name</span></span>
<span data-ttu-id="54944-116">指定要移除的網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="54944-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="54944-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54944-117">-NetworkInterface</span></span>
<span data-ttu-id="54944-118">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="54944-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="54944-119">這個物件包含要移除的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="54944-119">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54944-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54944-120">CommonParameters</span></span>
<span data-ttu-id="54944-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54944-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54944-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54944-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54944-123">輸入</span><span class="sxs-lookup"><span data-stu-id="54944-123">INPUTS</span></span>

### <span data-ttu-id="54944-124">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="54944-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="54944-125">輸出</span><span class="sxs-lookup"><span data-stu-id="54944-125">OUTPUTS</span></span>

### <span data-ttu-id="54944-126">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="54944-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="54944-127">筆記</span><span class="sxs-lookup"><span data-stu-id="54944-127">NOTES</span></span>
* <span data-ttu-id="54944-128">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="54944-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="54944-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="54944-129">RELATED LINKS</span></span>

[<span data-ttu-id="54944-130">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54944-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54944-131">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54944-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54944-132">新-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54944-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54944-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54944-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


