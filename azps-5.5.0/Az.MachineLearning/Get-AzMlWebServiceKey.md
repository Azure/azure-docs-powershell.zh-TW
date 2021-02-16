---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132778"
---
# <span data-ttu-id="8140b-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="8140b-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="8140b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8140b-102">SYNOPSIS</span></span>
<span data-ttu-id="8140b-103">檢索 web 服務的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8140b-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="8140b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8140b-104">SYNTAX</span></span>

### <span data-ttu-id="8140b-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8140b-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8140b-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="8140b-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8140b-107">說明</span><span class="sxs-lookup"><span data-stu-id="8140b-107">DESCRIPTION</span></span>
<span data-ttu-id="8140b-108">取得 Azure 電腦學習 web 服務的執行時間 Api 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8140b-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="8140b-109">示例</span><span class="sxs-lookup"><span data-stu-id="8140b-109">EXAMPLES</span></span>

### <span data-ttu-id="8140b-110">範例 1-取得由資源群組和名稱所指定之 web 服務的按鍵</span><span class="sxs-lookup"><span data-stu-id="8140b-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="8140b-111">範例 2-取得 web 服務實例的按鍵</span><span class="sxs-lookup"><span data-stu-id="8140b-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="8140b-112">[$mlService] 是 WebServices MachineLearning 的物件，可使用 WebService。</span><span class="sxs-lookup"><span data-stu-id="8140b-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="8140b-113">參數</span><span class="sxs-lookup"><span data-stu-id="8140b-113">PARAMETERS</span></span>

### <span data-ttu-id="8140b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8140b-114">-DefaultProfile</span></span>
<span data-ttu-id="8140b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8140b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8140b-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="8140b-116">-MlWebService</span></span>
<span data-ttu-id="8140b-117">要為其檢索便捷鍵的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8140b-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8140b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8140b-118">-Name</span></span>
<span data-ttu-id="8140b-119">要為其檢索便捷鍵的 web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8140b-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8140b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8140b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8140b-121">Web 服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="8140b-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8140b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8140b-122">CommonParameters</span></span>
<span data-ttu-id="8140b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8140b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8140b-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8140b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8140b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8140b-125">INPUTS</span></span>

### <span data-ttu-id="8140b-126">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="8140b-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="8140b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8140b-127">OUTPUTS</span></span>

### <span data-ttu-id="8140b-128">MachineLearning WebServices. WebServiceKeys （）</span><span class="sxs-lookup"><span data-stu-id="8140b-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="8140b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8140b-129">NOTES</span></span>
<span data-ttu-id="8140b-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="8140b-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8140b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8140b-131">RELATED LINKS</span></span>
