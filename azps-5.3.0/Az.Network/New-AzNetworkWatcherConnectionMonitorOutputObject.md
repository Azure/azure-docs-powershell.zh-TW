---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288703"
---
# <span data-ttu-id="93c7f-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="93c7f-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="93c7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="93c7f-103">建立連線監視輸出目的地物件。</span><span class="sxs-lookup"><span data-stu-id="93c7f-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="93c7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="93c7f-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93c7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="93c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="93c7f-106">New-AzNetworkWatcherConnectionMonitorOutputObject Cmdlet 會建立連接監視器輸出目的地物件。</span><span class="sxs-lookup"><span data-stu-id="93c7f-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="93c7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="93c7f-107">EXAMPLES</span></span>

### <span data-ttu-id="93c7f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="93c7f-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="93c7f-109">類型： "workspace" WorkspaceSettings： {"WorkspaceResourceId"： "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="93c7f-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="93c7f-110">參數</span><span class="sxs-lookup"><span data-stu-id="93c7f-110">PARAMETERS</span></span>

### <span data-ttu-id="93c7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c7f-111">-DefaultProfile</span></span>
<span data-ttu-id="93c7f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93c7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c7f-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="93c7f-113">-OutputType</span></span>
<span data-ttu-id="93c7f-114">[連線監視器] 輸出目的地類型。</span><span class="sxs-lookup"><span data-stu-id="93c7f-114">Connection monitor output destination type.</span></span> <span data-ttu-id="93c7f-115">目前只 \" 支援工作區 \" 。</span><span class="sxs-lookup"><span data-stu-id="93c7f-115">Currently, only \"Workspace\" is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c7f-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="93c7f-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="93c7f-117">Log analytics 工作區資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="93c7f-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="93c7f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="93c7f-118">-Confirm</span></span>
<span data-ttu-id="93c7f-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93c7f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c7f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c7f-120">-WhatIf</span></span>
<span data-ttu-id="93c7f-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93c7f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c7f-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93c7f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c7f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c7f-123">CommonParameters</span></span>
<span data-ttu-id="93c7f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93c7f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c7f-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93c7f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c7f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="93c7f-126">INPUTS</span></span>

### <span data-ttu-id="93c7f-127">所有</span><span class="sxs-lookup"><span data-stu-id="93c7f-127">None</span></span>

## <span data-ttu-id="93c7f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="93c7f-128">OUTPUTS</span></span>

### <span data-ttu-id="93c7f-129">PSNetworkWatcherConnectionMonitorOutputObject 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="93c7f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="93c7f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="93c7f-130">NOTES</span></span>

## <span data-ttu-id="93c7f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="93c7f-131">RELATED LINKS</span></span>
