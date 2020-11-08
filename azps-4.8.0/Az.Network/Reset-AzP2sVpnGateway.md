---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970305"
---
# <span data-ttu-id="0e7e0-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="0e7e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7e0-103">重設可伸縮的 P2S VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="0e7e0-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="0e7e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e7e0-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e7e0-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="0e7e0-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7e0-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0e7e0-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7e0-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7e0-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e7e0-108">說明</span><span class="sxs-lookup"><span data-stu-id="0e7e0-108">DESCRIPTION</span></span>
<span data-ttu-id="0e7e0-109">重設 P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="0e7e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="0e7e0-110">EXAMPLES</span></span>

### <span data-ttu-id="0e7e0-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="0e7e0-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="0e7e0-112">參數</span><span class="sxs-lookup"><span data-stu-id="0e7e0-112">PARAMETERS</span></span>

### <span data-ttu-id="0e7e0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e7e0-113">-AsJob</span></span>
<span data-ttu-id="0e7e0-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e7e0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e7e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7e0-115">-DefaultProfile</span></span>
<span data-ttu-id="0e7e0-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e7e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e7e0-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="0e7e0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7e0-118">CommonParameters</span></span>
<span data-ttu-id="0e7e0-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e7e0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7e0-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e7e0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7e0-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0e7e0-121">INPUTS</span></span>

### <span data-ttu-id="0e7e0-122">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e7e0-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="0e7e0-123">System.object</span><span class="sxs-lookup"><span data-stu-id="0e7e0-123">System.String</span></span>

## <span data-ttu-id="0e7e0-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0e7e0-124">OUTPUTS</span></span>

### <span data-ttu-id="0e7e0-125">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e7e0-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="0e7e0-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0e7e0-126">NOTES</span></span>

## <span data-ttu-id="0e7e0-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e7e0-127">RELATED LINKS</span></span>

[<span data-ttu-id="0e7e0-128">AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="0e7e0-129">新-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="0e7e0-130">移除-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="0e7e0-131">更新-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e7e0-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)