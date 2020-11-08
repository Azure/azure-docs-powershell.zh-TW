---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138329"
---
# <span data-ttu-id="214bf-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="214bf-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="214bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="214bf-102">SYNOPSIS</span></span>
<span data-ttu-id="214bf-103">移除路由表。</span><span class="sxs-lookup"><span data-stu-id="214bf-103">Removes a route table.</span></span>

## <span data-ttu-id="214bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="214bf-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="214bf-105">DESCRIPTION</span></span>
<span data-ttu-id="214bf-106">**AzRouteTable** Cmdlet 會移除 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="214bf-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="214bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="214bf-107">EXAMPLES</span></span>

### <span data-ttu-id="214bf-108">範例1：移除路由資料表</span><span class="sxs-lookup"><span data-stu-id="214bf-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="214bf-109">這個命令會移除名為 ResourceGroup11 的資源群組中名為 RouteTable01 的路由表。</span><span class="sxs-lookup"><span data-stu-id="214bf-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="214bf-110">Cmdlet 會在您移除資料表之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="214bf-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="214bf-111">參數</span><span class="sxs-lookup"><span data-stu-id="214bf-111">PARAMETERS</span></span>

### <span data-ttu-id="214bf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="214bf-112">-AsJob</span></span>
<span data-ttu-id="214bf-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="214bf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="214bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214bf-114">-DefaultProfile</span></span>
<span data-ttu-id="214bf-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="214bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="214bf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="214bf-116">-Force</span></span>
<span data-ttu-id="214bf-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="214bf-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="214bf-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="214bf-118">-Name</span></span>
<span data-ttu-id="214bf-119">指定此 Cmdlet 移除之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="214bf-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="214bf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="214bf-120">-PassThru</span></span>
<span data-ttu-id="214bf-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="214bf-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="214bf-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="214bf-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="214bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="214bf-124">指定包含此 Cmdlet 移除之路由表之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="214bf-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="214bf-125">-確認</span><span class="sxs-lookup"><span data-stu-id="214bf-125">-Confirm</span></span>
<span data-ttu-id="214bf-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="214bf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214bf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214bf-127">-WhatIf</span></span>
<span data-ttu-id="214bf-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="214bf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214bf-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="214bf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214bf-130">CommonParameters</span></span>
<span data-ttu-id="214bf-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="214bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214bf-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="214bf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214bf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="214bf-133">INPUTS</span></span>

### <span data-ttu-id="214bf-134">System.object</span><span class="sxs-lookup"><span data-stu-id="214bf-134">System.String</span></span>

## <span data-ttu-id="214bf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="214bf-135">OUTPUTS</span></span>

### <span data-ttu-id="214bf-136">System.object</span><span class="sxs-lookup"><span data-stu-id="214bf-136">System.Boolean</span></span>

## <span data-ttu-id="214bf-137">筆記</span><span class="sxs-lookup"><span data-stu-id="214bf-137">NOTES</span></span>

## <span data-ttu-id="214bf-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="214bf-138">RELATED LINKS</span></span>

[<span data-ttu-id="214bf-139">AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="214bf-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="214bf-140">新-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="214bf-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="214bf-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="214bf-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


