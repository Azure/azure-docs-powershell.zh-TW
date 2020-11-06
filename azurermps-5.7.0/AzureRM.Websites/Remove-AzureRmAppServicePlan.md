---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447556"
---
# <span data-ttu-id="2d55b-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d55b-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2d55b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d55b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d55b-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="2d55b-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d55b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d55b-104">SYNTAX</span></span>

### <span data-ttu-id="2d55b-105">S1</span><span class="sxs-lookup"><span data-stu-id="2d55b-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d55b-106">S2</span><span class="sxs-lookup"><span data-stu-id="2d55b-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d55b-107">說明</span><span class="sxs-lookup"><span data-stu-id="2d55b-107">DESCRIPTION</span></span>
<span data-ttu-id="2d55b-108">**AzureRmAppServicePlan** Cmdlet 會移除 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="2d55b-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="2d55b-109">示例</span><span class="sxs-lookup"><span data-stu-id="2d55b-109">EXAMPLES</span></span>

### <span data-ttu-id="2d55b-110">範例1：移除 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="2d55b-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2d55b-111">這個命令會從屬於名為「預設-Web-WestUS」的資源群組中，移除名為 ContosoASP 的 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="2d55b-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2d55b-112">參數</span><span class="sxs-lookup"><span data-stu-id="2d55b-112">PARAMETERS</span></span>

### <span data-ttu-id="2d55b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d55b-113">-AppServicePlan</span></span>
<span data-ttu-id="2d55b-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="2d55b-114">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d55b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d55b-115">-DefaultProfile</span></span>
<span data-ttu-id="2d55b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d55b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d55b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d55b-117">-Force</span></span>
<span data-ttu-id="2d55b-118">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="2d55b-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2d55b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d55b-119">-Name</span></span>
<span data-ttu-id="2d55b-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="2d55b-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="2d55b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d55b-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d55b-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2d55b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2d55b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2d55b-123">-Confirm</span></span>
<span data-ttu-id="2d55b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d55b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d55b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d55b-125">-WhatIf</span></span>
<span data-ttu-id="2d55b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d55b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d55b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d55b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d55b-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d55b-128">-AsJob</span></span>
<span data-ttu-id="2d55b-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d55b-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d55b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d55b-130">CommonParameters</span></span>
<span data-ttu-id="2d55b-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d55b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d55b-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d55b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d55b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2d55b-133">INPUTS</span></span>

### <span data-ttu-id="2d55b-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2d55b-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2d55b-135">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2d55b-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2d55b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2d55b-136">OUTPUTS</span></span>

### <span data-ttu-id="2d55b-137">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2d55b-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2d55b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2d55b-138">NOTES</span></span>

## <span data-ttu-id="2d55b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d55b-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d55b-140">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d55b-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="2d55b-141">新-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d55b-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="2d55b-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d55b-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


