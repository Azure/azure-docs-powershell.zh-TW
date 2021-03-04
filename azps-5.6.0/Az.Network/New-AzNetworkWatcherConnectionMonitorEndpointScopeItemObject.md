---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: 298586f11bba29ce44e78bc3c19d4d9fc6be21f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903553"
---
# <span data-ttu-id="6fdaf-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="6fdaf-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="6fdaf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6fdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdaf-103">建立連接監視器端點範圍專案。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="6fdaf-104">語法</span><span class="sxs-lookup"><span data-stu-id="6fdaf-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fdaf-105">描述</span><span class="sxs-lookup"><span data-stu-id="6fdaf-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdaf-106">Cmdlet New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject建立端點範圍專案。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="6fdaf-107">例子</span><span class="sxs-lookup"><span data-stu-id="6fdaf-107">EXAMPLES</span></span>

### <span data-ttu-id="6fdaf-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6fdaf-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="6fdaf-109">參數</span><span class="sxs-lookup"><span data-stu-id="6fdaf-109">PARAMETERS</span></span>

### <span data-ttu-id="6fdaf-110">-Address</span><span class="sxs-lookup"><span data-stu-id="6fdaf-110">-Address</span></span>
<span data-ttu-id="6fdaf-111">範圍專案的位址。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="6fdaf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdaf-112">-DefaultProfile</span></span>
<span data-ttu-id="6fdaf-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdaf-114">-確認</span><span class="sxs-lookup"><span data-stu-id="6fdaf-114">-Confirm</span></span>
<span data-ttu-id="6fdaf-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdaf-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdaf-116">-WhatIf</span></span>
<span data-ttu-id="6fdaf-117">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fdaf-118">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdaf-119">CommonParameters</span></span>
<span data-ttu-id="6fdaf-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6fdaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdaf-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fdaf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdaf-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6fdaf-122">INPUTS</span></span>

### <span data-ttu-id="6fdaf-123">沒有</span><span class="sxs-lookup"><span data-stu-id="6fdaf-123">None</span></span>

## <span data-ttu-id="6fdaf-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6fdaf-124">OUTPUTS</span></span>

### <span data-ttu-id="6fdaf-125">Microsoft.Azure.Commands.Network.models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="6fdaf-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="6fdaf-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6fdaf-126">NOTES</span></span>

## <span data-ttu-id="6fdaf-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fdaf-127">RELATED LINKS</span></span>
