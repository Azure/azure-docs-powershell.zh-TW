---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443772"
---
# <span data-ttu-id="6dadc-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6dadc-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="6dadc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6dadc-102">SYNOPSIS</span></span>
<span data-ttu-id="6dadc-103">設定分路配置的目標狀態</span><span class="sxs-lookup"><span data-stu-id="6dadc-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dadc-104">句法</span><span class="sxs-lookup"><span data-stu-id="6dadc-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dadc-105">說明</span><span class="sxs-lookup"><span data-stu-id="6dadc-105">DESCRIPTION</span></span>
<span data-ttu-id="6dadc-106">**AzureRmNetworkInterfaceTapConfig 設定** 的是 Azure network 介面的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="6dadc-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="6dadc-107">示例</span><span class="sxs-lookup"><span data-stu-id="6dadc-107">EXAMPLES</span></span>

### <span data-ttu-id="6dadc-108">範例1：使用更新的 TapConfig 名稱來設定 TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dadc-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="6dadc-109">參數</span><span class="sxs-lookup"><span data-stu-id="6dadc-109">PARAMETERS</span></span>

### <span data-ttu-id="6dadc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dadc-110">-AsJob</span></span>
<span data-ttu-id="6dadc-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6dadc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6dadc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dadc-112">-DefaultProfile</span></span>
<span data-ttu-id="6dadc-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dadc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dadc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6dadc-114">-Force</span></span>
<span data-ttu-id="6dadc-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6dadc-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6dadc-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6dadc-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="6dadc-117">NetworkInterface 攻絲 configurtion</span><span class="sxs-lookup"><span data-stu-id="6dadc-117">The NetworkInterface Tap configurtion</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dadc-118">-確認</span><span class="sxs-lookup"><span data-stu-id="6dadc-118">-Confirm</span></span>
<span data-ttu-id="6dadc-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6dadc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dadc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dadc-120">-WhatIf</span></span>
<span data-ttu-id="6dadc-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6dadc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dadc-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6dadc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dadc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dadc-123">CommonParameters</span></span>
<span data-ttu-id="6dadc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6dadc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dadc-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6dadc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dadc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6dadc-126">INPUTS</span></span>

### <span data-ttu-id="6dadc-127">PSNetworkInterfaceTapConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6dadc-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="6dadc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6dadc-128">OUTPUTS</span></span>

### <span data-ttu-id="6dadc-129">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6dadc-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6dadc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6dadc-130">NOTES</span></span>

## <span data-ttu-id="6dadc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dadc-131">RELATED LINKS</span></span>
