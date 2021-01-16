---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278803"
---
# <span data-ttu-id="2a581-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a581-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="2a581-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a581-102">SYNOPSIS</span></span>
<span data-ttu-id="2a581-103">取得網路介面的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="2a581-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="2a581-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a581-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a581-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a581-105">DESCRIPTION</span></span>
<span data-ttu-id="2a581-106">**AzNetworkInterfaceIPConfig** Cmdlet 會從 Azure 網路介面取得網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="2a581-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="2a581-107">示例</span><span class="sxs-lookup"><span data-stu-id="2a581-107">EXAMPLES</span></span>

### <span data-ttu-id="2a581-108">1：取得網路介面的 IP 設定</span><span class="sxs-lookup"><span data-stu-id="2a581-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="2a581-109">第一個命令會取得名為 mynic 的現有網路介面，並將它儲存在 $nic 1 的變數中。</span><span class="sxs-lookup"><span data-stu-id="2a581-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="2a581-110">第二個命令會取得此網路介面的名為 ipconfig1 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="2a581-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="2a581-111">參數</span><span class="sxs-lookup"><span data-stu-id="2a581-111">PARAMETERS</span></span>

### <span data-ttu-id="2a581-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a581-112">-DefaultProfile</span></span>
<span data-ttu-id="2a581-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a581-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a581-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a581-114">-Name</span></span>
<span data-ttu-id="2a581-115">指定此 Cmdlet 所取得之網路 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a581-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2a581-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a581-116">-NetworkInterface</span></span>
<span data-ttu-id="2a581-117">指定包含此 Cmdlet 所取得之網路 IP 配置的 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="2a581-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2a581-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a581-118">CommonParameters</span></span>
<span data-ttu-id="2a581-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a581-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a581-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a581-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a581-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2a581-121">INPUTS</span></span>

### <span data-ttu-id="2a581-122">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2a581-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2a581-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2a581-123">OUTPUTS</span></span>

### <span data-ttu-id="2a581-124">PSNetworkInterfaceIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2a581-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="2a581-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2a581-125">NOTES</span></span>
* <span data-ttu-id="2a581-126">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="2a581-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2a581-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a581-127">RELATED LINKS</span></span>

[<span data-ttu-id="2a581-128">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a581-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2a581-129">新-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a581-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2a581-130">移除-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a581-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2a581-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a581-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


