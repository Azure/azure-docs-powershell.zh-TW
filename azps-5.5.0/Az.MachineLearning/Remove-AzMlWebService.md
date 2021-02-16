---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132770"
---
# <span data-ttu-id="a6e17-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="a6e17-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="a6e17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6e17-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e17-103">刪除 web 服務。</span><span class="sxs-lookup"><span data-stu-id="a6e17-103">Deletes a web service.</span></span>

## <span data-ttu-id="a6e17-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6e17-104">SYNTAX</span></span>

### <span data-ttu-id="a6e17-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6e17-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6e17-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a6e17-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e17-107">說明</span><span class="sxs-lookup"><span data-stu-id="a6e17-107">DESCRIPTION</span></span>
<span data-ttu-id="a6e17-108">刪除由資源群組和名稱所參照的 Azure 電腦學習 web 服務。</span><span class="sxs-lookup"><span data-stu-id="a6e17-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="a6e17-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6e17-109">EXAMPLES</span></span>

### <span data-ttu-id="a6e17-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a6e17-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="a6e17-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6e17-111">PARAMETERS</span></span>

### <span data-ttu-id="a6e17-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e17-112">-DefaultProfile</span></span>
<span data-ttu-id="a6e17-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a6e17-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6e17-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a6e17-114">-Force</span></span>
<span data-ttu-id="a6e17-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a6e17-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6e17-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="a6e17-116">-MlWebService</span></span>
<span data-ttu-id="a6e17-117">要移除的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="a6e17-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="a6e17-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6e17-118">-Name</span></span>
<span data-ttu-id="a6e17-119">要移除的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e17-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="a6e17-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e17-120">-ResourceGroupName</span></span>
<span data-ttu-id="a6e17-121">Web 服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="a6e17-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="a6e17-122">-確認</span><span class="sxs-lookup"><span data-stu-id="a6e17-122">-Confirm</span></span>
<span data-ttu-id="a6e17-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6e17-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e17-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e17-124">-WhatIf</span></span>
<span data-ttu-id="a6e17-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6e17-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6e17-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6e17-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e17-127">CommonParameters</span></span>
<span data-ttu-id="a6e17-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6e17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e17-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6e17-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e17-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a6e17-130">INPUTS</span></span>

### <span data-ttu-id="a6e17-131">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="a6e17-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a6e17-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a6e17-132">OUTPUTS</span></span>

### <span data-ttu-id="a6e17-133">System.void</span><span class="sxs-lookup"><span data-stu-id="a6e17-133">System.Void</span></span>

## <span data-ttu-id="a6e17-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a6e17-134">NOTES</span></span>
<span data-ttu-id="a6e17-135">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="a6e17-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a6e17-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6e17-136">RELATED LINKS</span></span>
