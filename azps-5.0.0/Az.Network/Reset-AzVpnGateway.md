---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137399"
---
# <span data-ttu-id="64fef-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="64fef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64fef-102">SYNOPSIS</span></span>
<span data-ttu-id="64fef-103">重設可伸縮的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="64fef-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="64fef-104">句法</span><span class="sxs-lookup"><span data-stu-id="64fef-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64fef-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="64fef-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64fef-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="64fef-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64fef-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="64fef-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64fef-108">說明</span><span class="sxs-lookup"><span data-stu-id="64fef-108">DESCRIPTION</span></span>
<span data-ttu-id="64fef-109">重設 VpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="64fef-110">示例</span><span class="sxs-lookup"><span data-stu-id="64fef-110">EXAMPLES</span></span>

### <span data-ttu-id="64fef-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="64fef-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="64fef-112">參數</span><span class="sxs-lookup"><span data-stu-id="64fef-112">PARAMETERS</span></span>

### <span data-ttu-id="64fef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64fef-113">-AsJob</span></span>
<span data-ttu-id="64fef-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="64fef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64fef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64fef-115">-DefaultProfile</span></span>
<span data-ttu-id="64fef-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64fef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64fef-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-117">-VpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64fef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64fef-118">CommonParameters</span></span>
<span data-ttu-id="64fef-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64fef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64fef-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64fef-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64fef-121">輸入</span><span class="sxs-lookup"><span data-stu-id="64fef-121">INPUTS</span></span>

### <span data-ttu-id="64fef-122">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64fef-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="64fef-123">System.object</span><span class="sxs-lookup"><span data-stu-id="64fef-123">System.String</span></span>

## <span data-ttu-id="64fef-124">輸出</span><span class="sxs-lookup"><span data-stu-id="64fef-124">OUTPUTS</span></span>

### <span data-ttu-id="64fef-125">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64fef-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="64fef-126">筆記</span><span class="sxs-lookup"><span data-stu-id="64fef-126">NOTES</span></span>

## <span data-ttu-id="64fef-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="64fef-127">RELATED LINKS</span></span>

[<span data-ttu-id="64fef-128">AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="64fef-129">新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="64fef-130">移除-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="64fef-131">更新-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="64fef-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)