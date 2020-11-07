---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802254"
---
# <span data-ttu-id="a5565-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a5565-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a5565-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5565-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5565-103">句法</span><span class="sxs-lookup"><span data-stu-id="a5565-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5565-104">說明</span><span class="sxs-lookup"><span data-stu-id="a5565-104">DESCRIPTION</span></span>

## <span data-ttu-id="a5565-105">示例</span><span class="sxs-lookup"><span data-stu-id="a5565-105">EXAMPLES</span></span>

### <span data-ttu-id="a5565-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="a5565-106">1:</span></span>
```

```

## <span data-ttu-id="a5565-107">參數</span><span class="sxs-lookup"><span data-stu-id="a5565-107">PARAMETERS</span></span>

### <span data-ttu-id="a5565-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5565-108">-DefaultProfile</span></span>
<span data-ttu-id="a5565-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5565-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-110">-Force</span><span class="sxs-lookup"><span data-stu-id="a5565-110">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="a5565-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5565-112">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5565-113">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-114">-確認</span><span class="sxs-lookup"><span data-stu-id="a5565-114">-Confirm</span></span>
<span data-ttu-id="a5565-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5565-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5565-116">-WhatIf</span></span>
<span data-ttu-id="a5565-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5565-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5565-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5565-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5565-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5565-119">CommonParameters</span></span>
<span data-ttu-id="a5565-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5565-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5565-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5565-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5565-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a5565-122">INPUTS</span></span>

## <span data-ttu-id="a5565-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a5565-123">OUTPUTS</span></span>

### <span data-ttu-id="a5565-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a5565-124">System.String</span></span>

## <span data-ttu-id="a5565-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a5565-125">NOTES</span></span>

## <span data-ttu-id="a5565-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5565-126">RELATED LINKS</span></span>

[<span data-ttu-id="a5565-127">AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a5565-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a5565-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a5565-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


