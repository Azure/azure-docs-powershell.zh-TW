---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 33abb4e724f5a442efd6791cbf6256100662ab65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908805"
---
# <span data-ttu-id="37838-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="37838-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37838-102">SYNOPSIS</span></span>
<span data-ttu-id="37838-103">重設可縮放 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="37838-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="37838-104">語法</span><span class="sxs-lookup"><span data-stu-id="37838-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37838-105">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="37838-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37838-106">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="37838-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37838-107">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="37838-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37838-108">描述</span><span class="sxs-lookup"><span data-stu-id="37838-108">DESCRIPTION</span></span>
<span data-ttu-id="37838-109">重設 VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="37838-110">例子</span><span class="sxs-lookup"><span data-stu-id="37838-110">EXAMPLES</span></span>

### <span data-ttu-id="37838-111">範例 1：</span><span class="sxs-lookup"><span data-stu-id="37838-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="37838-112">參數</span><span class="sxs-lookup"><span data-stu-id="37838-112">PARAMETERS</span></span>

### <span data-ttu-id="37838-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37838-113">-AsJob</span></span>
<span data-ttu-id="37838-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37838-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37838-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37838-115">-DefaultProfile</span></span>
<span data-ttu-id="37838-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37838-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37838-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-117">-VpnGateway</span></span>
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

### <span data-ttu-id="37838-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37838-118">CommonParameters</span></span>
<span data-ttu-id="37838-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37838-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37838-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="37838-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37838-121">輸入</span><span class="sxs-lookup"><span data-stu-id="37838-121">INPUTS</span></span>

### <span data-ttu-id="37838-122">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="37838-123">System.String</span><span class="sxs-lookup"><span data-stu-id="37838-123">System.String</span></span>

## <span data-ttu-id="37838-124">輸出</span><span class="sxs-lookup"><span data-stu-id="37838-124">OUTPUTS</span></span>

### <span data-ttu-id="37838-125">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="37838-126">筆記</span><span class="sxs-lookup"><span data-stu-id="37838-126">NOTES</span></span>

## <span data-ttu-id="37838-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="37838-127">RELATED LINKS</span></span>

[<span data-ttu-id="37838-128">Get-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="37838-129">New-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="37838-130">Remove-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="37838-131">Update-Az VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37838-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
