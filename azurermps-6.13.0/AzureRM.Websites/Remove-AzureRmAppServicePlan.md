---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445304"
---
# <span data-ttu-id="a264f-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a264f-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="a264f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a264f-102">SYNOPSIS</span></span>
<span data-ttu-id="a264f-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="a264f-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a264f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a264f-104">SYNTAX</span></span>

### <span data-ttu-id="a264f-105">S1</span><span class="sxs-lookup"><span data-stu-id="a264f-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a264f-106">S2</span><span class="sxs-lookup"><span data-stu-id="a264f-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a264f-107">說明</span><span class="sxs-lookup"><span data-stu-id="a264f-107">DESCRIPTION</span></span>
<span data-ttu-id="a264f-108">**AzureRmAppServicePlan** Cmdlet 會移除 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="a264f-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="a264f-109">示例</span><span class="sxs-lookup"><span data-stu-id="a264f-109">EXAMPLES</span></span>

### <span data-ttu-id="a264f-110">範例1：移除 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="a264f-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a264f-111">這個命令會從屬於名為「預設-Web-WestUS」的資源群組中，移除名為 ContosoASP 的 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="a264f-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a264f-112">參數</span><span class="sxs-lookup"><span data-stu-id="a264f-112">PARAMETERS</span></span>

### <span data-ttu-id="a264f-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a264f-113">-AppServicePlan</span></span>
<span data-ttu-id="a264f-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="a264f-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="a264f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a264f-115">-AsJob</span></span>
<span data-ttu-id="a264f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a264f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a264f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a264f-117">-DefaultProfile</span></span>
<span data-ttu-id="a264f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a264f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a264f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a264f-119">-Force</span></span>
<span data-ttu-id="a264f-120">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="a264f-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="a264f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a264f-121">-Name</span></span>
<span data-ttu-id="a264f-122">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="a264f-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="a264f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a264f-123">-ResourceGroupName</span></span>
<span data-ttu-id="a264f-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a264f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a264f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a264f-125">-Confirm</span></span>
<span data-ttu-id="a264f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a264f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a264f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a264f-127">-WhatIf</span></span>
<span data-ttu-id="a264f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a264f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a264f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a264f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a264f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a264f-130">CommonParameters</span></span>
<span data-ttu-id="a264f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a264f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a264f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a264f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a264f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a264f-133">INPUTS</span></span>

### <span data-ttu-id="a264f-134">AppServicePlan 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="a264f-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="a264f-135">參數： AppServicePlan (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a264f-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="a264f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a264f-136">OUTPUTS</span></span>

### <span data-ttu-id="a264f-137">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a264f-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a264f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a264f-138">NOTES</span></span>

## <span data-ttu-id="a264f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a264f-139">RELATED LINKS</span></span>

[<span data-ttu-id="a264f-140">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a264f-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="a264f-141">新-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a264f-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="a264f-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a264f-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


