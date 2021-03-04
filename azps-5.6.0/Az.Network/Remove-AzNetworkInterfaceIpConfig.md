---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: abeeabcc3930a2f18822dbf3d9986e17fbc01c88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912665"
---
# <span data-ttu-id="7d1b0-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d1b0-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="7d1b0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1b0-103">從網路介面移除網路介面 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="7d1b0-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d1b0-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d1b0-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1b0-106">**Remove-AzNetworkInterfaceIpConfig** Cmdlet 會從 Azure 網路介面移除網路介面 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="7d1b0-107">例子</span><span class="sxs-lookup"><span data-stu-id="7d1b0-107">EXAMPLES</span></span>

### <span data-ttu-id="7d1b0-108">範例 1：從網路介面刪除 IP 組</span><span class="sxs-lookup"><span data-stu-id="7d1b0-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="7d1b0-109">第一個命令會獲得稱為 mynic 的網路介面，並儲存在變數或$nic。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="7d1b0-110">第二個命令會移除與此網路介面相關聯的 IP 組配置，稱為 IPConfig-1。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="7d1b0-111">第三個命令會設定對網路介面的變更。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="7d1b0-112">參數</span><span class="sxs-lookup"><span data-stu-id="7d1b0-112">PARAMETERS</span></span>

### <span data-ttu-id="7d1b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1b0-113">-DefaultProfile</span></span>
<span data-ttu-id="7d1b0-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d1b0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d1b0-115">-Name</span></span>
<span data-ttu-id="7d1b0-116">指定要移除的網路介面 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="7d1b0-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d1b0-117">-NetworkInterface</span></span>
<span data-ttu-id="7d1b0-118">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="7d1b0-119">此物件包含要移除的網路介面 IP 組。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="7d1b0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1b0-120">CommonParameters</span></span>
<span data-ttu-id="7d1b0-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1b0-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7d1b0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1b0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7d1b0-123">INPUTS</span></span>

### <span data-ttu-id="7d1b0-124">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d1b0-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7d1b0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7d1b0-125">OUTPUTS</span></span>

### <span data-ttu-id="7d1b0-126">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d1b0-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7d1b0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7d1b0-127">NOTES</span></span>
* <span data-ttu-id="7d1b0-128">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="7d1b0-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7d1b0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d1b0-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d1b0-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d1b0-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7d1b0-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d1b0-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7d1b0-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d1b0-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7d1b0-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d1b0-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


