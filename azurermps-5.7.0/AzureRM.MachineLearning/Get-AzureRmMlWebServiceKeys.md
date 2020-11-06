---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449885"
---
# <span data-ttu-id="f55a4-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f55a4-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="f55a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f55a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f55a4-103">檢索 web 服務的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f55a4-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f55a4-104">SYNTAX</span></span>

### <span data-ttu-id="f55a4-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f55a4-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f55a4-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="f55a4-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f55a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="f55a4-107">DESCRIPTION</span></span>
<span data-ttu-id="f55a4-108">取得 Azure 電腦學習 web 服務的執行時間 Api 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f55a4-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="f55a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="f55a4-109">EXAMPLES</span></span>

### <span data-ttu-id="f55a4-110">--------------------------範例 1-取得由資源群組和名稱所指定之 web 服務的按鍵--------------------------</span><span class="sxs-lookup"><span data-stu-id="f55a4-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="f55a4-111">--------------------------範例 2-取得 web 服務實例的按鍵--------------------------</span><span class="sxs-lookup"><span data-stu-id="f55a4-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="f55a4-112">[$mlService] 是 WebServices MachineLearning 的物件，可使用 WebService。</span><span class="sxs-lookup"><span data-stu-id="f55a4-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="f55a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="f55a4-113">PARAMETERS</span></span>

### <span data-ttu-id="f55a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55a4-114">-DefaultProfile</span></span>
<span data-ttu-id="f55a4-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f55a4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f55a4-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f55a4-116">-MlWebService</span></span>
<span data-ttu-id="f55a4-117">要為其檢索便捷鍵的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f55a4-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55a4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f55a4-118">-Name</span></span>
<span data-ttu-id="f55a4-119">要為其檢索便捷鍵的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f55a4-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55a4-120">-ResourceGroupName</span></span>
<span data-ttu-id="f55a4-121">Web 服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f55a4-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55a4-122">CommonParameters</span></span>
<span data-ttu-id="f55a4-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f55a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55a4-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f55a4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55a4-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f55a4-125">INPUTS</span></span>

### <span data-ttu-id="f55a4-126">WebService</span><span class="sxs-lookup"><span data-stu-id="f55a4-126">WebService</span></span>
<span data-ttu-id="f55a4-127">"MlWebService" 參數接受來自管線的 "WebService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f55a4-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f55a4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f55a4-128">OUTPUTS</span></span>

### <span data-ttu-id="f55a4-129">所有</span><span class="sxs-lookup"><span data-stu-id="f55a4-129">None</span></span>

## <span data-ttu-id="f55a4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f55a4-130">NOTES</span></span>
<span data-ttu-id="f55a4-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="f55a4-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f55a4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f55a4-132">RELATED LINKS</span></span>

