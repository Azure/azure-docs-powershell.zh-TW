---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: 17cd4ab4e60156c1ab4d6dd4357e638ddaf2c5a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624008"
---
# <span data-ttu-id="50a19-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="50a19-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="50a19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50a19-102">SYNOPSIS</span></span>
<span data-ttu-id="50a19-103">移除路由表。</span><span class="sxs-lookup"><span data-stu-id="50a19-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50a19-104">句法</span><span class="sxs-lookup"><span data-stu-id="50a19-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a19-105">說明</span><span class="sxs-lookup"><span data-stu-id="50a19-105">DESCRIPTION</span></span>
<span data-ttu-id="50a19-106">**AzureRmRouteTable** Cmdlet 會移除 Azure 路由表。</span><span class="sxs-lookup"><span data-stu-id="50a19-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="50a19-107">示例</span><span class="sxs-lookup"><span data-stu-id="50a19-107">EXAMPLES</span></span>

### <span data-ttu-id="50a19-108">範例1：移除路由資料表</span><span class="sxs-lookup"><span data-stu-id="50a19-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="50a19-109">這個命令會移除名為 ResourceGroup11 的資源群組中名為 RouteTable01 的路由表。</span><span class="sxs-lookup"><span data-stu-id="50a19-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="50a19-110">Cmdlet 會在您移除資料表之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50a19-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="50a19-111">參數</span><span class="sxs-lookup"><span data-stu-id="50a19-111">PARAMETERS</span></span>

### <span data-ttu-id="50a19-112">-Force</span><span class="sxs-lookup"><span data-stu-id="50a19-112">-Force</span></span>
<span data-ttu-id="50a19-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="50a19-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50a19-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="50a19-114">-Name</span></span>
<span data-ttu-id="50a19-115">指定此 Cmdlet 移除之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="50a19-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="50a19-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50a19-116">-PassThru</span></span>
<span data-ttu-id="50a19-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="50a19-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="50a19-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="50a19-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50a19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a19-119">-ResourceGroupName</span></span>
<span data-ttu-id="50a19-120">指定包含此 Cmdlet 移除之路由表之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50a19-120">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="50a19-121">-確認</span><span class="sxs-lookup"><span data-stu-id="50a19-121">-Confirm</span></span>
<span data-ttu-id="50a19-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50a19-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a19-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a19-123">-WhatIf</span></span>
<span data-ttu-id="50a19-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50a19-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a19-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50a19-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a19-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a19-126">-DefaultProfile</span></span>
<span data-ttu-id="50a19-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50a19-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50a19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a19-128">CommonParameters</span></span>
<span data-ttu-id="50a19-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50a19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a19-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50a19-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a19-131">輸入</span><span class="sxs-lookup"><span data-stu-id="50a19-131">INPUTS</span></span>

## <span data-ttu-id="50a19-132">輸出</span><span class="sxs-lookup"><span data-stu-id="50a19-132">OUTPUTS</span></span>

## <span data-ttu-id="50a19-133">筆記</span><span class="sxs-lookup"><span data-stu-id="50a19-133">NOTES</span></span>

## <span data-ttu-id="50a19-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="50a19-134">RELATED LINKS</span></span>

[<span data-ttu-id="50a19-135">AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="50a19-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="50a19-136">新-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="50a19-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="50a19-137">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="50a19-137">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


