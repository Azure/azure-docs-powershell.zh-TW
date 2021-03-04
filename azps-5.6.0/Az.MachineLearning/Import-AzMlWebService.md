---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: e30ecc151da5e4a202b8da63f8d57a8f25c387dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904390"
---
# <span data-ttu-id="1d378-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="1d378-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="1d378-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1d378-102">SYNOPSIS</span></span>
<span data-ttu-id="1d378-103">將 JSON 物件導入 Web 服務定義。</span><span class="sxs-lookup"><span data-stu-id="1d378-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="1d378-104">語法</span><span class="sxs-lookup"><span data-stu-id="1d378-104">SYNTAX</span></span>

### <span data-ttu-id="1d378-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="1d378-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d378-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="1d378-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d378-107">描述</span><span class="sxs-lookup"><span data-stu-id="1d378-107">DESCRIPTION</span></span>
<span data-ttu-id="1d378-108">Cmdlet Import-AzMlWebService直接指定或在參照的檔案中指定 ，然後建立可傳遞至 New-AzMlWebService Cmdlet 的 Web 服務定義物件。</span><span class="sxs-lookup"><span data-stu-id="1d378-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="1d378-109">例子</span><span class="sxs-lookup"><span data-stu-id="1d378-109">EXAMPLES</span></span>

### <span data-ttu-id="1d378-110">範例 1：從字串進行匯出</span><span class="sxs-lookup"><span data-stu-id="1d378-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="1d378-111">範例 2：從檔案路徑進行匯出</span><span class="sxs-lookup"><span data-stu-id="1d378-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="1d378-112">參數</span><span class="sxs-lookup"><span data-stu-id="1d378-112">PARAMETERS</span></span>

### <span data-ttu-id="1d378-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d378-113">-DefaultProfile</span></span>
<span data-ttu-id="1d378-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1d378-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d378-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1d378-115">-InputFile</span></span>
<span data-ttu-id="1d378-116">包含要匯出之 Web 服務定義之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1d378-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d378-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="1d378-117">-JsonString</span></span>
<span data-ttu-id="1d378-118">包含要匯出之 Web 服務定義的 JSON 格式化字串。</span><span class="sxs-lookup"><span data-stu-id="1d378-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d378-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d378-119">CommonParameters</span></span>
<span data-ttu-id="1d378-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1d378-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d378-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1d378-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d378-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1d378-122">INPUTS</span></span>

### <span data-ttu-id="1d378-123">沒有</span><span class="sxs-lookup"><span data-stu-id="1d378-123">None</span></span>

## <span data-ttu-id="1d378-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1d378-124">OUTPUTS</span></span>

### <span data-ttu-id="1d378-125">Microsoft.Azure.management.MachineLearning.WebServices.models.WebService</span><span class="sxs-lookup"><span data-stu-id="1d378-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1d378-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1d378-126">NOTES</span></span>
<span data-ttu-id="1d378-127">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="1d378-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1d378-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d378-128">RELATED LINKS</span></span>
