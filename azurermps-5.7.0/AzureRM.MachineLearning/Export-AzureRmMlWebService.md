---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: fd07ab55fad93fdf48df52e15db846630ba6c1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455392"
---
# <span data-ttu-id="35771-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="35771-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="35771-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35771-102">SYNOPSIS</span></span>
<span data-ttu-id="35771-103">將 web 服務定義物件匯出為 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="35771-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35771-104">句法</span><span class="sxs-lookup"><span data-stu-id="35771-104">SYNTAX</span></span>

### <span data-ttu-id="35771-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="35771-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35771-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="35771-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35771-107">說明</span><span class="sxs-lookup"><span data-stu-id="35771-107">DESCRIPTION</span></span>
<span data-ttu-id="35771-108">以 JSON 格式字串的形式匯出指定網頁 servive 的定義物件。</span><span class="sxs-lookup"><span data-stu-id="35771-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="35771-109">您可以立即傳回字串，或將它儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="35771-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="35771-110">示例</span><span class="sxs-lookup"><span data-stu-id="35771-110">EXAMPLES</span></span>

### <span data-ttu-id="35771-111">--------------------------範例1：以字串形式匯出--------------------------</span><span class="sxs-lookup"><span data-stu-id="35771-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="35771-112">--------------------------範例2：匯出至檔案--------------------------</span><span class="sxs-lookup"><span data-stu-id="35771-112">--------------------------  Example 2: Export to file  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="35771-113">參數</span><span class="sxs-lookup"><span data-stu-id="35771-113">PARAMETERS</span></span>

### <span data-ttu-id="35771-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35771-114">-DefaultProfile</span></span>
<span data-ttu-id="35771-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="35771-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35771-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35771-116">-Force</span></span>
<span data-ttu-id="35771-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="35771-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="35771-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="35771-118">-OutputFile</span></span>
<span data-ttu-id="35771-119">匯出定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="35771-119">The file path for exported definition.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35771-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="35771-120">-ToJsonString</span></span>
<span data-ttu-id="35771-121">指定定義將匯出為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="35771-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToJSON
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35771-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="35771-122">-WebService</span></span>
<span data-ttu-id="35771-123">要匯出的 web 服務定義物件。</span><span class="sxs-lookup"><span data-stu-id="35771-123">The web service definition object to be exported.</span></span>

```yaml
Type: WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35771-124">-確認</span><span class="sxs-lookup"><span data-stu-id="35771-124">-Confirm</span></span>
<span data-ttu-id="35771-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35771-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35771-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35771-126">-WhatIf</span></span>
<span data-ttu-id="35771-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35771-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35771-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35771-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35771-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35771-129">CommonParameters</span></span>
<span data-ttu-id="35771-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35771-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35771-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35771-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35771-132">輸入</span><span class="sxs-lookup"><span data-stu-id="35771-132">INPUTS</span></span>

### <span data-ttu-id="35771-133">WebService</span><span class="sxs-lookup"><span data-stu-id="35771-133">WebService</span></span>
<span data-ttu-id="35771-134">參數「WebService」接受來自管線的 "WebService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="35771-134">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="35771-135">輸出</span><span class="sxs-lookup"><span data-stu-id="35771-135">OUTPUTS</span></span>

### <span data-ttu-id="35771-136">所有</span><span class="sxs-lookup"><span data-stu-id="35771-136">None</span></span>

## <span data-ttu-id="35771-137">筆記</span><span class="sxs-lookup"><span data-stu-id="35771-137">NOTES</span></span>
<span data-ttu-id="35771-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="35771-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="35771-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="35771-139">RELATED LINKS</span></span>

