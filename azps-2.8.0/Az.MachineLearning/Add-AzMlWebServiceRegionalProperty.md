---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611934"
---
# <span data-ttu-id="f3725-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="f3725-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="f3725-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3725-102">SYNOPSIS</span></span>
<span data-ttu-id="f3725-103">建立區域 web 服務屬性。</span><span class="sxs-lookup"><span data-stu-id="f3725-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="f3725-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3725-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3725-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3725-105">DESCRIPTION</span></span>
<span data-ttu-id="f3725-106">針對現有的 web 服務建立 Azure 機器學習區域屬性。</span><span class="sxs-lookup"><span data-stu-id="f3725-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="f3725-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3725-107">EXAMPLES</span></span>

### <span data-ttu-id="f3725-108">範例1：新增適用于 West 中北部的區域屬性</span><span class="sxs-lookup"><span data-stu-id="f3725-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="f3725-109">這個範例命令會在「西部美國中部」區域中建立 web 服務的地區性屬性。</span><span class="sxs-lookup"><span data-stu-id="f3725-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="f3725-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3725-110">PARAMETERS</span></span>

### <span data-ttu-id="f3725-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3725-111">-DefaultProfile</span></span>
<span data-ttu-id="f3725-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f3725-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3725-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f3725-113">-Force</span></span>
<span data-ttu-id="f3725-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f3725-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f3725-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3725-115">-Name</span></span>
<span data-ttu-id="f3725-116">Web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3725-116">The name for the web service.</span></span>

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

### <span data-ttu-id="f3725-117">-Region</span><span class="sxs-lookup"><span data-stu-id="f3725-117">-Region</span></span>
<span data-ttu-id="f3725-118">要在其中建立 web 服務屬性的區域。</span><span class="sxs-lookup"><span data-stu-id="f3725-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="f3725-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3725-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3725-120">Web 服務所屬的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f3725-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="f3725-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f3725-121">-Confirm</span></span>
<span data-ttu-id="f3725-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3725-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3725-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3725-123">-WhatIf</span></span>
<span data-ttu-id="f3725-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3725-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3725-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3725-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3725-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3725-126">CommonParameters</span></span>
<span data-ttu-id="f3725-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3725-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3725-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3725-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3725-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f3725-129">INPUTS</span></span>

### <span data-ttu-id="f3725-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f3725-130">System.String</span></span>

## <span data-ttu-id="f3725-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f3725-131">OUTPUTS</span></span>

### <span data-ttu-id="f3725-132">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="f3725-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f3725-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f3725-133">NOTES</span></span>
<span data-ttu-id="f3725-134">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="f3725-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f3725-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3725-135">RELATED LINKS</span></span>