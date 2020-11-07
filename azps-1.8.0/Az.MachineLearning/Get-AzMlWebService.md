---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: fe304408ee236312c2e6c71324d6a2a34157ff58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786954"
---
# <span data-ttu-id="14de6-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="14de6-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="14de6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14de6-102">SYNOPSIS</span></span>
<span data-ttu-id="14de6-103">檢索一或多個 web 服務的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="14de6-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="14de6-104">句法</span><span class="sxs-lookup"><span data-stu-id="14de6-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14de6-105">說明</span><span class="sxs-lookup"><span data-stu-id="14de6-105">DESCRIPTION</span></span>
<span data-ttu-id="14de6-106">檢索 web 服務的所需資訊。</span><span class="sxs-lookup"><span data-stu-id="14de6-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="14de6-107">根據已傳送的 paramenters，Cmdlet 會針對特定的 web 服務、針對目前訂閱中指定資源群組的 web 服務 defintions 集合，或針對目前訂閱中的 web 服務的 defintions，傳回該集合。</span><span class="sxs-lookup"><span data-stu-id="14de6-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="14de6-108">示例</span><span class="sxs-lookup"><span data-stu-id="14de6-108">EXAMPLES</span></span>

### <span data-ttu-id="14de6-109">範例1：取得特定 web 服務的詳細資料</span><span class="sxs-lookup"><span data-stu-id="14de6-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="14de6-110">範例2：取得目前訂閱中的所有 web 服務資源</span><span class="sxs-lookup"><span data-stu-id="14de6-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="14de6-111">範例3：取得目前訂閱與指定資源群組中的所有 web 服務</span><span class="sxs-lookup"><span data-stu-id="14de6-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="14de6-112">參數</span><span class="sxs-lookup"><span data-stu-id="14de6-112">PARAMETERS</span></span>

### <span data-ttu-id="14de6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14de6-113">-DefaultProfile</span></span>
<span data-ttu-id="14de6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="14de6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14de6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="14de6-115">-Name</span></span>
<span data-ttu-id="14de6-116">要為其檢索詳細資料之 web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="14de6-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="14de6-117">-Region</span><span class="sxs-lookup"><span data-stu-id="14de6-117">-Region</span></span>
<span data-ttu-id="14de6-118">Regio 的名稱</span><span class="sxs-lookup"><span data-stu-id="14de6-118">The name of regio</span></span>

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

### <span data-ttu-id="14de6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14de6-119">-ResourceGroupName</span></span>
<span data-ttu-id="14de6-120">從哪個資源群組檢索 web 服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="14de6-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="14de6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14de6-121">CommonParameters</span></span>
<span data-ttu-id="14de6-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14de6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14de6-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14de6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14de6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="14de6-124">INPUTS</span></span>

### <span data-ttu-id="14de6-125">所有</span><span class="sxs-lookup"><span data-stu-id="14de6-125">None</span></span>

## <span data-ttu-id="14de6-126">輸出</span><span class="sxs-lookup"><span data-stu-id="14de6-126">OUTPUTS</span></span>

### <span data-ttu-id="14de6-127">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="14de6-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="14de6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="14de6-128">NOTES</span></span>
<span data-ttu-id="14de6-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="14de6-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="14de6-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="14de6-130">RELATED LINKS</span></span>
