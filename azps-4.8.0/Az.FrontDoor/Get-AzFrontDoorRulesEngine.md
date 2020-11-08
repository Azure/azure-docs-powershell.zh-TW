---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136404"
---
# <span data-ttu-id="7854b-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="7854b-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="7854b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7854b-102">SYNOPSIS</span></span>
<span data-ttu-id="7854b-103">取得規則引擎設定。</span><span class="sxs-lookup"><span data-stu-id="7854b-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="7854b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7854b-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7854b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7854b-105">DESCRIPTION</span></span>
<span data-ttu-id="7854b-106">**AzFrontDoorRulesEngine** Cmdlet 會取得特定規則引擎配置，或取得與前門相關的所有規則引擎設定。</span><span class="sxs-lookup"><span data-stu-id="7854b-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="7854b-107">示例</span><span class="sxs-lookup"><span data-stu-id="7854b-107">EXAMPLES</span></span>

### <span data-ttu-id="7854b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7854b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="7854b-109">取得特定規則引擎配置。</span><span class="sxs-lookup"><span data-stu-id="7854b-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="7854b-110">範例2</span><span class="sxs-lookup"><span data-stu-id="7854b-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="7854b-111">在前門中取得所有規則引擎設定。</span><span class="sxs-lookup"><span data-stu-id="7854b-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="7854b-112">範例3</span><span class="sxs-lookup"><span data-stu-id="7854b-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="7854b-113">在取得不存在的規則引擎時，預期的輸出。</span><span class="sxs-lookup"><span data-stu-id="7854b-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="7854b-114">參數</span><span class="sxs-lookup"><span data-stu-id="7854b-114">PARAMETERS</span></span>

### <span data-ttu-id="7854b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7854b-115">-DefaultProfile</span></span>
<span data-ttu-id="7854b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7854b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7854b-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="7854b-117">-FrontDoorName</span></span>
<span data-ttu-id="7854b-118">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="7854b-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7854b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7854b-119">-Name</span></span>
<span data-ttu-id="7854b-120">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="7854b-120">Rules engine name.</span></span>

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

### <span data-ttu-id="7854b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7854b-121">-ResourceGroupName</span></span>
<span data-ttu-id="7854b-122">在其中建立前蓋的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="7854b-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7854b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7854b-123">CommonParameters</span></span>
<span data-ttu-id="7854b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7854b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7854b-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7854b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7854b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7854b-126">INPUTS</span></span>

### <span data-ttu-id="7854b-127">所有</span><span class="sxs-lookup"><span data-stu-id="7854b-127">None</span></span>

## <span data-ttu-id="7854b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7854b-128">OUTPUTS</span></span>

### <span data-ttu-id="7854b-129">PSRulesEngine 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="7854b-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="7854b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7854b-130">NOTES</span></span>

## <span data-ttu-id="7854b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7854b-131">RELATED LINKS</span></span>