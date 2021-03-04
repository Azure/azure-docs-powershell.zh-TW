---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: 5cb8c8f93b491476e01d5ae54cf2db93ac4a848a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915285"
---
# <span data-ttu-id="c1d2e-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="c1d2e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d2e-103">更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-103">Updates a network profile.</span></span>

## <span data-ttu-id="c1d2e-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1d2e-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1d2e-105">描述</span><span class="sxs-lookup"><span data-stu-id="c1d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d2e-106">**Set-AzPublicIpPrefix** Cmdlet 會更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="c1d2e-107">例子</span><span class="sxs-lookup"><span data-stu-id="c1d2e-107">EXAMPLES</span></span>

### <span data-ttu-id="c1d2e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c1d2e-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="c1d2e-109">第一個命令會獲得現有的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="c1d2e-110">第二個命令會更新標記，第三個命令會新增網路設定檔上的網路介面組式。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="c1d2e-111">第四個命令會更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="c1d2e-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1d2e-112">PARAMETERS</span></span>

### <span data-ttu-id="c1d2e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1d2e-113">-AsJob</span></span>
<span data-ttu-id="c1d2e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1d2e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1d2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-115">-DefaultProfile</span></span>
<span data-ttu-id="c1d2e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1d2e-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-117">-NetworkProfile</span></span>
<span data-ttu-id="c1d2e-118">網路設定檔</span><span class="sxs-lookup"><span data-stu-id="c1d2e-118">The network profile</span></span>

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

### <span data-ttu-id="c1d2e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c1d2e-119">-Confirm</span></span>
<span data-ttu-id="c1d2e-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d2e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d2e-121">-WhatIf</span></span>
<span data-ttu-id="c1d2e-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1d2e-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d2e-124">CommonParameters</span></span>
<span data-ttu-id="c1d2e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d2e-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c1d2e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d2e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c1d2e-127">INPUTS</span></span>

### <span data-ttu-id="c1d2e-128">Microsoft.Azure.Commands.Network.models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c1d2e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c1d2e-129">OUTPUTS</span></span>

### <span data-ttu-id="c1d2e-130">Microsoft.Azure.Commands.Network.models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c1d2e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c1d2e-131">NOTES</span></span>

## <span data-ttu-id="c1d2e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1d2e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1d2e-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="c1d2e-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="c1d2e-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2e-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
