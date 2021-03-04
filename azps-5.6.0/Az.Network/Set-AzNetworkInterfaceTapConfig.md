---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: a542b69b1f028a7fdfd3e02d02f95735bc4add9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915290"
---
# <span data-ttu-id="d557b-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d557b-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="d557b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d557b-102">SYNOPSIS</span></span>
<span data-ttu-id="d557b-103">更新網路介面的點一下組配置。</span><span class="sxs-lookup"><span data-stu-id="d557b-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="d557b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d557b-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d557b-105">描述</span><span class="sxs-lookup"><span data-stu-id="d557b-105">DESCRIPTION</span></span>
<span data-ttu-id="d557b-106">**Set-AzNetworkInterfaceTapConfig 會** 更新網路介面的點一下設定。</span><span class="sxs-lookup"><span data-stu-id="d557b-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="d557b-107">例子</span><span class="sxs-lookup"><span data-stu-id="d557b-107">EXAMPLES</span></span>

### <span data-ttu-id="d557b-108">範例 1：使用更新的 TapConfig 名稱設定 TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="d557b-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="d557b-109">參數</span><span class="sxs-lookup"><span data-stu-id="d557b-109">PARAMETERS</span></span>

### <span data-ttu-id="d557b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d557b-110">-AsJob</span></span>
<span data-ttu-id="d557b-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d557b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d557b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d557b-112">-DefaultProfile</span></span>
<span data-ttu-id="d557b-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d557b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d557b-114">-強制</span><span class="sxs-lookup"><span data-stu-id="d557b-114">-Force</span></span>
<span data-ttu-id="d557b-115">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="d557b-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d557b-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d557b-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="d557b-117">NetworkInterface Tap 組配置</span><span class="sxs-lookup"><span data-stu-id="d557b-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="d557b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="d557b-118">-Confirm</span></span>
<span data-ttu-id="d557b-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d557b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d557b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d557b-120">-WhatIf</span></span>
<span data-ttu-id="d557b-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d557b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d557b-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d557b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d557b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d557b-123">CommonParameters</span></span>
<span data-ttu-id="d557b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d557b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d557b-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d557b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d557b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d557b-126">INPUTS</span></span>

### <span data-ttu-id="d557b-127">Microsoft.Azure.Commands.Network.models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="d557b-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="d557b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d557b-128">OUTPUTS</span></span>

### <span data-ttu-id="d557b-129">Microsoft.Azure.Commands.Network.models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d557b-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d557b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d557b-130">NOTES</span></span>

## <span data-ttu-id="d557b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d557b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d557b-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d557b-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d557b-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d557b-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d557b-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d557b-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
