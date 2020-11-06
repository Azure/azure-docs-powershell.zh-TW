---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450240"
---
# <span data-ttu-id="bb8c9-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="bb8c9-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="bb8c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8c9-103">建立容器 nic 配置 ip 設定物件。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb8c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb8c9-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8c9-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb8c9-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8c9-106">**新的-AzureRmNetworkProfileContainerNicConfigIpConfig** Cmdlet 會建立新的容器網路介面配置 ip 配置。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="bb8c9-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb8c9-107">EXAMPLES</span></span>

### <span data-ttu-id="bb8c9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb8c9-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="bb8c9-109">前兩個命令會建立和初始化 vnet 與子網。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="bb8c9-110">第三個命令會建立一個參照所建立子網的容器 nic ip 配置設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="bb8c9-111">第四個命令會建立容器網路介面配置，以提供在前一個命令中建立的 ip 配置設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="bb8c9-112">最後，第五個命令會使用儲存在 $containerNicConfig 中的容器網路介面配置來建立已初始化的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="bb8c9-113">參數</span><span class="sxs-lookup"><span data-stu-id="bb8c9-113">PARAMETERS</span></span>

### <span data-ttu-id="bb8c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8c9-114">-DefaultProfile</span></span>
<span data-ttu-id="bb8c9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8c9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb8c9-116">-Name</span></span>
<span data-ttu-id="bb8c9-117">容器網路介面配置 ip 配置設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="bb8c9-118">-子網</span><span class="sxs-lookup"><span data-stu-id="bb8c9-118">-Subnet</span></span>
<span data-ttu-id="bb8c9-119">端子</span><span class="sxs-lookup"><span data-stu-id="bb8c9-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8c9-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bb8c9-120">-SubnetId</span></span>
<span data-ttu-id="bb8c9-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="bb8c9-121">SubnetId</span></span>

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

### <span data-ttu-id="bb8c9-122">-確認</span><span class="sxs-lookup"><span data-stu-id="bb8c9-122">-Confirm</span></span>
<span data-ttu-id="bb8c9-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8c9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8c9-124">-WhatIf</span></span>
<span data-ttu-id="bb8c9-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb8c9-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8c9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8c9-127">CommonParameters</span></span>
<span data-ttu-id="bb8c9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8c9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb8c9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8c9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="bb8c9-130">INPUTS</span></span>

### <span data-ttu-id="bb8c9-131">所有</span><span class="sxs-lookup"><span data-stu-id="bb8c9-131">None</span></span>

## <span data-ttu-id="bb8c9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bb8c9-132">OUTPUTS</span></span>

### <span data-ttu-id="bb8c9-133">PSContainerNetworkInterfaceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb8c9-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="bb8c9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="bb8c9-134">NOTES</span></span>

## <span data-ttu-id="bb8c9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb8c9-135">RELATED LINKS</span></span>
