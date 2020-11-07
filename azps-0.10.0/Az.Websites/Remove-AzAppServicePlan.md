---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794964"
---
# <span data-ttu-id="6ee1a-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ee1a-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="6ee1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ee1a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee1a-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="6ee1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ee1a-104">SYNTAX</span></span>

### <span data-ttu-id="6ee1a-105">S1</span><span class="sxs-lookup"><span data-stu-id="6ee1a-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee1a-106">S2</span><span class="sxs-lookup"><span data-stu-id="6ee1a-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ee1a-107">說明</span><span class="sxs-lookup"><span data-stu-id="6ee1a-107">DESCRIPTION</span></span>
<span data-ttu-id="6ee1a-108">**AzAppServicePlan** Cmdlet 會移除 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="6ee1a-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ee1a-109">EXAMPLES</span></span>

### <span data-ttu-id="6ee1a-110">範例1：移除 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="6ee1a-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="6ee1a-111">這個命令會從屬於名為「預設-Web-WestUS」的資源群組中，移除名為 ContosoASP 的 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6ee1a-112">參數</span><span class="sxs-lookup"><span data-stu-id="6ee1a-112">PARAMETERS</span></span>

### <span data-ttu-id="6ee1a-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ee1a-113">-AppServicePlan</span></span>
<span data-ttu-id="6ee1a-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="6ee1a-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee1a-115">-DefaultProfile</span></span>
<span data-ttu-id="6ee1a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee1a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6ee1a-117">-Force</span></span>
<span data-ttu-id="6ee1a-118">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="6ee1a-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="6ee1a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ee1a-119">-Name</span></span>
<span data-ttu-id="6ee1a-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="6ee1a-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee1a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee1a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ee1a-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6ee1a-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee1a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="6ee1a-123">-Confirm</span></span>
<span data-ttu-id="6ee1a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee1a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee1a-125">-WhatIf</span></span>
<span data-ttu-id="6ee1a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ee1a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee1a-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ee1a-128">-AsJob</span></span>
<span data-ttu-id="6ee1a-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ee1a-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ee1a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee1a-130">CommonParameters</span></span>
<span data-ttu-id="6ee1a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee1a-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ee1a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee1a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6ee1a-133">INPUTS</span></span>

### <span data-ttu-id="6ee1a-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6ee1a-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="6ee1a-135">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ee1a-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="6ee1a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6ee1a-136">OUTPUTS</span></span>

### <span data-ttu-id="6ee1a-137">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6ee1a-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="6ee1a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6ee1a-138">NOTES</span></span>

## <span data-ttu-id="6ee1a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ee1a-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ee1a-140">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ee1a-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="6ee1a-141">新-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ee1a-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="6ee1a-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ee1a-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


