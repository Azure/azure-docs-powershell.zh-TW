---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626376"
---
# <span data-ttu-id="b8632-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b8632-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="b8632-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8632-102">SYNOPSIS</span></span>
<span data-ttu-id="b8632-103">建立新的樹枝 network 介面設定物件。</span><span class="sxs-lookup"><span data-stu-id="b8632-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8632-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8632-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8632-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8632-105">DESCRIPTION</span></span>
<span data-ttu-id="b8632-106">**新的-AzureRmNetworkProfileContainerNicConfig** Cmdlet 會建立新的容器網路介面設定物件。</span><span class="sxs-lookup"><span data-stu-id="b8632-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="b8632-107">這個物件會判斷已建立參照上層網路設定檔之容器網路 interfacs 的特性。</span><span class="sxs-lookup"><span data-stu-id="b8632-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="b8632-108">示例</span><span class="sxs-lookup"><span data-stu-id="b8632-108">EXAMPLES</span></span>

### <span data-ttu-id="b8632-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b8632-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="b8632-110">第一個命令會建立空白的容器網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="b8632-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="b8632-111">第二個建立新的網路設定檔，將先前建立的容器網路介面設定傳送成 New-NetworkProfile Cmdlet 的引數。</span><span class="sxs-lookup"><span data-stu-id="b8632-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="b8632-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8632-112">PARAMETERS</span></span>

### <span data-ttu-id="b8632-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8632-113">-DefaultProfile</span></span>
<span data-ttu-id="b8632-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8632-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8632-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8632-115">-IpConfiguration</span></span>
<span data-ttu-id="b8632-116">{{Fill IpConfiguration 描述}}</span><span class="sxs-lookup"><span data-stu-id="b8632-116">{{Fill IpConfiguration Description}}</span></span>

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

### <span data-ttu-id="b8632-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8632-117">-Name</span></span>
<span data-ttu-id="b8632-118">容器網路介面配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8632-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="b8632-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b8632-119">-Confirm</span></span>
<span data-ttu-id="b8632-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8632-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8632-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8632-121">-WhatIf</span></span>
<span data-ttu-id="b8632-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8632-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8632-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8632-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8632-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8632-124">CommonParameters</span></span>
<span data-ttu-id="b8632-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8632-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8632-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8632-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8632-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b8632-127">INPUTS</span></span>

### <span data-ttu-id="b8632-128">[System.object]. 清單 ' 1 [PSIPConfigurationProfile，6.7.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="b8632-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b8632-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b8632-129">OUTPUTS</span></span>

### <span data-ttu-id="b8632-130">PSContainerNetworkInterfaceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8632-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="b8632-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b8632-131">NOTES</span></span>

## <span data-ttu-id="b8632-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8632-132">RELATED LINKS</span></span>
