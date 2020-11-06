---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443768"
---
# <span data-ttu-id="91487-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="91487-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="91487-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91487-102">SYNOPSIS</span></span>
<span data-ttu-id="91487-103">設定現有網路設定檔的目標狀態</span><span class="sxs-lookup"><span data-stu-id="91487-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91487-104">句法</span><span class="sxs-lookup"><span data-stu-id="91487-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91487-105">說明</span><span class="sxs-lookup"><span data-stu-id="91487-105">DESCRIPTION</span></span>
<span data-ttu-id="91487-106">**AzureRmPublicIpPrefix** Cmdlet 設定網路設定檔的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="91487-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="91487-107">示例</span><span class="sxs-lookup"><span data-stu-id="91487-107">EXAMPLES</span></span>

### <span data-ttu-id="91487-108">範例1</span><span class="sxs-lookup"><span data-stu-id="91487-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="91487-109">第一個命令會取得現有的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="91487-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="91487-110">第二個命令會更新標記，第三個命令會在網路設定檔上新增網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="91487-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="91487-111">第四個命令會更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="91487-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="91487-112">參數</span><span class="sxs-lookup"><span data-stu-id="91487-112">PARAMETERS</span></span>

### <span data-ttu-id="91487-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91487-113">-AsJob</span></span>
<span data-ttu-id="91487-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91487-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91487-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91487-115">-DefaultProfile</span></span>
<span data-ttu-id="91487-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91487-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91487-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="91487-117">-NetworkProfile</span></span>
<span data-ttu-id="91487-118">網路設定檔</span><span class="sxs-lookup"><span data-stu-id="91487-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91487-119">-確認</span><span class="sxs-lookup"><span data-stu-id="91487-119">-Confirm</span></span>
<span data-ttu-id="91487-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91487-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91487-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91487-121">-WhatIf</span></span>
<span data-ttu-id="91487-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91487-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91487-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91487-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91487-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91487-124">CommonParameters</span></span>
<span data-ttu-id="91487-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91487-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91487-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91487-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91487-127">輸入</span><span class="sxs-lookup"><span data-stu-id="91487-127">INPUTS</span></span>

### <span data-ttu-id="91487-128">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="91487-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="91487-129">輸出</span><span class="sxs-lookup"><span data-stu-id="91487-129">OUTPUTS</span></span>

### <span data-ttu-id="91487-130">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="91487-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="91487-131">筆記</span><span class="sxs-lookup"><span data-stu-id="91487-131">NOTES</span></span>

## <span data-ttu-id="91487-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="91487-132">RELATED LINKS</span></span>
