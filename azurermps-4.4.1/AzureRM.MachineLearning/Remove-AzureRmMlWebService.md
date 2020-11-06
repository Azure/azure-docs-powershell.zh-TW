---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451656"
---
# <span data-ttu-id="80c60-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="80c60-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="80c60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80c60-102">SYNOPSIS</span></span>
<span data-ttu-id="80c60-103">刪除 web 服務。</span><span class="sxs-lookup"><span data-stu-id="80c60-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80c60-104">句法</span><span class="sxs-lookup"><span data-stu-id="80c60-104">SYNTAX</span></span>

### <span data-ttu-id="80c60-105">依名稱和資源群組移除 Azure ML web 服務資源。</span><span class="sxs-lookup"><span data-stu-id="80c60-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c60-106">移除指定為物件的 Azure ML web 服務。</span><span class="sxs-lookup"><span data-stu-id="80c60-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c60-107">說明</span><span class="sxs-lookup"><span data-stu-id="80c60-107">DESCRIPTION</span></span>
<span data-ttu-id="80c60-108">刪除由資源群組和名稱所參照的 Azure 電腦學習 web 服務。</span><span class="sxs-lookup"><span data-stu-id="80c60-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="80c60-109">示例</span><span class="sxs-lookup"><span data-stu-id="80c60-109">EXAMPLES</span></span>

### <span data-ttu-id="80c60-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80c60-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="80c60-111">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="80c60-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="80c60-112">參數</span><span class="sxs-lookup"><span data-stu-id="80c60-112">PARAMETERS</span></span>

### <span data-ttu-id="80c60-113">-Force</span><span class="sxs-lookup"><span data-stu-id="80c60-113">-Force</span></span>
<span data-ttu-id="80c60-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="80c60-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="80c60-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="80c60-115">-MlWebService</span></span>
<span data-ttu-id="80c60-116">要移除的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="80c60-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80c60-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="80c60-117">-Name</span></span>
<span data-ttu-id="80c60-118">要移除的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="80c60-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c60-119">-ResourceGroupName</span></span>
<span data-ttu-id="80c60-120">Web 服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="80c60-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c60-121">-確認</span><span class="sxs-lookup"><span data-stu-id="80c60-121">-Confirm</span></span>
<span data-ttu-id="80c60-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80c60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c60-123">-WhatIf</span></span>
<span data-ttu-id="80c60-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80c60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c60-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80c60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c60-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c60-126">-DefaultProfile</span></span>
<span data-ttu-id="80c60-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80c60-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c60-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c60-128">CommonParameters</span></span>
<span data-ttu-id="80c60-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80c60-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c60-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80c60-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c60-131">輸入</span><span class="sxs-lookup"><span data-stu-id="80c60-131">INPUTS</span></span>

### <span data-ttu-id="80c60-132">WebService</span><span class="sxs-lookup"><span data-stu-id="80c60-132">WebService</span></span>
<span data-ttu-id="80c60-133">"MlWebService" 參數接受來自管線的 "WebService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="80c60-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="80c60-134">輸出</span><span class="sxs-lookup"><span data-stu-id="80c60-134">OUTPUTS</span></span>

### <span data-ttu-id="80c60-135">所有</span><span class="sxs-lookup"><span data-stu-id="80c60-135">None</span></span>

## <span data-ttu-id="80c60-136">筆記</span><span class="sxs-lookup"><span data-stu-id="80c60-136">NOTES</span></span>
<span data-ttu-id="80c60-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="80c60-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="80c60-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="80c60-138">RELATED LINKS</span></span>

