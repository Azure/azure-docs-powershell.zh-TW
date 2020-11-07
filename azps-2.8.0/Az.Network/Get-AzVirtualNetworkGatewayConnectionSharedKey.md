---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 071843c47ea3a8f97125746aa80fdb90eb1cb566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790021"
---
# <span data-ttu-id="89a3a-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="89a3a-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="89a3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="89a3a-103">顯示連線所用的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="89a3a-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="89a3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="89a3a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89a3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="89a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="89a3a-106">顯示連線所用的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="89a3a-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="89a3a-107">示例</span><span class="sxs-lookup"><span data-stu-id="89a3a-107">EXAMPLES</span></span>

### <span data-ttu-id="89a3a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="89a3a-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="89a3a-109">參數</span><span class="sxs-lookup"><span data-stu-id="89a3a-109">PARAMETERS</span></span>

### <span data-ttu-id="89a3a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a3a-110">-DefaultProfile</span></span>
<span data-ttu-id="89a3a-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89a3a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89a3a-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="89a3a-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a3a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a3a-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="89a3a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a3a-114">CommonParameters</span></span>
<span data-ttu-id="89a3a-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89a3a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a3a-116">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89a3a-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a3a-117">輸入</span><span class="sxs-lookup"><span data-stu-id="89a3a-117">INPUTS</span></span>

### <span data-ttu-id="89a3a-118">System.object</span><span class="sxs-lookup"><span data-stu-id="89a3a-118">System.String</span></span>

## <span data-ttu-id="89a3a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="89a3a-119">OUTPUTS</span></span>

### <span data-ttu-id="89a3a-120">System.object</span><span class="sxs-lookup"><span data-stu-id="89a3a-120">System.String</span></span>

## <span data-ttu-id="89a3a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="89a3a-121">NOTES</span></span>

## <span data-ttu-id="89a3a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="89a3a-122">RELATED LINKS</span></span>

[<span data-ttu-id="89a3a-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="89a3a-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="89a3a-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="89a3a-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
