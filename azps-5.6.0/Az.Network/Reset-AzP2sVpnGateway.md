---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: c813f5d5921f0291174a77cf6cdc4b0a1f7ee6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903462"
---
# <span data-ttu-id="9ed5d-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="9ed5d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9ed5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed5d-103">重設可縮放 P2S VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="9ed5d-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="9ed5d-104">語法</span><span class="sxs-lookup"><span data-stu-id="9ed5d-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed5d-105">ByP2S VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="9ed5d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed5d-106">ByP2S VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9ed5d-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed5d-107">ByP2S VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed5d-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed5d-108">描述</span><span class="sxs-lookup"><span data-stu-id="9ed5d-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed5d-109">重設 P2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="9ed5d-110">例子</span><span class="sxs-lookup"><span data-stu-id="9ed5d-110">EXAMPLES</span></span>

### <span data-ttu-id="9ed5d-111">範例 1：</span><span class="sxs-lookup"><span data-stu-id="9ed5d-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="9ed5d-112">參數</span><span class="sxs-lookup"><span data-stu-id="9ed5d-112">PARAMETERS</span></span>

### <span data-ttu-id="9ed5d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ed5d-113">-AsJob</span></span>
<span data-ttu-id="9ed5d-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ed5d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ed5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed5d-115">-DefaultProfile</span></span>
<span data-ttu-id="9ed5d-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ed5d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed5d-117">-P2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="9ed5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed5d-118">CommonParameters</span></span>
<span data-ttu-id="9ed5d-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9ed5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed5d-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9ed5d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed5d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9ed5d-121">INPUTS</span></span>

### <span data-ttu-id="9ed5d-122">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="9ed5d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9ed5d-123">System.String</span></span>

## <span data-ttu-id="9ed5d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9ed5d-124">OUTPUTS</span></span>

### <span data-ttu-id="9ed5d-125">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="9ed5d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9ed5d-126">NOTES</span></span>

## <span data-ttu-id="9ed5d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ed5d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9ed5d-128">Get-AzP2s VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="9ed5d-129">New-AzP2s VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="9ed5d-130">Remove-AzP2s VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="9ed5d-131">Update-AzP2s VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9ed5d-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
