---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: f8923c6f98dad44a56c35cadc4b3e1daedeb1227
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451664"
---
# <span data-ttu-id="b064c-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="b064c-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="b064c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b064c-102">SYNOPSIS</span></span>
<span data-ttu-id="b064c-103">將 web 服務定義物件匯出為 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="b064c-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b064c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b064c-104">SYNTAX</span></span>

### <span data-ttu-id="b064c-105">[匯出至檔案]。</span><span class="sxs-lookup"><span data-stu-id="b064c-105">Export to file.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b064c-106">匯出至 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="b064c-106">Export to JSON string.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b064c-107">說明</span><span class="sxs-lookup"><span data-stu-id="b064c-107">DESCRIPTION</span></span>
<span data-ttu-id="b064c-108">以 JSON 格式字串的形式匯出指定網頁 servive 的定義物件。</span><span class="sxs-lookup"><span data-stu-id="b064c-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="b064c-109">您可以立即傳回字串，或將它儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="b064c-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="b064c-110">示例</span><span class="sxs-lookup"><span data-stu-id="b064c-110">EXAMPLES</span></span>

### <span data-ttu-id="b064c-111">--------------------------範例1：以字串形式匯出--------------------------</span><span class="sxs-lookup"><span data-stu-id="b064c-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
<span data-ttu-id="b064c-112">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b064c-112">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="b064c-113">--------------------------範例2：匯出至檔案--------------------------</span><span class="sxs-lookup"><span data-stu-id="b064c-113">--------------------------  Example 2: Export to file  --------------------------</span></span>
<span data-ttu-id="b064c-114">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b064c-114">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="b064c-115">參數</span><span class="sxs-lookup"><span data-stu-id="b064c-115">PARAMETERS</span></span>

### <span data-ttu-id="b064c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b064c-116">-Force</span></span>
<span data-ttu-id="b064c-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b064c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b064c-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b064c-118">-OutputFile</span></span>
<span data-ttu-id="b064c-119">匯出定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b064c-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="b064c-120">-ToJsonString</span></span>
<span data-ttu-id="b064c-121">指定定義將匯出為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="b064c-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="b064c-122">-WebService</span></span>
<span data-ttu-id="b064c-123">要匯出的 web 服務定義物件。</span><span class="sxs-lookup"><span data-stu-id="b064c-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b064c-124">-Confirm</span></span>
<span data-ttu-id="b064c-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b064c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b064c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b064c-126">-WhatIf</span></span>
<span data-ttu-id="b064c-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b064c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b064c-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b064c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b064c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b064c-129">-DefaultProfile</span></span>
<span data-ttu-id="b064c-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b064c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b064c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b064c-131">CommonParameters</span></span>
<span data-ttu-id="b064c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b064c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b064c-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b064c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b064c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b064c-134">INPUTS</span></span>

### <span data-ttu-id="b064c-135">WebService</span><span class="sxs-lookup"><span data-stu-id="b064c-135">WebService</span></span>
<span data-ttu-id="b064c-136">參數「WebService」接受來自管線的 "WebService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b064c-136">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="b064c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b064c-137">OUTPUTS</span></span>

### <span data-ttu-id="b064c-138">所有</span><span class="sxs-lookup"><span data-stu-id="b064c-138">None</span></span>

## <span data-ttu-id="b064c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b064c-139">NOTES</span></span>
<span data-ttu-id="b064c-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="b064c-140">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b064c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b064c-141">RELATED LINKS</span></span>

