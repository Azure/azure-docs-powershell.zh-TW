---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456319"
---
# <span data-ttu-id="ab846-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab846-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ab846-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab846-102">SYNOPSIS</span></span>
<span data-ttu-id="ab846-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="ab846-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab846-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab846-104">SYNTAX</span></span>

### <span data-ttu-id="ab846-105">S1</span><span class="sxs-lookup"><span data-stu-id="ab846-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab846-106">S2</span><span class="sxs-lookup"><span data-stu-id="ab846-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab846-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab846-107">DESCRIPTION</span></span>
<span data-ttu-id="ab846-108">**AzureRmAppServicePlan** Cmdlet 會移除 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="ab846-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="ab846-109">示例</span><span class="sxs-lookup"><span data-stu-id="ab846-109">EXAMPLES</span></span>

### <span data-ttu-id="ab846-110">範例1：移除 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="ab846-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ab846-111">這個命令會從屬於名為「預設-Web-WestUS」的資源群組中，移除名為 ContosoASP 的 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="ab846-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ab846-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab846-112">PARAMETERS</span></span>

### <span data-ttu-id="ab846-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab846-113">-AppServicePlan</span></span>
<span data-ttu-id="ab846-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="ab846-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab846-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab846-115">-Force</span></span>
<span data-ttu-id="ab846-116">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="ab846-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ab846-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab846-117">-Name</span></span>
<span data-ttu-id="ab846-118">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="ab846-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="ab846-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab846-119">-ResourceGroupName</span></span>
<span data-ttu-id="ab846-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ab846-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ab846-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ab846-121">-Confirm</span></span>
<span data-ttu-id="ab846-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab846-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab846-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab846-123">-WhatIf</span></span>
<span data-ttu-id="ab846-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab846-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab846-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab846-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab846-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab846-126">-DefaultProfile</span></span>
<span data-ttu-id="ab846-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab846-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab846-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab846-128">CommonParameters</span></span>
<span data-ttu-id="ab846-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab846-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab846-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab846-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab846-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ab846-131">INPUTS</span></span>

### <span data-ttu-id="ab846-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ab846-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="ab846-133">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ab846-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="ab846-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ab846-134">OUTPUTS</span></span>

### <span data-ttu-id="ab846-135">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ab846-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ab846-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ab846-136">NOTES</span></span>

## <span data-ttu-id="ab846-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab846-137">RELATED LINKS</span></span>

[<span data-ttu-id="ab846-138">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab846-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="ab846-139">新-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab846-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="ab846-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab846-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


