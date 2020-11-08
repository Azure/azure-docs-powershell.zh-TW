---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 75f05c76b76f37e936798766d9288ace38d1397f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966204"
---
# <span data-ttu-id="f4e11-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f4e11-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="f4e11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4e11-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e11-103">建立新的樹枝 network 介面設定物件。</span><span class="sxs-lookup"><span data-stu-id="f4e11-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="f4e11-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4e11-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e11-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4e11-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e11-106">**新的-AzContainerNicConfig** Cmdlet 會建立新的容器網路介面設定物件。</span><span class="sxs-lookup"><span data-stu-id="f4e11-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="f4e11-107">這個物件會判斷已建立參照上層網路設定檔之容器網路介面的特性。</span><span class="sxs-lookup"><span data-stu-id="f4e11-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="f4e11-108">示例</span><span class="sxs-lookup"><span data-stu-id="f4e11-108">EXAMPLES</span></span>

### <span data-ttu-id="f4e11-109">範例1</span><span class="sxs-lookup"><span data-stu-id="f4e11-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="f4e11-110">第一個命令會建立空白的容器網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="f4e11-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="f4e11-111">第二個建立新的網路設定檔，將先前建立的容器網路介面設定傳送成 New-NetworkProfile Cmdlet 的引數。</span><span class="sxs-lookup"><span data-stu-id="f4e11-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="f4e11-112">參數</span><span class="sxs-lookup"><span data-stu-id="f4e11-112">PARAMETERS</span></span>

### <span data-ttu-id="f4e11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e11-113">-DefaultProfile</span></span>
<span data-ttu-id="f4e11-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4e11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e11-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4e11-115">-IpConfiguration</span></span>
<span data-ttu-id="f4e11-116">從這個容器網路介面設定來具現化容器 nic 時，決定要建立哪些 ip 配置的 IP 配置設定檔集合</span><span class="sxs-lookup"><span data-stu-id="f4e11-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e11-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4e11-117">-Name</span></span>
<span data-ttu-id="f4e11-118">容器網路介面配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e11-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="f4e11-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f4e11-119">-Confirm</span></span>
<span data-ttu-id="f4e11-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4e11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e11-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e11-121">-WhatIf</span></span>
<span data-ttu-id="f4e11-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4e11-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4e11-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4e11-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e11-124">CommonParameters</span></span>
<span data-ttu-id="f4e11-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4e11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e11-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4e11-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e11-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f4e11-127">INPUTS</span></span>

### <span data-ttu-id="f4e11-128">PSIPConfigurationProfile [] （[]）</span><span class="sxs-lookup"><span data-stu-id="f4e11-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="f4e11-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f4e11-129">OUTPUTS</span></span>

### <span data-ttu-id="f4e11-130">PSContainerNetworkInterfaceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4e11-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="f4e11-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f4e11-131">NOTES</span></span>

## <span data-ttu-id="f4e11-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4e11-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4e11-133">新-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e11-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)