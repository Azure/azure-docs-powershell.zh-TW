---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9cbb814fde6d81449228a18913254cf807d5502c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446168"
---
# <span data-ttu-id="839bb-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="839bb-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="839bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="839bb-102">SYNOPSIS</span></span>
<span data-ttu-id="839bb-103">從網路介面移除網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="839bb-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="839bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="839bb-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="839bb-105">DESCRIPTION</span></span>
<span data-ttu-id="839bb-106">**AzureRmNetworkInterfaceIpConfig** Cmdlet 會從 Azure 網路介面移除網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="839bb-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="839bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="839bb-107">EXAMPLES</span></span>

### <span data-ttu-id="839bb-108">1：從網路介面刪除 IP 設定</span><span class="sxs-lookup"><span data-stu-id="839bb-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="839bb-109">第一個命令會取得稱為 mynic 的網路介面，並將它儲存在 $nic 的變數中。</span><span class="sxs-lookup"><span data-stu-id="839bb-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="839bb-110">第二個命令會移除與此網路介面相關聯的 IP 配置（即，稱為 IPConfig-1）。</span><span class="sxs-lookup"><span data-stu-id="839bb-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="839bb-111">參數</span><span class="sxs-lookup"><span data-stu-id="839bb-111">PARAMETERS</span></span>

### <span data-ttu-id="839bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839bb-112">-DefaultProfile</span></span>
<span data-ttu-id="839bb-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="839bb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839bb-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="839bb-114">-Name</span></span>
<span data-ttu-id="839bb-115">指定要移除的網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="839bb-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839bb-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="839bb-116">-NetworkInterface</span></span>
<span data-ttu-id="839bb-117">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="839bb-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="839bb-118">這個物件包含要移除的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="839bb-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="839bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839bb-119">CommonParameters</span></span>
<span data-ttu-id="839bb-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="839bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839bb-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="839bb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839bb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="839bb-122">INPUTS</span></span>

### <span data-ttu-id="839bb-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="839bb-123">PSNetworkInterface</span></span>
<span data-ttu-id="839bb-124">形參 "NetworkInterface" 接受管線中 "PSNetworkInterface" 類型的值</span><span class="sxs-lookup"><span data-stu-id="839bb-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="839bb-125">輸出</span><span class="sxs-lookup"><span data-stu-id="839bb-125">OUTPUTS</span></span>

### <span data-ttu-id="839bb-126">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="839bb-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="839bb-127">筆記</span><span class="sxs-lookup"><span data-stu-id="839bb-127">NOTES</span></span>
* <span data-ttu-id="839bb-128">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="839bb-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="839bb-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="839bb-129">RELATED LINKS</span></span>

[<span data-ttu-id="839bb-130">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="839bb-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="839bb-131">AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="839bb-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="839bb-132">新-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="839bb-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="839bb-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="839bb-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


