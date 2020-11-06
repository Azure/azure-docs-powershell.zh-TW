---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457552"
---
# <span data-ttu-id="7f2b9-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="7f2b9-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="7f2b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2b9-103">建立區域 web 服務屬性。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f2b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f2b9-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="7f2b9-106">針對現有的 web 服務建立 Azure 機器學習區域屬性。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="7f2b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f2b9-107">EXAMPLES</span></span>

### <span data-ttu-id="7f2b9-108">--------------------------範例1：新增新的地區屬性給 West 美國中部--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f2b9-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="7f2b9-109">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7f2b9-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="7f2b9-110">這個範例命令會在「西部美國中部」區域中建立 web 服務的地區性屬性。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="7f2b9-111">參數</span><span class="sxs-lookup"><span data-stu-id="7f2b9-111">PARAMETERS</span></span>

### <span data-ttu-id="7f2b9-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7f2b9-112">-Force</span></span>
<span data-ttu-id="7f2b9-113">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7f2b9-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f2b9-114">-Name</span></span>
<span data-ttu-id="7f2b9-115">Web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-115">The name for the web service.</span></span>

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

### <span data-ttu-id="7f2b9-116">-Region</span><span class="sxs-lookup"><span data-stu-id="7f2b9-116">-Region</span></span>
<span data-ttu-id="7f2b9-117">要在其中建立 web 服務屬性的區域。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-117">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="7f2b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f2b9-119">Web 服務所屬的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="7f2b9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="7f2b9-120">-Confirm</span></span>
<span data-ttu-id="7f2b9-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2b9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2b9-122">-WhatIf</span></span>
<span data-ttu-id="7f2b9-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f2b9-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2b9-125">-DefaultProfile</span></span>
<span data-ttu-id="7f2b9-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f2b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2b9-127">CommonParameters</span></span>
<span data-ttu-id="7f2b9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2b9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2b9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7f2b9-130">INPUTS</span></span>

## <span data-ttu-id="7f2b9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7f2b9-131">OUTPUTS</span></span>

### <span data-ttu-id="7f2b9-132">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="7f2b9-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="7f2b9-133">Azure 機器學習 web 服務的摘要描述。</span><span class="sxs-lookup"><span data-stu-id="7f2b9-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="7f2b9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7f2b9-134">NOTES</span></span>
<span data-ttu-id="7f2b9-135">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="7f2b9-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7f2b9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f2b9-136">RELATED LINKS</span></span>

