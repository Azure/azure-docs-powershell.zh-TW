---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958428"
---
# <span data-ttu-id="ac5c1-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ac5c1-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ac5c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5c1-103">更新網路介面的攻絲配置。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="ac5c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac5c1-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ac5c1-106">AzNetworkInterfaceTapConfig 會更新網路介面的攻絲 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="ac5c1-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac5c1-107">EXAMPLES</span></span>

### <span data-ttu-id="ac5c1-108">範例1：使用更新的 TapConfig 名稱來設定 TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac5c1-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="ac5c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="ac5c1-109">PARAMETERS</span></span>

### <span data-ttu-id="ac5c1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac5c1-110">-AsJob</span></span>
<span data-ttu-id="ac5c1-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac5c1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac5c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5c1-112">-DefaultProfile</span></span>
<span data-ttu-id="ac5c1-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5c1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ac5c1-114">-Force</span></span>
<span data-ttu-id="ac5c1-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ac5c1-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ac5c1-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="ac5c1-117">NetworkInterface 攻絲設定</span><span class="sxs-lookup"><span data-stu-id="ac5c1-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="ac5c1-118">-確認</span><span class="sxs-lookup"><span data-stu-id="ac5c1-118">-Confirm</span></span>
<span data-ttu-id="ac5c1-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5c1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5c1-120">-WhatIf</span></span>
<span data-ttu-id="ac5c1-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5c1-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5c1-123">CommonParameters</span></span>
<span data-ttu-id="ac5c1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5c1-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac5c1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5c1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ac5c1-126">INPUTS</span></span>

### <span data-ttu-id="ac5c1-127">PSNetworkInterfaceTapConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ac5c1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="ac5c1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ac5c1-128">OUTPUTS</span></span>

### <span data-ttu-id="ac5c1-129">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ac5c1-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ac5c1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ac5c1-130">NOTES</span></span>

## <span data-ttu-id="ac5c1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac5c1-131">RELATED LINKS</span></span>

[<span data-ttu-id="ac5c1-132">附加 AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ac5c1-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ac5c1-133">AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ac5c1-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ac5c1-134">移除-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ac5c1-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
