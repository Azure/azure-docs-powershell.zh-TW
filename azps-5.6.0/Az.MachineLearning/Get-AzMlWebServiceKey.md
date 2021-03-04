---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: 05adf2476c922fdea17a69bd33f74570309349ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904393"
---
# <span data-ttu-id="46ba8-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="46ba8-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="46ba8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="46ba8-103">會取回 Web 服務的金鑰。</span><span class="sxs-lookup"><span data-stu-id="46ba8-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="46ba8-104">語法</span><span class="sxs-lookup"><span data-stu-id="46ba8-104">SYNTAX</span></span>

### <span data-ttu-id="46ba8-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46ba8-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46ba8-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="46ba8-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46ba8-107">描述</span><span class="sxs-lookup"><span data-stu-id="46ba8-107">DESCRIPTION</span></span>
<span data-ttu-id="46ba8-108">取得 Azure 機器學習 Web 服務執行時間 API 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="46ba8-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="46ba8-109">例子</span><span class="sxs-lookup"><span data-stu-id="46ba8-109">EXAMPLES</span></span>

### <span data-ttu-id="46ba8-110">範例 1 - 取得由資源群組和名稱指定的 Web 服務金鑰</span><span class="sxs-lookup"><span data-stu-id="46ba8-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="46ba8-111">範例 2 - 取得 Web 服務實例的金鑰</span><span class="sxs-lookup"><span data-stu-id="46ba8-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="46ba8-112">$mlService是 Microsoft.Azure.Management.MachineLearning.WebServices.models.WebService 類型的物件。</span><span class="sxs-lookup"><span data-stu-id="46ba8-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="46ba8-113">參數</span><span class="sxs-lookup"><span data-stu-id="46ba8-113">PARAMETERS</span></span>

### <span data-ttu-id="46ba8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ba8-114">-DefaultProfile</span></span>
<span data-ttu-id="46ba8-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="46ba8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46ba8-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="46ba8-116">-MlWebService</span></span>
<span data-ttu-id="46ba8-117">要取得便捷鍵的 Web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="46ba8-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="46ba8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="46ba8-118">-Name</span></span>
<span data-ttu-id="46ba8-119">要取得便捷鍵的 Web 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="46ba8-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="46ba8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ba8-120">-ResourceGroupName</span></span>
<span data-ttu-id="46ba8-121">Web 服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="46ba8-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="46ba8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ba8-122">CommonParameters</span></span>
<span data-ttu-id="46ba8-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46ba8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ba8-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="46ba8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ba8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="46ba8-125">INPUTS</span></span>

### <span data-ttu-id="46ba8-126">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="46ba8-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="46ba8-127">輸出</span><span class="sxs-lookup"><span data-stu-id="46ba8-127">OUTPUTS</span></span>

### <span data-ttu-id="46ba8-128">Microsoft.Azure.management.MachineLearning.WebServices.models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="46ba8-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="46ba8-129">筆記</span><span class="sxs-lookup"><span data-stu-id="46ba8-129">NOTES</span></span>
<span data-ttu-id="46ba8-130">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="46ba8-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="46ba8-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="46ba8-131">RELATED LINKS</span></span>
