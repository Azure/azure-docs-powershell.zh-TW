---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909897"
---
# <span data-ttu-id="98052-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="98052-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="98052-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98052-102">SYNOPSIS</span></span>
<span data-ttu-id="98052-103">獲得應用程式服務環境。</span><span class="sxs-lookup"><span data-stu-id="98052-103">Gets App Service Environment.</span></span> <span data-ttu-id="98052-104">如果只指定資源群組，它會在資源群組中返回 ASE 清單。</span><span class="sxs-lookup"><span data-stu-id="98052-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="98052-105">語法</span><span class="sxs-lookup"><span data-stu-id="98052-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98052-106">描述</span><span class="sxs-lookup"><span data-stu-id="98052-106">DESCRIPTION</span></span>
<span data-ttu-id="98052-107">**Get-AzAppServiceEnvironment** Cmdlet 會 (查詢) ASE。</span><span class="sxs-lookup"><span data-stu-id="98052-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="98052-108">例子</span><span class="sxs-lookup"><span data-stu-id="98052-108">EXAMPLES</span></span>

### <span data-ttu-id="98052-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="98052-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="98052-110">會以 <MyAseName><MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="98052-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="98052-111">參數</span><span class="sxs-lookup"><span data-stu-id="98052-111">PARAMETERS</span></span>

### <span data-ttu-id="98052-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98052-112">-DefaultProfile</span></span>
<span data-ttu-id="98052-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98052-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98052-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="98052-114">-Name</span></span>
<span data-ttu-id="98052-115">應用程式服務環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="98052-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98052-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98052-116">-ResourceGroupName</span></span>
<span data-ttu-id="98052-117">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98052-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98052-118">-確認</span><span class="sxs-lookup"><span data-stu-id="98052-118">-Confirm</span></span>
<span data-ttu-id="98052-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98052-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98052-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98052-120">-WhatIf</span></span>
<span data-ttu-id="98052-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98052-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98052-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98052-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98052-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98052-123">CommonParameters</span></span>
<span data-ttu-id="98052-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98052-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98052-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98052-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98052-126">輸入</span><span class="sxs-lookup"><span data-stu-id="98052-126">INPUTS</span></span>

### <span data-ttu-id="98052-127">沒有</span><span class="sxs-lookup"><span data-stu-id="98052-127">None</span></span>

## <span data-ttu-id="98052-128">輸出</span><span class="sxs-lookup"><span data-stu-id="98052-128">OUTPUTS</span></span>

### <span data-ttu-id="98052-129">Microsoft.Azure.Commands.WebApps.models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="98052-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="98052-130">筆記</span><span class="sxs-lookup"><span data-stu-id="98052-130">NOTES</span></span>

## <span data-ttu-id="98052-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="98052-131">RELATED LINKS</span></span>

[<span data-ttu-id="98052-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="98052-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="98052-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="98052-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="98052-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="98052-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)