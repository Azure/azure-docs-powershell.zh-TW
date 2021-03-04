---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 572ea4aac029068e3b7e4fbcf12f3b240129d585
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916041"
---
# <span data-ttu-id="e5375-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5375-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e5375-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5375-102">SYNOPSIS</span></span>
<span data-ttu-id="e5375-103">為網路介面進行網路介面 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="e5375-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="e5375-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5375-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5375-105">描述</span><span class="sxs-lookup"><span data-stu-id="e5375-105">DESCRIPTION</span></span>
<span data-ttu-id="e5375-106">**Get-AzNetworkInterfaceIPConfig** Cmdlet 會從 Azure 網路介面取得網路介面 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="e5375-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="e5375-107">例子</span><span class="sxs-lookup"><span data-stu-id="e5375-107">EXAMPLES</span></span>

### <span data-ttu-id="e5375-108">1：取得網路介面的 IP 組</span><span class="sxs-lookup"><span data-stu-id="e5375-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="e5375-109">第一個命令會獲得稱為 mynic 的現有網路介面，並儲存在變數 $nic 1。</span><span class="sxs-lookup"><span data-stu-id="e5375-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="e5375-110">第二個命令會獲得此網路介面的 IP 組配置，稱為 ipconfig1。</span><span class="sxs-lookup"><span data-stu-id="e5375-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="e5375-111">參數</span><span class="sxs-lookup"><span data-stu-id="e5375-111">PARAMETERS</span></span>

### <span data-ttu-id="e5375-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5375-112">-DefaultProfile</span></span>
<span data-ttu-id="e5375-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5375-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5375-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5375-114">-Name</span></span>
<span data-ttu-id="e5375-115">指定此 Cmdlet 所獲得之網路 IP 組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5375-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e5375-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e5375-116">-NetworkInterface</span></span>
<span data-ttu-id="e5375-117">指定 **包含此 Cmdlet** 所獲得之網路 IP 配置的 NetworkInterface 物件。</span><span class="sxs-lookup"><span data-stu-id="e5375-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e5375-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5375-118">CommonParameters</span></span>
<span data-ttu-id="e5375-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5375-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5375-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5375-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5375-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e5375-121">INPUTS</span></span>

### <span data-ttu-id="e5375-122">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e5375-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e5375-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e5375-123">OUTPUTS</span></span>

### <span data-ttu-id="e5375-124">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5375-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="e5375-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e5375-125">NOTES</span></span>
* <span data-ttu-id="e5375-126">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="e5375-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e5375-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5375-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5375-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5375-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e5375-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5375-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e5375-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5375-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e5375-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5375-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


