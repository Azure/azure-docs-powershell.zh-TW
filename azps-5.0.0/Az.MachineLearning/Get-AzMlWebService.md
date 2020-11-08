---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141556"
---
# <span data-ttu-id="76177-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="76177-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="76177-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76177-102">SYNOPSIS</span></span>
<span data-ttu-id="76177-103">檢索一或多個 web 服務的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="76177-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="76177-104">句法</span><span class="sxs-lookup"><span data-stu-id="76177-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76177-105">說明</span><span class="sxs-lookup"><span data-stu-id="76177-105">DESCRIPTION</span></span>
<span data-ttu-id="76177-106">檢索 web 服務定義資訊。</span><span class="sxs-lookup"><span data-stu-id="76177-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="76177-107">根據傳遞的參數，此 Cmdlet 會傳回特定 web 服務的定義、目前訂閱中指定資源群組的 web 服務定義集合，或是目前訂閱中的 web 服務定義集合。</span><span class="sxs-lookup"><span data-stu-id="76177-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="76177-108">示例</span><span class="sxs-lookup"><span data-stu-id="76177-108">EXAMPLES</span></span>

### <span data-ttu-id="76177-109">範例1：取得特定 web 服務的詳細資料</span><span class="sxs-lookup"><span data-stu-id="76177-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="76177-110">範例2：取得目前訂閱中的所有 web 服務資源</span><span class="sxs-lookup"><span data-stu-id="76177-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="76177-111">範例3：取得目前訂閱與指定資源群組中的所有 web 服務</span><span class="sxs-lookup"><span data-stu-id="76177-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="76177-112">參數</span><span class="sxs-lookup"><span data-stu-id="76177-112">PARAMETERS</span></span>

### <span data-ttu-id="76177-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76177-113">-DefaultProfile</span></span>
<span data-ttu-id="76177-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="76177-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76177-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="76177-115">-Name</span></span>
<span data-ttu-id="76177-116">要為其檢索詳細資料之 web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="76177-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76177-117">-Region</span><span class="sxs-lookup"><span data-stu-id="76177-117">-Region</span></span>
<span data-ttu-id="76177-118">地區名稱</span><span class="sxs-lookup"><span data-stu-id="76177-118">The name of region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76177-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76177-119">-ResourceGroupName</span></span>
<span data-ttu-id="76177-120">從哪個資源群組檢索 web 服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="76177-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76177-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76177-121">CommonParameters</span></span>
<span data-ttu-id="76177-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76177-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76177-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76177-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76177-124">輸入</span><span class="sxs-lookup"><span data-stu-id="76177-124">INPUTS</span></span>

### <span data-ttu-id="76177-125">所有</span><span class="sxs-lookup"><span data-stu-id="76177-125">None</span></span>

## <span data-ttu-id="76177-126">輸出</span><span class="sxs-lookup"><span data-stu-id="76177-126">OUTPUTS</span></span>

### <span data-ttu-id="76177-127">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="76177-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="76177-128">筆記</span><span class="sxs-lookup"><span data-stu-id="76177-128">NOTES</span></span>
<span data-ttu-id="76177-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="76177-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="76177-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="76177-130">RELATED LINKS</span></span>
