---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281883"
---
# <span data-ttu-id="80f52-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="80f52-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="80f52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80f52-102">SYNOPSIS</span></span>
<span data-ttu-id="80f52-103">將 JSON 物件匯入至 web 服務定義。</span><span class="sxs-lookup"><span data-stu-id="80f52-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="80f52-104">句法</span><span class="sxs-lookup"><span data-stu-id="80f52-104">SYNTAX</span></span>

### <span data-ttu-id="80f52-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="80f52-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80f52-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="80f52-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f52-107">說明</span><span class="sxs-lookup"><span data-stu-id="80f52-107">DESCRIPTION</span></span>
<span data-ttu-id="80f52-108">Import-AzMlWebService Cmdlet 會直接或在參照檔案中指定，並建立可傳遞至 New-AzMlWebService Cmdlet 的 web 服務定義物件。</span><span class="sxs-lookup"><span data-stu-id="80f52-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="80f52-109">示例</span><span class="sxs-lookup"><span data-stu-id="80f52-109">EXAMPLES</span></span>

### <span data-ttu-id="80f52-110">範例1：從字串匯入</span><span class="sxs-lookup"><span data-stu-id="80f52-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="80f52-111">範例2：從檔案路徑匯入</span><span class="sxs-lookup"><span data-stu-id="80f52-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="80f52-112">參數</span><span class="sxs-lookup"><span data-stu-id="80f52-112">PARAMETERS</span></span>

### <span data-ttu-id="80f52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f52-113">-DefaultProfile</span></span>
<span data-ttu-id="80f52-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="80f52-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80f52-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="80f52-115">-InputFile</span></span>
<span data-ttu-id="80f52-116">檔案的路徑，該檔案包含要匯入的 web 服務定義。</span><span class="sxs-lookup"><span data-stu-id="80f52-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="80f52-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="80f52-117">-JsonString</span></span>
<span data-ttu-id="80f52-118">包含要匯入之 web 服務定義的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="80f52-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="80f52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f52-119">CommonParameters</span></span>
<span data-ttu-id="80f52-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80f52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f52-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80f52-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f52-122">輸入</span><span class="sxs-lookup"><span data-stu-id="80f52-122">INPUTS</span></span>

### <span data-ttu-id="80f52-123">所有</span><span class="sxs-lookup"><span data-stu-id="80f52-123">None</span></span>

## <span data-ttu-id="80f52-124">輸出</span><span class="sxs-lookup"><span data-stu-id="80f52-124">OUTPUTS</span></span>

### <span data-ttu-id="80f52-125">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="80f52-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="80f52-126">筆記</span><span class="sxs-lookup"><span data-stu-id="80f52-126">NOTES</span></span>
<span data-ttu-id="80f52-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="80f52-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="80f52-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="80f52-128">RELATED LINKS</span></span>
