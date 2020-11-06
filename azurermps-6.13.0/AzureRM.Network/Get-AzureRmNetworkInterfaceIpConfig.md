---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: eac8a985cfcb531247fcf2617fee86da92ea0112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457412"
---
# <span data-ttu-id="0e3a8-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e3a8-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="0e3a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3a8-103">取得網路介面的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e3a8-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e3a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3a8-106">**AzureRmNetworkInterfaceIPConfig** Cmdlet 會從 Azure 網路介面取得網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="0e3a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e3a8-107">EXAMPLES</span></span>

### <span data-ttu-id="0e3a8-108">1：取得網路介面的 IP 設定</span><span class="sxs-lookup"><span data-stu-id="0e3a8-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="0e3a8-109">第一個命令會取得名為 mynic 的現有網路介面，並將它儲存在 $nic 1 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="0e3a8-110">第二個命令會取得此網路介面的名為 ipconfig1 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="0e3a8-111">參數</span><span class="sxs-lookup"><span data-stu-id="0e3a8-111">PARAMETERS</span></span>

### <span data-ttu-id="0e3a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3a8-112">-DefaultProfile</span></span>
<span data-ttu-id="0e3a8-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3a8-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e3a8-114">-Name</span></span>
<span data-ttu-id="0e3a8-115">指定此 Cmdlet 所取得之網路 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0e3a8-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0e3a8-116">-NetworkInterface</span></span>
<span data-ttu-id="0e3a8-117">指定包含此 Cmdlet 所取得之網路 IP 配置的 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0e3a8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3a8-118">CommonParameters</span></span>
<span data-ttu-id="0e3a8-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3a8-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e3a8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3a8-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0e3a8-121">INPUTS</span></span>

### <span data-ttu-id="0e3a8-122">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e3a8-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="0e3a8-123">參數： NetworkInterface (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0e3a8-123">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="0e3a8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0e3a8-124">OUTPUTS</span></span>

### <span data-ttu-id="0e3a8-125">PSNetworkInterfaceIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e3a8-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="0e3a8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0e3a8-126">NOTES</span></span>
* <span data-ttu-id="0e3a8-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="0e3a8-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0e3a8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e3a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e3a8-129">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e3a8-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0e3a8-130">新-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e3a8-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0e3a8-131">移除-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e3a8-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0e3a8-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e3a8-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


