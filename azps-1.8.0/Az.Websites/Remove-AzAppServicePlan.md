---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: f541ac58fe8512d67fab1755cfededc8839388e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614264"
---
# <span data-ttu-id="e5fbd-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5fbd-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="e5fbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fbd-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="e5fbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5fbd-104">SYNTAX</span></span>

### <span data-ttu-id="e5fbd-105">S1</span><span class="sxs-lookup"><span data-stu-id="e5fbd-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5fbd-106">S2</span><span class="sxs-lookup"><span data-stu-id="e5fbd-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5fbd-107">說明</span><span class="sxs-lookup"><span data-stu-id="e5fbd-107">DESCRIPTION</span></span>
<span data-ttu-id="e5fbd-108">**AzAppServicePlan** Cmdlet 會移除 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="e5fbd-109">示例</span><span class="sxs-lookup"><span data-stu-id="e5fbd-109">EXAMPLES</span></span>

### <span data-ttu-id="e5fbd-110">範例1：移除 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="e5fbd-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="e5fbd-111">這個命令會從屬於名為「預設-Web-WestUS」的資源群組中，移除名為 ContosoASP 的 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e5fbd-112">參數</span><span class="sxs-lookup"><span data-stu-id="e5fbd-112">PARAMETERS</span></span>

### <span data-ttu-id="e5fbd-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5fbd-113">-AppServicePlan</span></span>
<span data-ttu-id="e5fbd-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="e5fbd-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="e5fbd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5fbd-115">-AsJob</span></span>
<span data-ttu-id="e5fbd-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5fbd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5fbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fbd-117">-DefaultProfile</span></span>
<span data-ttu-id="e5fbd-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5fbd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e5fbd-119">-Force</span></span>
<span data-ttu-id="e5fbd-120">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="e5fbd-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e5fbd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5fbd-121">-Name</span></span>
<span data-ttu-id="e5fbd-122">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="e5fbd-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="e5fbd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fbd-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5fbd-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e5fbd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e5fbd-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e5fbd-125">-Confirm</span></span>
<span data-ttu-id="e5fbd-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fbd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fbd-127">-WhatIf</span></span>
<span data-ttu-id="e5fbd-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5fbd-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fbd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fbd-130">CommonParameters</span></span>
<span data-ttu-id="e5fbd-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fbd-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5fbd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fbd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e5fbd-133">INPUTS</span></span>

### <span data-ttu-id="e5fbd-134">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="e5fbd-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="e5fbd-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e5fbd-135">OUTPUTS</span></span>

### <span data-ttu-id="e5fbd-136">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e5fbd-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e5fbd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e5fbd-137">NOTES</span></span>

## <span data-ttu-id="e5fbd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5fbd-138">RELATED LINKS</span></span>

[<span data-ttu-id="e5fbd-139">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5fbd-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="e5fbd-140">新-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5fbd-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="e5fbd-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5fbd-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

