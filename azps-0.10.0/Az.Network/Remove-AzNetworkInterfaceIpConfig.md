---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2ccb5f7117df8f959698c894915cedd3a5d4c7e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794165"
---
# <span data-ttu-id="4094a-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4094a-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="4094a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4094a-102">SYNOPSIS</span></span>
<span data-ttu-id="4094a-103">從網路介面移除網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4094a-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="4094a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4094a-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4094a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4094a-105">DESCRIPTION</span></span>
<span data-ttu-id="4094a-106">**AzNetworkInterfaceIpConfig** Cmdlet 會從 Azure 網路介面移除網路介面 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4094a-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="4094a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4094a-107">EXAMPLES</span></span>

### <span data-ttu-id="4094a-108">1：從網路介面刪除 IP 設定</span><span class="sxs-lookup"><span data-stu-id="4094a-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="4094a-109">第一個命令會取得稱為 mynic 的網路介面，並將它儲存在 $nic 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4094a-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="4094a-110">第二個命令會移除與此網路介面相關聯的 IP 配置（即，稱為 IPConfig-1）。</span><span class="sxs-lookup"><span data-stu-id="4094a-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="4094a-111">參數</span><span class="sxs-lookup"><span data-stu-id="4094a-111">PARAMETERS</span></span>

### <span data-ttu-id="4094a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4094a-112">-DefaultProfile</span></span>
<span data-ttu-id="4094a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4094a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4094a-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4094a-114">-Name</span></span>
<span data-ttu-id="4094a-115">指定要移除的網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="4094a-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="4094a-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4094a-116">-NetworkInterface</span></span>
<span data-ttu-id="4094a-117">指定 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="4094a-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="4094a-118">這個物件包含要移除的網路介面 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="4094a-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="4094a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4094a-119">CommonParameters</span></span>
<span data-ttu-id="4094a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4094a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4094a-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4094a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4094a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4094a-122">INPUTS</span></span>

### <span data-ttu-id="4094a-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4094a-123">PSNetworkInterface</span></span>
<span data-ttu-id="4094a-124">形參 "NetworkInterface" 接受管線中 "PSNetworkInterface" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4094a-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="4094a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4094a-125">OUTPUTS</span></span>

### <span data-ttu-id="4094a-126">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4094a-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4094a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4094a-127">NOTES</span></span>
* <span data-ttu-id="4094a-128">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="4094a-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4094a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4094a-129">RELATED LINKS</span></span>

[<span data-ttu-id="4094a-130">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4094a-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4094a-131">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4094a-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4094a-132">新-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4094a-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4094a-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4094a-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


