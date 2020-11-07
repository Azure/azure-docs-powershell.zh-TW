---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: ddd1ab1ce748def345604447988d0fc53b5989fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625616"
---
# <span data-ttu-id="e046f-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e046f-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="e046f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e046f-102">SYNOPSIS</span></span>
<span data-ttu-id="e046f-103">移除路由表。</span><span class="sxs-lookup"><span data-stu-id="e046f-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e046f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e046f-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e046f-105">說明</span><span class="sxs-lookup"><span data-stu-id="e046f-105">DESCRIPTION</span></span>
<span data-ttu-id="e046f-106">**AzureRmRouteTable** Cmdlet 會移除 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="e046f-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="e046f-107">示例</span><span class="sxs-lookup"><span data-stu-id="e046f-107">EXAMPLES</span></span>

### <span data-ttu-id="e046f-108">範例1：移除路由資料表</span><span class="sxs-lookup"><span data-stu-id="e046f-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e046f-109">這個命令會移除名為 ResourceGroup11 的資源群組中名為 RouteTable01 的路由表。</span><span class="sxs-lookup"><span data-stu-id="e046f-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="e046f-110">Cmdlet 會在您移除資料表之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e046f-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="e046f-111">參數</span><span class="sxs-lookup"><span data-stu-id="e046f-111">PARAMETERS</span></span>

### <span data-ttu-id="e046f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e046f-112">-AsJob</span></span>
<span data-ttu-id="e046f-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e046f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e046f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e046f-114">-DefaultProfile</span></span>
<span data-ttu-id="e046f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e046f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e046f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e046f-116">-Force</span></span>
<span data-ttu-id="e046f-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e046f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e046f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e046f-118">-Name</span></span>
<span data-ttu-id="e046f-119">指定此 Cmdlet 移除之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="e046f-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e046f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e046f-120">-PassThru</span></span>
<span data-ttu-id="e046f-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e046f-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e046f-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e046f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e046f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e046f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e046f-124">指定包含此 Cmdlet 移除之路由表之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e046f-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e046f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e046f-125">-Confirm</span></span>
<span data-ttu-id="e046f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e046f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e046f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e046f-127">-WhatIf</span></span>
<span data-ttu-id="e046f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e046f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e046f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e046f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e046f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e046f-130">CommonParameters</span></span>
<span data-ttu-id="e046f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e046f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e046f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e046f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e046f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e046f-133">INPUTS</span></span>

### <span data-ttu-id="e046f-134">所有</span><span class="sxs-lookup"><span data-stu-id="e046f-134">None</span></span>
<span data-ttu-id="e046f-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e046f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e046f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e046f-136">OUTPUTS</span></span>

## <span data-ttu-id="e046f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e046f-137">NOTES</span></span>

## <span data-ttu-id="e046f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e046f-138">RELATED LINKS</span></span>

[<span data-ttu-id="e046f-139">AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e046f-139">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="e046f-140">新-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e046f-140">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="e046f-141">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e046f-141">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


