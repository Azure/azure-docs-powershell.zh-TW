---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 8c7c1a86b4db7c479367fa83a16888717f1f8079
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621405"
---
# <span data-ttu-id="b555c-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b555c-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b555c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b555c-102">SYNOPSIS</span></span>
<span data-ttu-id="b555c-103">配置虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b555c-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b555c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b555c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b555c-105">說明</span><span class="sxs-lookup"><span data-stu-id="b555c-105">DESCRIPTION</span></span>
<span data-ttu-id="b555c-106">AzVirtualNetworkGatewayConnectionSharedKey Cmdlet 會 **設定** 虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b555c-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b555c-107">示例</span><span class="sxs-lookup"><span data-stu-id="b555c-107">EXAMPLES</span></span>

### <span data-ttu-id="b555c-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="b555c-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="b555c-109">參數</span><span class="sxs-lookup"><span data-stu-id="b555c-109">PARAMETERS</span></span>

### <span data-ttu-id="b555c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b555c-110">-DefaultProfile</span></span>
<span data-ttu-id="b555c-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b555c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b555c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b555c-112">-Force</span></span>
<span data-ttu-id="b555c-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b555c-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b555c-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="b555c-114">-Name</span></span>
<span data-ttu-id="b555c-115">指定虛擬網路閘道共用金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="b555c-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="b555c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b555c-116">-ResourceGroupName</span></span>
<span data-ttu-id="b555c-117">指定虛擬網路閘道所屬之資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b555c-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="b555c-118">-值</span><span class="sxs-lookup"><span data-stu-id="b555c-118">-Value</span></span>
<span data-ttu-id="b555c-119">指定共用金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="b555c-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="b555c-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b555c-120">-Confirm</span></span>
<span data-ttu-id="b555c-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b555c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b555c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b555c-122">-WhatIf</span></span>
<span data-ttu-id="b555c-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b555c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b555c-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b555c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b555c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b555c-125">CommonParameters</span></span>
<span data-ttu-id="b555c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b555c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b555c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b555c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b555c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b555c-128">INPUTS</span></span>

### <span data-ttu-id="b555c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b555c-129">System.String</span></span>

## <span data-ttu-id="b555c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b555c-130">OUTPUTS</span></span>

### <span data-ttu-id="b555c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="b555c-131">System.String</span></span>

## <span data-ttu-id="b555c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b555c-132">NOTES</span></span>

## <span data-ttu-id="b555c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b555c-133">RELATED LINKS</span></span>

[<span data-ttu-id="b555c-134">AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b555c-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b555c-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b555c-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)