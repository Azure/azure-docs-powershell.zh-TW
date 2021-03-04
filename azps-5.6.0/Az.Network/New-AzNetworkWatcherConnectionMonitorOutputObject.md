---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903546"
---
# <span data-ttu-id="0a5b7-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="0a5b7-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="0a5b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5b7-103">建立連接監視器輸出目的物件。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="0a5b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a5b7-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a5b7-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a5b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0a5b7-106">Cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject建立連接監視器輸出目的物件。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="0a5b7-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a5b7-107">EXAMPLES</span></span>

### <span data-ttu-id="0a5b7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0a5b7-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="0a5b7-109">類型 ： "workspace" WorkspaceSettings ： { "WorkspaceResourceId"： "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="0a5b7-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="0a5b7-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a5b7-110">PARAMETERS</span></span>

### <span data-ttu-id="0a5b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5b7-111">-DefaultProfile</span></span>
<span data-ttu-id="0a5b7-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a5b7-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="0a5b7-113">-OutputType</span></span>
<span data-ttu-id="0a5b7-114">連接監視器輸出目的類型。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-114">Connection monitor output destination type.</span></span> <span data-ttu-id="0a5b7-115">目前僅 \" 支援工作區 \" 。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="0a5b7-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0a5b7-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="0a5b7-117">記錄分析工作區資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="0a5b7-118">-確認</span><span class="sxs-lookup"><span data-stu-id="0a5b7-118">-Confirm</span></span>
<span data-ttu-id="0a5b7-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5b7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5b7-120">-WhatIf</span></span>
<span data-ttu-id="0a5b7-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5b7-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5b7-123">CommonParameters</span></span>
<span data-ttu-id="0a5b7-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a5b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5b7-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a5b7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5b7-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0a5b7-126">INPUTS</span></span>

### <span data-ttu-id="0a5b7-127">沒有</span><span class="sxs-lookup"><span data-stu-id="0a5b7-127">None</span></span>

## <span data-ttu-id="0a5b7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0a5b7-128">OUTPUTS</span></span>

### <span data-ttu-id="0a5b7-129">Microsoft.Azure.Commands.Network.models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="0a5b7-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="0a5b7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0a5b7-130">NOTES</span></span>

## <span data-ttu-id="0a5b7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a5b7-131">RELATED LINKS</span></span>
