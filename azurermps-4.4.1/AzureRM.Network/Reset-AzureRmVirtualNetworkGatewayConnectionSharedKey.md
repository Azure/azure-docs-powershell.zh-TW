---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457539"
---
# <span data-ttu-id="569a1-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="569a1-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="569a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="569a1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="569a1-103">句法</span><span class="sxs-lookup"><span data-stu-id="569a1-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="569a1-104">說明</span><span class="sxs-lookup"><span data-stu-id="569a1-104">DESCRIPTION</span></span>

## <span data-ttu-id="569a1-105">示例</span><span class="sxs-lookup"><span data-stu-id="569a1-105">EXAMPLES</span></span>

## <span data-ttu-id="569a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="569a1-106">PARAMETERS</span></span>

### <span data-ttu-id="569a1-107">-Force</span><span class="sxs-lookup"><span data-stu-id="569a1-107">-Force</span></span>
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

### <span data-ttu-id="569a1-108">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="569a1-108">-KeyLength</span></span>
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

### <span data-ttu-id="569a1-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="569a1-109">-Name</span></span>
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

### <span data-ttu-id="569a1-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569a1-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="569a1-111">-確認</span><span class="sxs-lookup"><span data-stu-id="569a1-111">-Confirm</span></span>
<span data-ttu-id="569a1-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="569a1-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="569a1-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569a1-113">-WhatIf</span></span>
<span data-ttu-id="569a1-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="569a1-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="569a1-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="569a1-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="569a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569a1-116">-DefaultProfile</span></span>
<span data-ttu-id="569a1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="569a1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569a1-118">CommonParameters</span></span>
<span data-ttu-id="569a1-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="569a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569a1-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="569a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569a1-121">輸入</span><span class="sxs-lookup"><span data-stu-id="569a1-121">INPUTS</span></span>

## <span data-ttu-id="569a1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="569a1-122">OUTPUTS</span></span>

### <span data-ttu-id="569a1-123">System.object</span><span class="sxs-lookup"><span data-stu-id="569a1-123">System.String</span></span>

## <span data-ttu-id="569a1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="569a1-124">NOTES</span></span>

## <span data-ttu-id="569a1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="569a1-125">RELATED LINKS</span></span>

[<span data-ttu-id="569a1-126">AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="569a1-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="569a1-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="569a1-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


