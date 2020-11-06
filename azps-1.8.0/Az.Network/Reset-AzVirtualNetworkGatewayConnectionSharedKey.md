---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1fa793396fba139d1aa08e760c9aa780f8e0f166
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621522"
---
# <span data-ttu-id="16aa7-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="16aa7-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="16aa7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="16aa7-103">重設虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="16aa7-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="16aa7-104">句法</span><span class="sxs-lookup"><span data-stu-id="16aa7-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16aa7-105">說明</span><span class="sxs-lookup"><span data-stu-id="16aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="16aa7-106">重設虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="16aa7-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="16aa7-107">示例</span><span class="sxs-lookup"><span data-stu-id="16aa7-107">EXAMPLES</span></span>

### <span data-ttu-id="16aa7-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="16aa7-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="16aa7-109">參數</span><span class="sxs-lookup"><span data-stu-id="16aa7-109">PARAMETERS</span></span>

### <span data-ttu-id="16aa7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16aa7-110">-DefaultProfile</span></span>
<span data-ttu-id="16aa7-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16aa7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16aa7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="16aa7-112">-Force</span></span>
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

### <span data-ttu-id="16aa7-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="16aa7-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16aa7-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="16aa7-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16aa7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16aa7-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16aa7-116">-確認</span><span class="sxs-lookup"><span data-stu-id="16aa7-116">-Confirm</span></span>
<span data-ttu-id="16aa7-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16aa7-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16aa7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16aa7-118">-WhatIf</span></span>
<span data-ttu-id="16aa7-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16aa7-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16aa7-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16aa7-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16aa7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16aa7-121">CommonParameters</span></span>
<span data-ttu-id="16aa7-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16aa7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16aa7-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16aa7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16aa7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="16aa7-124">INPUTS</span></span>

### <span data-ttu-id="16aa7-125">System.object</span><span class="sxs-lookup"><span data-stu-id="16aa7-125">System.String</span></span>

### <span data-ttu-id="16aa7-126">UInt32</span><span class="sxs-lookup"><span data-stu-id="16aa7-126">System.UInt32</span></span>

## <span data-ttu-id="16aa7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="16aa7-127">OUTPUTS</span></span>

### <span data-ttu-id="16aa7-128">System.object</span><span class="sxs-lookup"><span data-stu-id="16aa7-128">System.String</span></span>

## <span data-ttu-id="16aa7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="16aa7-129">NOTES</span></span>

## <span data-ttu-id="16aa7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="16aa7-130">RELATED LINKS</span></span>

[<span data-ttu-id="16aa7-131">AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="16aa7-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="16aa7-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="16aa7-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
