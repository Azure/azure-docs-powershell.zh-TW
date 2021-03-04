---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 46e9ae8f4b6b4bb954bca158adb82c0d821d67eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916129"
---
# <span data-ttu-id="ae31f-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ae31f-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="ae31f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae31f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae31f-103">刪除 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="ae31f-103">Deletes a web service.</span></span>

## <span data-ttu-id="ae31f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae31f-104">SYNTAX</span></span>

### <span data-ttu-id="ae31f-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae31f-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae31f-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ae31f-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae31f-107">描述</span><span class="sxs-lookup"><span data-stu-id="ae31f-107">DESCRIPTION</span></span>
<span data-ttu-id="ae31f-108">刪除資源組和名稱所參照的 Azure 機器學習 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="ae31f-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="ae31f-109">例子</span><span class="sxs-lookup"><span data-stu-id="ae31f-109">EXAMPLES</span></span>

### <span data-ttu-id="ae31f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ae31f-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="ae31f-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae31f-111">PARAMETERS</span></span>

### <span data-ttu-id="ae31f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae31f-112">-DefaultProfile</span></span>
<span data-ttu-id="ae31f-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ae31f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae31f-114">-強制</span><span class="sxs-lookup"><span data-stu-id="ae31f-114">-Force</span></span>
<span data-ttu-id="ae31f-115">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="ae31f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ae31f-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="ae31f-116">-MlWebService</span></span>
<span data-ttu-id="ae31f-117">要移除的 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="ae31f-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="ae31f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae31f-118">-Name</span></span>
<span data-ttu-id="ae31f-119">要移除的 Web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ae31f-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="ae31f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae31f-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae31f-121">Web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ae31f-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="ae31f-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ae31f-122">-Confirm</span></span>
<span data-ttu-id="ae31f-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ae31f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae31f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae31f-124">-WhatIf</span></span>
<span data-ttu-id="ae31f-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae31f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae31f-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae31f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae31f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae31f-127">CommonParameters</span></span>
<span data-ttu-id="ae31f-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae31f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae31f-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ae31f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae31f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ae31f-130">INPUTS</span></span>

### <span data-ttu-id="ae31f-131">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="ae31f-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ae31f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ae31f-132">OUTPUTS</span></span>

### <span data-ttu-id="ae31f-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="ae31f-133">System.Void</span></span>

## <span data-ttu-id="ae31f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ae31f-134">NOTES</span></span>
<span data-ttu-id="ae31f-135">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="ae31f-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ae31f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae31f-136">RELATED LINKS</span></span>
