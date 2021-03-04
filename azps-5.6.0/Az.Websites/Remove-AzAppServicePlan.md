---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: acd6b0735cb0ecf38ecef3448d02c4349954f405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910801"
---
# <span data-ttu-id="fe04e-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe04e-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="fe04e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fe04e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe04e-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="fe04e-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="fe04e-104">語法</span><span class="sxs-lookup"><span data-stu-id="fe04e-104">SYNTAX</span></span>

### <span data-ttu-id="fe04e-105">S1</span><span class="sxs-lookup"><span data-stu-id="fe04e-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe04e-106">S2</span><span class="sxs-lookup"><span data-stu-id="fe04e-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe04e-107">描述</span><span class="sxs-lookup"><span data-stu-id="fe04e-107">DESCRIPTION</span></span>
<span data-ttu-id="fe04e-108">**Remove-AzAppServicePlan** Cmdlet 會移除 Azure 應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="fe04e-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="fe04e-109">例子</span><span class="sxs-lookup"><span data-stu-id="fe04e-109">EXAMPLES</span></span>

### <span data-ttu-id="fe04e-110">範例 1：移除應用程式服務計畫</span><span class="sxs-lookup"><span data-stu-id="fe04e-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="fe04e-111">此命令會移除名稱為 ContosoASP 的 Azure 應用程式服務計畫，該計畫屬於名為 Default-Web-WestUS 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="fe04e-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fe04e-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe04e-112">PARAMETERS</span></span>

### <span data-ttu-id="fe04e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe04e-113">-AppServicePlan</span></span>
<span data-ttu-id="fe04e-114">應用程式服務計畫物件</span><span class="sxs-lookup"><span data-stu-id="fe04e-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe04e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe04e-115">-AsJob</span></span>
<span data-ttu-id="fe04e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe04e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe04e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe04e-117">-DefaultProfile</span></span>
<span data-ttu-id="fe04e-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe04e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe04e-119">-強制</span><span class="sxs-lookup"><span data-stu-id="fe04e-119">-Force</span></span>
<span data-ttu-id="fe04e-120">強制移除選項</span><span class="sxs-lookup"><span data-stu-id="fe04e-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="fe04e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe04e-121">-Name</span></span>
<span data-ttu-id="fe04e-122">應用程式服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="fe04e-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe04e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe04e-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe04e-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="fe04e-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe04e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="fe04e-125">-Confirm</span></span>
<span data-ttu-id="fe04e-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fe04e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe04e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe04e-127">-WhatIf</span></span>
<span data-ttu-id="fe04e-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe04e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe04e-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe04e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe04e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe04e-130">CommonParameters</span></span>
<span data-ttu-id="fe04e-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fe04e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe04e-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fe04e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe04e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fe04e-133">INPUTS</span></span>

### <span data-ttu-id="fe04e-134">Microsoft.Azure.Commands.WebApps.models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe04e-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="fe04e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fe04e-135">OUTPUTS</span></span>

### <span data-ttu-id="fe04e-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fe04e-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="fe04e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fe04e-137">NOTES</span></span>

## <span data-ttu-id="fe04e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe04e-138">RELATED LINKS</span></span>

[<span data-ttu-id="fe04e-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe04e-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="fe04e-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe04e-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="fe04e-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe04e-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


