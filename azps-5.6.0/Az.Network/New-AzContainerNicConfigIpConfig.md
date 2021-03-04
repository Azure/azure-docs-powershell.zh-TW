---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 6ed82377de2a87b3bc40d3d4e8dff6af751ed1f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903570"
---
# <span data-ttu-id="2c516-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c516-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="2c516-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c516-102">SYNOPSIS</span></span>
<span data-ttu-id="2c516-103">建立容器 nic configuration ip 組組物件。</span><span class="sxs-lookup"><span data-stu-id="2c516-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="2c516-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c516-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c516-105">描述</span><span class="sxs-lookup"><span data-stu-id="2c516-105">DESCRIPTION</span></span>
<span data-ttu-id="2c516-106">**New-AzContainerNicConfigIpConfig Cmdlet** 會建立一個新的容器網路介面組式 ip 組式。</span><span class="sxs-lookup"><span data-stu-id="2c516-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="2c516-107">例子</span><span class="sxs-lookup"><span data-stu-id="2c516-107">EXAMPLES</span></span>

### <span data-ttu-id="2c516-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c516-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="2c516-109">前兩個命令會建立並初始化 vnet 和子網。</span><span class="sxs-lookup"><span data-stu-id="2c516-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="2c516-110">第三個命令會建立參照所建立子網的容器 nic ip 組設定檔。</span><span class="sxs-lookup"><span data-stu-id="2c516-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="2c516-111">第四個命令會建立容器網路介面組配置，提供在上一個命令中建立之 ip 組設定檔。</span><span class="sxs-lookup"><span data-stu-id="2c516-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="2c516-112">最後，第五個命令會建立一個初始化的網路設定檔，其為儲存在 $containerNicConfig 中的容器網路介面$containerNicConfig。</span><span class="sxs-lookup"><span data-stu-id="2c516-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="2c516-113">參數</span><span class="sxs-lookup"><span data-stu-id="2c516-113">PARAMETERS</span></span>

### <span data-ttu-id="2c516-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c516-114">-DefaultProfile</span></span>
<span data-ttu-id="2c516-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c516-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c516-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c516-116">-Name</span></span>
<span data-ttu-id="2c516-117">容器網路介面組調 ip 組設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c516-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="2c516-118">-子網</span><span class="sxs-lookup"><span data-stu-id="2c516-118">-Subnet</span></span>
<span data-ttu-id="2c516-119">子</span><span class="sxs-lookup"><span data-stu-id="2c516-119">Subnet</span></span>

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

### <span data-ttu-id="2c516-120">-子網Id</span><span class="sxs-lookup"><span data-stu-id="2c516-120">-SubnetId</span></span>
<span data-ttu-id="2c516-121">子網Id</span><span class="sxs-lookup"><span data-stu-id="2c516-121">SubnetId</span></span>

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

### <span data-ttu-id="2c516-122">-確認</span><span class="sxs-lookup"><span data-stu-id="2c516-122">-Confirm</span></span>
<span data-ttu-id="2c516-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2c516-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c516-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c516-124">-WhatIf</span></span>
<span data-ttu-id="2c516-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c516-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c516-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c516-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c516-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c516-127">CommonParameters</span></span>
<span data-ttu-id="2c516-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c516-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c516-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2c516-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c516-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2c516-130">INPUTS</span></span>

### <span data-ttu-id="2c516-131">沒有</span><span class="sxs-lookup"><span data-stu-id="2c516-131">None</span></span>

## <span data-ttu-id="2c516-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2c516-132">OUTPUTS</span></span>

### <span data-ttu-id="2c516-133">Microsoft.Azure.Commands.Network.models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c516-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="2c516-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2c516-134">NOTES</span></span>

## <span data-ttu-id="2c516-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c516-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c516-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2c516-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
