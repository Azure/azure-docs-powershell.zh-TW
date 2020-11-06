---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456563"
---
# <span data-ttu-id="df04c-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="df04c-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="df04c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df04c-102">SYNOPSIS</span></span>
<span data-ttu-id="df04c-103">檢索一或多個 web 服務的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="df04c-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df04c-104">句法</span><span class="sxs-lookup"><span data-stu-id="df04c-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df04c-105">說明</span><span class="sxs-lookup"><span data-stu-id="df04c-105">DESCRIPTION</span></span>
<span data-ttu-id="df04c-106">檢索 web 服務的所需資訊。</span><span class="sxs-lookup"><span data-stu-id="df04c-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="df04c-107">根據已傳送的 paramenters，Cmdlet 會針對特定的 web 服務、針對目前訂閱中指定資源群組的 web 服務 defintions 集合，或針對目前訂閱中的 web 服務的 defintions，傳回該集合。</span><span class="sxs-lookup"><span data-stu-id="df04c-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="df04c-108">示例</span><span class="sxs-lookup"><span data-stu-id="df04c-108">EXAMPLES</span></span>

### <span data-ttu-id="df04c-109">--------------------------範例1：取得特定 web 服務的詳細資料--------------------------</span><span class="sxs-lookup"><span data-stu-id="df04c-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="df04c-110">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="df04c-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="df04c-111">--------------------------範例2：取得目前訂閱中的所有 web 服務資源--------------------------</span><span class="sxs-lookup"><span data-stu-id="df04c-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="df04c-112">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="df04c-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="df04c-113">--------------------------範例3：取得目前訂閱和指定資源群組中的所有 web 服務--------------------------</span><span class="sxs-lookup"><span data-stu-id="df04c-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="df04c-114">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="df04c-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="df04c-115">參數</span><span class="sxs-lookup"><span data-stu-id="df04c-115">PARAMETERS</span></span>

### <span data-ttu-id="df04c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="df04c-116">-Name</span></span>
<span data-ttu-id="df04c-117">要為其檢索詳細資料之 web 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="df04c-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="df04c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df04c-118">-ResourceGroupName</span></span>
<span data-ttu-id="df04c-119">從哪個資源群組檢索 web 服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="df04c-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="df04c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df04c-120">-DefaultProfile</span></span>
<span data-ttu-id="df04c-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df04c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df04c-122">-Region</span><span class="sxs-lookup"><span data-stu-id="df04c-122">-Region</span></span>
<span data-ttu-id="df04c-123">地區名稱</span><span class="sxs-lookup"><span data-stu-id="df04c-123">The name of region</span></span>

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

### <span data-ttu-id="df04c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df04c-124">CommonParameters</span></span>
<span data-ttu-id="df04c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df04c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df04c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df04c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df04c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="df04c-127">INPUTS</span></span>

## <span data-ttu-id="df04c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="df04c-128">OUTPUTS</span></span>

### <span data-ttu-id="df04c-129">所有</span><span class="sxs-lookup"><span data-stu-id="df04c-129">None</span></span>

## <span data-ttu-id="df04c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="df04c-130">NOTES</span></span>
<span data-ttu-id="df04c-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="df04c-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="df04c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="df04c-132">RELATED LINKS</span></span>

