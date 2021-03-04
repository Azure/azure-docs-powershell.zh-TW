---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b645154e9aaa011fccf1fa01624481e44b4eebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902010"
---
# <span data-ttu-id="f7fa4-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="f7fa4-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="f7fa4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fa4-103">建立區域 Web 服務屬性。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="f7fa4-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7fa4-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7fa4-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="f7fa4-106">為現有的 Web 服務建立 Azure 機器學習地區屬性。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="f7fa4-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="f7fa4-108">範例 1：新增美國中西部的新地區屬性</span><span class="sxs-lookup"><span data-stu-id="f7fa4-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="f7fa4-109">此範例命令會針對「美國中西部」地區的 Web 服務建立地區屬性。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="f7fa4-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7fa4-110">PARAMETERS</span></span>

### <span data-ttu-id="f7fa4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fa4-111">-DefaultProfile</span></span>
<span data-ttu-id="f7fa4-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f7fa4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7fa4-113">-強制</span><span class="sxs-lookup"><span data-stu-id="f7fa4-113">-Force</span></span>
<span data-ttu-id="f7fa4-114">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f7fa4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7fa4-115">-Name</span></span>
<span data-ttu-id="f7fa4-116">Web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7fa4-117">-區域</span><span class="sxs-lookup"><span data-stu-id="f7fa4-117">-Region</span></span>
<span data-ttu-id="f7fa4-118">建立 Web 服務屬性的區域。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7fa4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7fa4-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7fa4-120">Web 服務所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7fa4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f7fa4-121">-Confirm</span></span>
<span data-ttu-id="f7fa4-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7fa4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7fa4-123">-WhatIf</span></span>
<span data-ttu-id="f7fa4-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7fa4-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7fa4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fa4-126">CommonParameters</span></span>
<span data-ttu-id="f7fa4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fa4-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7fa4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fa4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f7fa4-129">INPUTS</span></span>

### <span data-ttu-id="f7fa4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f7fa4-130">System.String</span></span>

## <span data-ttu-id="f7fa4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f7fa4-131">OUTPUTS</span></span>

### <span data-ttu-id="f7fa4-132">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="f7fa4-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f7fa4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f7fa4-133">NOTES</span></span>
<span data-ttu-id="f7fa4-134">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="f7fa4-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f7fa4-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7fa4-135">RELATED LINKS</span></span>
