---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906442"
---
# <span data-ttu-id="ab484-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="ab484-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="ab484-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab484-102">SYNOPSIS</span></span>
<span data-ttu-id="ab484-103">移除應用程式服務環境。</span><span class="sxs-lookup"><span data-stu-id="ab484-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="ab484-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab484-104">SYNTAX</span></span>

### <span data-ttu-id="ab484-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab484-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab484-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab484-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab484-107">描述</span><span class="sxs-lookup"><span data-stu-id="ab484-107">DESCRIPTION</span></span>
<span data-ttu-id="ab484-108">**Remove-AzAppServiceEnvironment** Cmdlet 會移除應用程式服務環境。</span><span class="sxs-lookup"><span data-stu-id="ab484-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="ab484-109">刪除 ASE 之前，必須先刪除任何應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="ab484-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="ab484-110">例子</span><span class="sxs-lookup"><span data-stu-id="ab484-110">EXAMPLES</span></span>

### <span data-ttu-id="ab484-111">範例 1：刪除應用程式服務環境</span><span class="sxs-lookup"><span data-stu-id="ab484-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="ab484-112">刪除應用程式服務環境</span><span class="sxs-lookup"><span data-stu-id="ab484-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="ab484-113">參數</span><span class="sxs-lookup"><span data-stu-id="ab484-113">PARAMETERS</span></span>

### <span data-ttu-id="ab484-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab484-114">-AsJob</span></span>
<span data-ttu-id="ab484-115">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ab484-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ab484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab484-116">-DefaultProfile</span></span>
<span data-ttu-id="ab484-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab484-118">-強制</span><span class="sxs-lookup"><span data-stu-id="ab484-118">-Force</span></span>
<span data-ttu-id="ab484-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="ab484-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab484-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab484-120">-InputObject</span></span>
<span data-ttu-id="ab484-121">應用程式服務環境物件</span><span class="sxs-lookup"><span data-stu-id="ab484-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab484-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab484-122">-Name</span></span>
<span data-ttu-id="ab484-123">應用程式服務環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab484-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab484-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab484-124">-PassThru</span></span>
<span data-ttu-id="ab484-125">退貨狀態。</span><span class="sxs-lookup"><span data-stu-id="ab484-125">Return status.</span></span>

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

### <span data-ttu-id="ab484-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab484-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab484-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab484-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab484-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ab484-128">-Confirm</span></span>
<span data-ttu-id="ab484-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ab484-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab484-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab484-130">-WhatIf</span></span>
<span data-ttu-id="ab484-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab484-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab484-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab484-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab484-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab484-133">CommonParameters</span></span>
<span data-ttu-id="ab484-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab484-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab484-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab484-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab484-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ab484-136">INPUTS</span></span>

### <span data-ttu-id="ab484-137">沒有</span><span class="sxs-lookup"><span data-stu-id="ab484-137">None</span></span>

## <span data-ttu-id="ab484-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ab484-138">OUTPUTS</span></span>

### <span data-ttu-id="ab484-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="ab484-139">System.Object</span></span>
## <span data-ttu-id="ab484-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ab484-140">NOTES</span></span>

## <span data-ttu-id="ab484-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab484-141">RELATED LINKS</span></span>

[<span data-ttu-id="ab484-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="ab484-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="ab484-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="ab484-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="ab484-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="ab484-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)