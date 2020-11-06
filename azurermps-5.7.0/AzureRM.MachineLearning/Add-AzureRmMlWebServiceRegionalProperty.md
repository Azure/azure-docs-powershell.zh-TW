---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b2f881b57639a83227c2f590ffd260b78509a54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455395"
---
# <span data-ttu-id="6781b-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="6781b-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="6781b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6781b-102">SYNOPSIS</span></span>
<span data-ttu-id="6781b-103">建立區域 web 服務屬性。</span><span class="sxs-lookup"><span data-stu-id="6781b-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6781b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6781b-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6781b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6781b-105">DESCRIPTION</span></span>
<span data-ttu-id="6781b-106">針對現有的 web 服務建立 Azure 機器學習區域屬性。</span><span class="sxs-lookup"><span data-stu-id="6781b-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="6781b-107">示例</span><span class="sxs-lookup"><span data-stu-id="6781b-107">EXAMPLES</span></span>

### <span data-ttu-id="6781b-108">--------------------------範例1：新增新的地區屬性給 West 美國中部--------------------------</span><span class="sxs-lookup"><span data-stu-id="6781b-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="6781b-109">這個範例命令會在「西部美國中部」區域中建立 web 服務的地區性屬性。</span><span class="sxs-lookup"><span data-stu-id="6781b-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="6781b-110">參數</span><span class="sxs-lookup"><span data-stu-id="6781b-110">PARAMETERS</span></span>

### <span data-ttu-id="6781b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6781b-111">-DefaultProfile</span></span>
<span data-ttu-id="6781b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6781b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6781b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6781b-113">-Force</span></span>
<span data-ttu-id="6781b-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6781b-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6781b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6781b-115">-Name</span></span>
<span data-ttu-id="6781b-116">Web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6781b-116">The name for the web service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6781b-117">-Region</span><span class="sxs-lookup"><span data-stu-id="6781b-117">-Region</span></span>
<span data-ttu-id="6781b-118">要在其中建立 web 服務屬性的區域。</span><span class="sxs-lookup"><span data-stu-id="6781b-118">The region in which to create the web service properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6781b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6781b-119">-ResourceGroupName</span></span>
<span data-ttu-id="6781b-120">Web 服務所屬的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="6781b-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6781b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="6781b-121">-Confirm</span></span>
<span data-ttu-id="6781b-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6781b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6781b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6781b-123">-WhatIf</span></span>
<span data-ttu-id="6781b-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6781b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6781b-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6781b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6781b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6781b-126">CommonParameters</span></span>
<span data-ttu-id="6781b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6781b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6781b-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6781b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6781b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6781b-129">INPUTS</span></span>

### <span data-ttu-id="6781b-130">所有</span><span class="sxs-lookup"><span data-stu-id="6781b-130">None</span></span>
<span data-ttu-id="6781b-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6781b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6781b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6781b-132">OUTPUTS</span></span>

### <span data-ttu-id="6781b-133">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="6781b-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="6781b-134">Azure 機器學習 web 服務的摘要描述。</span><span class="sxs-lookup"><span data-stu-id="6781b-134">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="6781b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6781b-135">NOTES</span></span>
<span data-ttu-id="6781b-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="6781b-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6781b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6781b-137">RELATED LINKS</span></span>

