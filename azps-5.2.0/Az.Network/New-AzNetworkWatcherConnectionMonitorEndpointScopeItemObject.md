---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276727"
---
# <span data-ttu-id="179db-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="179db-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="179db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="179db-102">SYNOPSIS</span></span>
<span data-ttu-id="179db-103">建立連線監視端點範圍專案。</span><span class="sxs-lookup"><span data-stu-id="179db-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="179db-104">句法</span><span class="sxs-lookup"><span data-stu-id="179db-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="179db-105">說明</span><span class="sxs-lookup"><span data-stu-id="179db-105">DESCRIPTION</span></span>
<span data-ttu-id="179db-106">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject Cmdlet 會建立端點範圍專案。</span><span class="sxs-lookup"><span data-stu-id="179db-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="179db-107">示例</span><span class="sxs-lookup"><span data-stu-id="179db-107">EXAMPLES</span></span>

### <span data-ttu-id="179db-108">範例1</span><span class="sxs-lookup"><span data-stu-id="179db-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="179db-109">參數</span><span class="sxs-lookup"><span data-stu-id="179db-109">PARAMETERS</span></span>

### <span data-ttu-id="179db-110">-位址</span><span class="sxs-lookup"><span data-stu-id="179db-110">-Address</span></span>
<span data-ttu-id="179db-111">作用中專案的位址。</span><span class="sxs-lookup"><span data-stu-id="179db-111">The address of the scope item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179db-112">-DefaultProfile</span></span>
<span data-ttu-id="179db-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="179db-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="179db-114">-確認</span><span class="sxs-lookup"><span data-stu-id="179db-114">-Confirm</span></span>
<span data-ttu-id="179db-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="179db-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179db-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="179db-116">-WhatIf</span></span>
<span data-ttu-id="179db-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="179db-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="179db-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="179db-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179db-119">CommonParameters</span></span>
<span data-ttu-id="179db-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="179db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179db-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="179db-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179db-122">輸入</span><span class="sxs-lookup"><span data-stu-id="179db-122">INPUTS</span></span>

### <span data-ttu-id="179db-123">所有</span><span class="sxs-lookup"><span data-stu-id="179db-123">None</span></span>

## <span data-ttu-id="179db-124">輸出</span><span class="sxs-lookup"><span data-stu-id="179db-124">OUTPUTS</span></span>

### <span data-ttu-id="179db-125">PSNetworkWatcherConnectionMonitorEndpointScopeItem 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="179db-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="179db-126">筆記</span><span class="sxs-lookup"><span data-stu-id="179db-126">NOTES</span></span>

## <span data-ttu-id="179db-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="179db-127">RELATED LINKS</span></span>
