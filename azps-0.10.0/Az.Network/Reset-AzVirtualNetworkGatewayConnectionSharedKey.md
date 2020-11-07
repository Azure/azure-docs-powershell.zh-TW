---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795469"
---
# <span data-ttu-id="1cf92-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1cf92-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="1cf92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cf92-102">SYNOPSIS</span></span>

## <span data-ttu-id="1cf92-103">句法</span><span class="sxs-lookup"><span data-stu-id="1cf92-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cf92-104">說明</span><span class="sxs-lookup"><span data-stu-id="1cf92-104">DESCRIPTION</span></span>

## <span data-ttu-id="1cf92-105">示例</span><span class="sxs-lookup"><span data-stu-id="1cf92-105">EXAMPLES</span></span>

### <span data-ttu-id="1cf92-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="1cf92-106">1:</span></span>
```

```

## <span data-ttu-id="1cf92-107">參數</span><span class="sxs-lookup"><span data-stu-id="1cf92-107">PARAMETERS</span></span>

### <span data-ttu-id="1cf92-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf92-108">-DefaultProfile</span></span>
<span data-ttu-id="1cf92-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cf92-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cf92-110">-Force</span><span class="sxs-lookup"><span data-stu-id="1cf92-110">-Force</span></span>
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

### <span data-ttu-id="1cf92-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="1cf92-111">-KeyLength</span></span>
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

### <span data-ttu-id="1cf92-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cf92-112">-Name</span></span>
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

### <span data-ttu-id="1cf92-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf92-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1cf92-114">-確認</span><span class="sxs-lookup"><span data-stu-id="1cf92-114">-Confirm</span></span>
<span data-ttu-id="1cf92-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1cf92-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cf92-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf92-116">-WhatIf</span></span>
<span data-ttu-id="1cf92-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cf92-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cf92-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cf92-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cf92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf92-119">CommonParameters</span></span>
<span data-ttu-id="1cf92-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cf92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf92-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cf92-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf92-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1cf92-122">INPUTS</span></span>

## <span data-ttu-id="1cf92-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1cf92-123">OUTPUTS</span></span>

### <span data-ttu-id="1cf92-124">System.object</span><span class="sxs-lookup"><span data-stu-id="1cf92-124">System.String</span></span>

## <span data-ttu-id="1cf92-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1cf92-125">NOTES</span></span>

## <span data-ttu-id="1cf92-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cf92-126">RELATED LINKS</span></span>

[<span data-ttu-id="1cf92-127">AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1cf92-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="1cf92-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1cf92-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


