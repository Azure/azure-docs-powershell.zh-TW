---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456555"
---
# <span data-ttu-id="ee74c-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="ee74c-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="ee74c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee74c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee74c-103">檢索 web 服務的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ee74c-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee74c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee74c-104">SYNTAX</span></span>

### <span data-ttu-id="ee74c-105">取得已知其名稱和資源群組的 Azure ML web 服務便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ee74c-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee74c-106">取得特定 web 服務實例的存取 kesy。</span><span class="sxs-lookup"><span data-stu-id="ee74c-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee74c-107">說明</span><span class="sxs-lookup"><span data-stu-id="ee74c-107">DESCRIPTION</span></span>
<span data-ttu-id="ee74c-108">取得 Azure 電腦學習 web 服務的執行時間 Api 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ee74c-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="ee74c-109">示例</span><span class="sxs-lookup"><span data-stu-id="ee74c-109">EXAMPLES</span></span>

### <span data-ttu-id="ee74c-110">--------------------------範例 1-取得由資源群組和名稱所指定之 web 服務的按鍵--------------------------</span><span class="sxs-lookup"><span data-stu-id="ee74c-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="ee74c-111">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ee74c-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="ee74c-112">--------------------------範例 2-取得 web 服務實例的按鍵--------------------------</span><span class="sxs-lookup"><span data-stu-id="ee74c-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="ee74c-113">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ee74c-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="ee74c-114">[$mlService] 是 WebServices MachineLearning 的物件，可使用 WebService。</span><span class="sxs-lookup"><span data-stu-id="ee74c-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="ee74c-115">參數</span><span class="sxs-lookup"><span data-stu-id="ee74c-115">PARAMETERS</span></span>

### <span data-ttu-id="ee74c-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="ee74c-116">-MlWebService</span></span>
<span data-ttu-id="ee74c-117">要為其檢索便捷鍵的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ee74c-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee74c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee74c-118">-Name</span></span>
<span data-ttu-id="ee74c-119">要為其檢索便捷鍵的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ee74c-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee74c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee74c-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee74c-121">Web 服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="ee74c-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee74c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee74c-122">-DefaultProfile</span></span>
<span data-ttu-id="ee74c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee74c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee74c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee74c-124">CommonParameters</span></span>
<span data-ttu-id="ee74c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee74c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee74c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee74c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee74c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ee74c-127">INPUTS</span></span>

### <span data-ttu-id="ee74c-128">WebService</span><span class="sxs-lookup"><span data-stu-id="ee74c-128">WebService</span></span>
<span data-ttu-id="ee74c-129">"MlWebService" 參數接受來自管線的 "WebService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ee74c-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="ee74c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ee74c-130">OUTPUTS</span></span>

### <span data-ttu-id="ee74c-131">所有</span><span class="sxs-lookup"><span data-stu-id="ee74c-131">None</span></span>

## <span data-ttu-id="ee74c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ee74c-132">NOTES</span></span>
<span data-ttu-id="ee74c-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="ee74c-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ee74c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee74c-134">RELATED LINKS</span></span>

