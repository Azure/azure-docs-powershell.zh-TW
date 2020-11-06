---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449762"
---
# <span data-ttu-id="2065d-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="2065d-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="2065d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2065d-102">SYNOPSIS</span></span>
<span data-ttu-id="2065d-103">刪除 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2065d-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2065d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2065d-104">SYNTAX</span></span>

### <span data-ttu-id="2065d-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2065d-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2065d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="2065d-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2065d-107">說明</span><span class="sxs-lookup"><span data-stu-id="2065d-107">DESCRIPTION</span></span>
<span data-ttu-id="2065d-108">刪除由資源群組和名稱所參照的 Azure 電腦學習 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2065d-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="2065d-109">示例</span><span class="sxs-lookup"><span data-stu-id="2065d-109">EXAMPLES</span></span>

### <span data-ttu-id="2065d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2065d-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="2065d-111">參數</span><span class="sxs-lookup"><span data-stu-id="2065d-111">PARAMETERS</span></span>

### <span data-ttu-id="2065d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2065d-112">-DefaultProfile</span></span>
<span data-ttu-id="2065d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2065d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2065d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2065d-114">-Force</span></span>
<span data-ttu-id="2065d-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2065d-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2065d-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="2065d-116">-MlWebService</span></span>
<span data-ttu-id="2065d-117">要移除的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="2065d-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2065d-118">-Name</span></span>
<span data-ttu-id="2065d-119">要移除的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="2065d-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2065d-120">-ResourceGroupName</span></span>
<span data-ttu-id="2065d-121">Web 服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="2065d-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-122">-確認</span><span class="sxs-lookup"><span data-stu-id="2065d-122">-Confirm</span></span>
<span data-ttu-id="2065d-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2065d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2065d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2065d-124">-WhatIf</span></span>
<span data-ttu-id="2065d-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2065d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2065d-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2065d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2065d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2065d-127">CommonParameters</span></span>
<span data-ttu-id="2065d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2065d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2065d-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2065d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2065d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2065d-130">INPUTS</span></span>

### <span data-ttu-id="2065d-131">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="2065d-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="2065d-132">參數： MlWebService (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2065d-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="2065d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2065d-133">OUTPUTS</span></span>

### <span data-ttu-id="2065d-134">System.void</span><span class="sxs-lookup"><span data-stu-id="2065d-134">System.Void</span></span>

## <span data-ttu-id="2065d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2065d-135">NOTES</span></span>
<span data-ttu-id="2065d-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="2065d-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2065d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2065d-137">RELATED LINKS</span></span>
